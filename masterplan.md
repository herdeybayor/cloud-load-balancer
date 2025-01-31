# Cloud Load Balancer Implementation Master Plan

## 1. Project Setup & Environment Configuration

### Initial Setup
- Create private Git repository on Olympus (https://olympus.ntu.ac.uk)
- Set up NetBeans with Maven
- Install Scene Builder for JavaFX GUI development
- Configure Docker environment with required containers:
  - Main container (pedrombmachado/ntu_lubuntu:comp20081)
  - File storage containers (4x ubuntu:latest)
  - MySQL container

### Docker Configuration
- Create Docker Compose file to manage all containers
- Configure networking between containers
- Set up Docker volumes for persistent storage
- Implement health check mechanisms

## 2. Core Components Development

### Load Balancer Implementation
1. Core Functionality:
   - Request handling and distribution
   - Implementation of scheduling algorithms:
     - First-Come-First-Served (FCFS)
     - Shortest-Job-Next (SJN)
     - Round Robin (RR)
   - Health monitoring of file storage containers
   - Traffic management and load distribution

2. File Management System:
   - File chunking mechanism
   - Chunk distribution across containers
   - File reconstruction
   - Encryption/Decryption using AES
   - Concurrent access control

### Database Implementation
1. SQLite (Local):
   - User session management
   - Temporary file metadata
   - Cache management

2. MySQL (Remote):
   - User profiles
   - File metadata
   - Access control lists
   - Sharing permissions

3. Database Synchronization:
   - Implement sync mechanisms
   - Handle conflicts
   - Ensure data consistency

## 3. User Interface Development

### JavaFX GUI Implementation
1. User Management Screens:
   - Login/Registration
   - Profile management
   - Admin dashboard

2. File Management Interface:
   - File upload/download
   - File sharing
   - Permission management
   - Progress indicators

3. Terminal Emulation:
   - Implementation of required commands:
     - mv, cp, ls, mkdir, ps
     - whoami, tree, nano
   - Command history
   - Output display

## 4. Testing & Quality Assurance

### Testing Strategy
1. Unit Testing:
   - Load balancer components
   - File operations
   - Database operations

2. Integration Testing:
   - Container communication
   - Database synchronization
   - File distribution

3. Performance Testing:
   - Load testing
   - Concurrent access
   - Artificial delay simulation

### Security Implementation
- AES encryption for files
- Secure password handling
- Session management
- Access control enforcement

## 5. Documentation & Deployment

### Documentation
- Code documentation
- User manual
- API documentation
- System architecture documentation

### Deployment
- Docker container configuration
- Database initialization scripts
- Startup scripts
- Health check implementation

## 6. Presentation Preparation
- Create presentation using provided template (max 6 pages)
- Prepare live demonstration scenarios
- Document key features and implementations
- Prepare backup plans for demo

## Timeline & Milestones

1. Week 1-2: Project Setup & Basic Implementation
   - Environment setup
   - Basic GUI
   - Database structure

2. Week 3-4: Core Functionality
   - Load balancer
   - File management
   - User authentication

3. Week 5-6: Advanced Features
   - File chunking
   - Encryption
   - Terminal emulation

4. Week 7-8: Testing & Documentation
   - Testing
   - Bug fixes
   - Documentation
   - Presentation preparation

## Grade Targeting Requirements

### For 3rd (Pass):
- Basic user management
- Simple file operations
- Local SQLite implementation
- Basic GUI

### For 2:2:
- Additional container for file storage
- Traffic management
- Basic load balancing
- Artificial delay simulation

### For 2:1:
- Multiple containers
- Advanced file sharing
- Performance metrics
- Remote terminal emulation

### For 1st:
- Full container implementation
- Advanced load balancing
- Complete security features
- All additional features
