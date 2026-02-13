# ☁️ MiniWeatherApp

**A lightweight weather application built with Go and optimized for Docker.**
> **Note:** Interface is in Polish.

<table>
  <td><img src="https://github.com/user-attachments/assets/a49160a4-f886-49f3-81fa-49da4cb85e0c"/></td>
</table>

## ✨ Features

- 🌤️ **Real-time Weather Data** - Get current weather information using OpenWeatherMap API
- 🌍 **Multi-country Support** - Works for cities in Poland, Germany, UK, and USA
- 🐳 **Docker Optimized** - Ultra-small Docker image
- 💪 **Health Monitoring** - Built-in health check endpoint
- ⚡ **Fast & Lightweight** - Written in Go for maximum performance
- 🔒 **Secure** - Runs on minimal `scratch` base image

## 🛠️ Technologies

- **Backend:** Go (Golang)
- **Frontend:** HTML/CSS/JavaScript
- **Containerization:** Docker
- **API:** OpenWeatherMap API
- **Compression:** UPX (Ultimate Packer for eXecutables)

## 🎯 Docker Optimization

This project showcases advanced Docker optimization techniques:

- **Multi-stage build** - Separate build and runtime stages
- **Static compilation** - Go binary compiled with all dependencies
- **UPX compression** - Executable compressed for minimal size
- **Scratch base image** - Smallest possible base image (no OS!)
- **Health checks** - Container health monitoring

### Build Results
- 📦 **Image size:** 4.44 MB
- 📊 **Layers:** 3
  
## 🚀 Getting Started

### Prerequisites

- Docker installed on your system
- OpenWeatherMap API key ([Get it free here](https://openweathermap.org/api))

### Quick Start with Docker

1. **Clone the repository**
   ```bash
   git clone https://github.com/r1ckshot/MiniWeatherApp.git
   cd MiniWeatherApp
   ```

2. **Build the Docker image**
   ```bash
   docker build -t weather-app:go .
   ```

3. **Run the container**
   ```bash
   docker run -d -p 5000:5000 \
     -e WEATHER_API_KEY=your_api_key_here \
     --name weather-container \
     weather-app:go
   ```
   
   > **Note:** Replace `your_api_key_here` with your actual OpenWeatherMap API key

4. **Access the application**
   - Open your browser and navigate to: `http://localhost:5000`

### Useful Docker Commands

```bash
# Check container logs
docker logs weather-container

# Check container health status
docker inspect weather-container | grep -A 10 "Health"

# View image details
docker image ls weather-app:go

# Check number of layers
docker image inspect weather-app:go --format='{{.RootFS.Layers}}' | wc -w

# Stop and remove container
docker stop weather-container
docker rm weather-container
```

## 📚 What I Learned

This project taught me important DevOps and backend development concepts:

- Go programming language basics & HTTP server creation
- Docker containerization
- Multi-stage Docker builds
- Image size reduction techniques
- Container health monitoring
- API integration and environment variables
- Static binary compilation

## 👨‍💻 Author

**Mykhailo Kapustianyk**
- GitHub: [@r1ckshot](https://github.com/r1ckshot)
- Year: 2025
