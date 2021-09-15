---
description: Interfaz de programación de aplicaciones WPD
ms.assetid: 3e2be15f-7af7-4e76-89b1-f9bc591c4f1b
title: Interfaz de programación de aplicaciones WPD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c44dbcf731aa46941599b99766e52fa67a5c5a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572020"
---
# <a name="wpd-application-programming-interface"></a>Interfaz de programación de aplicaciones WPD

Las aplicaciones integradas en Windows Portable Devices pueden explorar un dispositivo, enviar y recibir contenido, e incluso controlar el dispositivo, por ejemplo, tomar una imagen o enviar un mensaje de texto. El sistema está diseñado para ser flexible para que se puedan explorar muchos tipos de dispositivos y ampliarse para que los desarrolladores de controladores puedan definir propiedades y comandos personalizados para dispositivos personalizados.

En la tabla siguiente se describen los temas principales de esta documentación.



| Tema                                                                                                                  | Descripción                                                                                                |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Requisitos generales para el desarrollo de aplicaciones](general-requirements-for-application-development.md)               | Requisitos de hardware y software para desarrollar controladores y aplicaciones mediante Windows dispositivos portátiles.     |
| [Requisitos para Windows aplicaciones de DRM-Enabled multimedia](requirements-for-windows-media-drm-enabled-applications.md) | Propiedades necesarias para habilitar las transferencias Windows contenido protegido con DRM multimedia.                      |
| [Muestras](sample.md)                                                                                                  | Descripción de dos aplicaciones de escritorio de línea de comandos que se proporcionan con este kit de desarrollo de software. |
| [Introducción a la aplicación](application-overview.md)                                                                       | Conceptos clave que se usan Windows dispositivos portátiles.                                                             |
| [Guía de programación](programming-guide.md)                                                                             | Tareas clave que realizará una aplicación, con instrucciones paso a paso y fragmentos de código.              |
| [Referencia de programación](programming-reference.md)                                                                     | Guía de referencia de las interfaces y los tipos de datos definidos por Windows portables.                      |



 

Las aplicaciones creadas en Windows Media Administrador de dispositivos o Windows Image Acquisition pueden acceder a Windows dispositivos portátiles a través de una capa de compatibilidad.

Microsoft proporciona varios controladores para protocolos y dispositivos estándar, incluidos los dispositivos del Protocolo de transporte de medios (MTP) y los dispositivos Storage clase de almacenamiento masivo (MSC). Si está familiarizado con User-Mode Driver Framework, puede desarrollar sus propios controladores para dispositivos personalizados.

 

 



