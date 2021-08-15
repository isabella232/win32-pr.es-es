---
title: Dispositivos (Windows 7 Developer Guide)
description: Los dispositivos son una parte fundamental de la experiencia del equipo y Windows 7 permite nuevas posibilidades para los desarrolladores de aplicaciones que interactúan con dispositivos.
ms.assetid: faed8ec8-2f12-4090-a003-b14b3d26e02a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775389f1a3548e2e94b8b2c25f9b46560cef5fc61a5e486f5dff28871da9f9e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086738"
---
# <a name="devices-windows-7-developer-guide"></a>Dispositivos (Windows 7 Developer Guide)

Los dispositivos son una parte fundamental de la experiencia del equipo y Windows 7 permite nuevas posibilidades para los desarrolladores de aplicaciones que interactúan con dispositivos. Device Experience Platform permite la asociación de aplicaciones y servicios con un dispositivo determinado, para que los usuarios puedan obtener el máximo beneficio de sus periféricos inmediatamente después de la conexión. La plataforma sensor proporciona un conjunto de API para la detección y la comunicación con dispositivos sensores que permitirán una nueva generación de aplicaciones que son conscientes de sus entornos. La plataforma de ubicación proporciona nuevas API para usar datos de ubicación de un receptor de sistemas de posicionamiento global (GPS) u otros servicios que permiten el comportamiento de la aplicación específica de la ubicación para los usuarios móviles. (Consulte [Aspectos básicos del dispositivo- Información general).](https://www.microsoft.com/whdc/device/default.mspx)

## <a name="device-experience-platform"></a>Plataforma de experiencia del dispositivo

Windows 7 combina software y servicios para crear nuevas experiencias interesantes para teléfonos móviles, reproductores multimedia portátiles, cámaras e impresoras. Windows 7 facilita el uso de estos dispositivos directamente desde Windows escritorio. También proporciona a los creadores de dispositivos una ubicación destacada en el escritorio de Windows, con oportunidades de personalidad de marca y una interfaz sencilla para presentar la funcionalidad y los servicios que admite el dispositivo.

A través de la Plataforma de experiencia del dispositivo, cada Windows sesión se convierte en un portal para que los clientes obtengan más valor de sus dispositivos. Device Experience Platform permite a los usuarios conectarse con el fabricante del dispositivo, detectar y usar servicios relacionados y obtener información sobre los accesorios. Dado que la experiencia del dispositivo está conectada a los servicios web de Microsoft, las empresas de dispositivos pueden actualizar la experiencia incluso después de que los dispositivos se hayan enviado a los consumidores. La plataforma de experiencia del dispositivo puede generar una experiencia de aplicación para Windows *dispositivos logotipos,* como teléfonos móviles.

La plataforma de experiencia del dispositivo proporciona a las aplicaciones acceso [a](https://www.bing.com/search?q=Windows+Portable+Devices) dispositivos como teléfonos móviles y reproductores multimedia que implementan servicios a través del Protocolo de transferencia de medios *(MTP)* o el modelo de controlador Windows dispositivos portátiles.

Para habilitar la sincronización de información personal entre un equipo y un dispositivo, la Plataforma de experiencia del dispositivo hospeda una nueva plataforma de sincronización para dispositivos conectados y proporciona una interfaz de usuario para seleccionar aplicaciones de destino para la sincronización de datos como **Contactos,** Calendario y **Tareas.** (Consulte [Windows experiencia del dispositivo).](https://www.microsoft.com/whdc/device/DeviceExperience/default.mspx)

## <a name="windows-biometric-framework"></a>Marco biométrico de Windows

El marco biométrico de Windows (WBF) proporciona una API que permite a las aplicaciones usar dispositivos con huella digital para inscribir, identificar y comprobar las identidades de usuario sin obtener acceso directo a ningún hardware biométrico con huellas digitales o muestras. Puede usar WBF con dispositivos con huellas digitales que tengan Windows de interfaz de dispositivo biométrica (WBDI). WBF es extensible a través de adaptadores de complemento que administran las comunicaciones del sensor, la coincidencia biométrica y el almacenamiento de plantillas. Esto garantiza que WBF se puede usar con una amplia gama de sensores de huella digital. En Windows 7, los lectores de huellas digitales pueden usar WBF para la autenticación durante *UAC* y Windows inicio de sesión. (Consulte [Windows API de Marco biométrico).](../secbiomet/biometric-service-api-portal.md)

 

 
