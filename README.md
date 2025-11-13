# 🔧 SOAP CXF Service - TP 12

**Service web SOAP avec Apache CXF (JAX-WS, JAXB, WSDL, WS-Security)**

[![Java](https://img.shields.io/badge/Java-17+-blue.svg)](https://java.com)
[![Maven](https://img.shields.io/badge/Maven-3.6+-orange.svg)](https://maven.apache.org)
[![CXF](https://img.shields.io/badge/Apache%20CXF-4.0.3-green.svg)](https://cxf.apache.org)
[![License](https://img.shields.io/badge/License-Educational-lightgrey.svg)](LICENSE)

## 🎯 Aperçu

Ce projet est une implémentation complète d'un service web SOAP utilisant **Apache CXF** dans le cadre du TP 12 du cours *Architecture Microservices*. Il démontre les concepts fondamentaux des services web SOAP avec une approche **code-first** et inclut la sécurisation via **WS-Security**.

### ✨ Fonctionnalités

- ✅ Service SOAP JAX-WS avec Apache CXF
- ✅ Sérialisation XML avec JAXB
- ✅ Génération automatique de WSDL
- ✅ Client Java généré via `wsdl2java`
- ✅ Sécurité WS-Security avec UsernameToken
- ✅ Tests avec SoapUI et client Java
- ✅ Serveur HTTP embarqué Jetty

## 🏗️ Architecture

### 📁 Structure du Projet

```bash
soap-cxf-service/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/acme/cxf/
│   │   │       ├── Server.java                 # Serveur non sécurisé
│   │   │       ├── SecureServer.java           # Serveur avec WS-Security
│   │   │       ├── api/
│   │   │       │   └── HelloService.java       # Interface du service
│   │   │       ├── impl/
│   │   │       │   └── HelloServiceImpl.java   # Implémentation
│   │   │       ├── model/
│   │   │       │   └── Person.java             # Modèle JAXB
│   │   │       ├── client/
│   │   │       │   └── ClientDemo.java         # Client de test
│   │   │       └── security/
│   │   │           └── UTPasswordCallback.java # Handler d'auth
│   │   └── resources/
```

## Tester le service avec SoapUI

<img width="1386" height="861" alt="Capture d’écran 2025-11-08 à 09 57 22" src="https://github.com/user-attachments/assets/9d425f67-c0cf-4cee-b07f-fff3e7687436" />
<img width="1386" height="861" alt="Capture d’écran 2025-11-08 à 09 57 10" src="https://github.com/user-attachments/assets/ffd645ee-ec64-4075-8d60-8e356db4b29c" />

## Ajouter WS-Security 

<img width="2940" height="1708" alt="image" src="https://github.com/user-attachments/assets/61e0602d-1dda-41f8-8649-4d88c050c130" />
<img width="2940" height="1708" alt="image" src="https://github.com/user-attachments/assets/8766740d-70a5-460b-8d57-ff3732e0adce" />

##  Conclusion
Ce TP m’a permis de comprendre comment créer et sécuriser un service SOAP avec Apache CXF en mode code-first.
J’ai appris à utiliser WS-Security (UsernameToken), à tester le service avec SoapUI, et à appliquer les bonnes pratiques de sécurité comme HTTPS et PasswordDigest.
│   └── test/
│       └── java/
├── pom.xml                                    # Configuration Maven
└── README.md
