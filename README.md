# UNIVERSIDAD DE CARTAGENA  
## Ingeniería de Software  
### Trabajo Colaborativo Contextualizado  

---

# Sistema de Gestión Comunitaria de Casos, Incidencias y Servicios  
# TICKETS — Frontend

![Flutter](https://img.shields.io/badge/Flutter-3.x-blue?logo=flutter)
![Dart](https://img.shields.io/badge/Dart-3.x-blue?logo=dart)
![Status](https://img.shields.io/badge/Status-En%20desarrollo-yellow)

---

## Descripción

TICKETS es una plataforma de gestión comunitaria orientada al registro, seguimiento y control de casos, incidencias y servicios dentro de una comunidad.

Este repositorio corresponde al frontend móvil, desarrollado con Flutter y Dart, encargado de la interfaz de usuario, navegación y comunicación con el backend mediante API REST.

Permite a los usuarios:

- Registrar y gestionar casos  
- Reportar incidencias  
- Acceder a servicios comunitarios  
- Usar chat en tiempo real  
- Consultar historial de cambios  

---

## Tecnologías

- Flutter 3.x  
- Dart 3.x  

---

## Dependencias principales

```yaml
dependencies:
  flutter:
    sdk: flutter

  dio: ^5.4.0
  retrofit: ^4.1.0

  flutter_secure_storage: ^9.0.0
  jwt_decoder: ^2.0.1

  go_router: ^13.0.0
  flutter_riverpod: ^2.5.1

  flutter_svg: ^2.0.10
  cached_network_image: ^3.3.1
  intl: ^0.19.0

  equatable: ^2.0.5
  freezed_annotation: ^2.4.1
  json_annotation: ^4.9.0
```

---

## Requisitos

- Flutter SDK >= 3.0.0  
- Dart SDK >= 3.0.0  
- Android Studio o VS Code  
- Backend corriendo en: `http://localhost:8080`  

---

## Cómo empezar

### 1. Clonar repositorio
```bash
git clone git@github.com:KarinaRedondo/tickets-frontend.git
```

### 2. Instalar dependencias
```bash
flutter pub get
```

### 3. Configurar backend
```dart
const String baseUrl = 'http://localhost:8080/api/v1';
```

### 4. Generar código
```bash
flutter pub run build_runner build --delete-conflicting-outputs
```

### 5. Ejecutar app
```bash
flutter run
```

---

## Estructura del Proyecto

```bash
lib/
├── core/
├── data/
├── domain/
├── presentation/
├── routes/
└── main.dart
```

---

## Autenticación y Seguridad

Se utiliza JWT para autenticar usuarios.  
El token se almacena con `flutter_secure_storage` y se adjunta automáticamente a cada petición usando interceptores de Dio.

---

## Arquitectura

Se implementa arquitectura limpia basada en capas:

- Presentation: UI (Screens y Widgets)  
- State Management: Riverpod  
- Domain: Entidades y lógica  
- Data: Repositorios y consumo de API  

---

## Roles del Sistema

| Rol               | Descripción |
|------------------|------------|
| ADMIN_GENERAL     | Administra todo el sistema |
| ADMIN_COMUNIDAD   | Administra su comunidad |
| RESPONSABLE       | Gestiona casos asignados |
| USUARIO_GENERAL   | Reporta incidencias |

---

## Módulos

- Autenticación  
- Usuarios  
- Comunidades  
- Casos e Incidencias  
- Servicios  
- Chat  
- Historial  
- Reportes  

---

## Backend

- API: http://localhost:8080/api/v1  
- Swagger: http://localhost:8080/swagger-ui/index.html  

---

## Comandos útiles

| Comando | Descripción |
|--------|------------|
| flutter pub get | Instala dependencias |
| flutter run | Ejecuta la app |
| flutter build apk | Genera APK |
| flutter test | Ejecuta pruebas |

---

## Notas

Asegúrate de tener el backend en ejecución antes de iniciar la aplicación.

---

## Créditos

Proyecto desarrollado como parte del Trabajo Colaborativo Contextualizado  
Ingeniería de Software — Universidad de Cartagena
