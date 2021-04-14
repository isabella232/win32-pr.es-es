---
title: Dispositivos (guía para desarrolladores de Windows 7)
description: Los dispositivos son una parte fundamental de la experiencia del PC y Windows 7 permite nuevas posibilidades para los desarrolladores de aplicaciones que interactúan con los dispositivos.
ms.assetid: faed8ec8-2f12-4090-a003-b14b3d26e02a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cbfa699d129fd6d8343a0645fc6ed22aa9618ee
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421852"
---
# <a name="devices-windows-7-developer-guide"></a>Dispositivos (guía para desarrolladores de Windows 7)

Los dispositivos son una parte fundamental de la experiencia del PC y Windows 7 permite nuevas posibilidades para los desarrolladores de aplicaciones que interactúan con los dispositivos. La plataforma de experiencia del dispositivo permite la Asociación de aplicaciones y servicios con un dispositivo determinado, de modo que los usuarios puedan sacar el máximo partido de sus periféricos inmediatamente después de la conexión. La plataforma del sensor proporciona un conjunto de API para la detección y la comunicación con dispositivos de sensor que permitirán una nueva generación de aplicaciones que son conscientes de sus entornos. La plataforma de ubicación proporciona nuevas API para usar los datos de ubicación de un receptor de sistemas de posicionamiento global (GPS) u otros servicios que habilitan el comportamiento de la aplicación específica de la ubicación para los usuarios móviles. (Consulte [aspectos básicos de los dispositivos: información general](https://www.microsoft.com/whdc/device/default.mspx)).

## <a name="device-experience-platform"></a>Plataforma de experiencia del dispositivo

Windows 7 combina software y servicios para crear fantásticas experiencias nuevas para teléfonos móviles, reproductores multimedia portátiles, cámaras e impresoras. Windows 7 facilita el uso de estos dispositivos directamente desde el escritorio de Windows. También proporciona a los fabricantes de dispositivos una ubicación destacada en el escritorio de Windows, con oportunidades de personalización de marca y una interfaz sencilla para presentar la funcionalidad y los servicios que admite el dispositivo.

A través de la plataforma de experiencia del dispositivo, cada sesión de Windows se convierte en un portal para que los clientes obtengan más valor de sus dispositivos. La plataforma de experiencia del dispositivo permite a los usuarios conectarse con el fabricante del dispositivo, detectar y usar servicios relacionados y obtener información acerca de los accesorios. Dado que la experiencia del dispositivo está conectada a los servicios Web de Microsoft, las empresas de dispositivos pueden actualizar la experiencia incluso después de que los dispositivos se hayan enviado a los consumidores. La plataforma de experiencia del dispositivo puede generar una experiencia similar a la aplicación para dispositivos con el *logotipo* de Windows, como los teléfonos móviles.

La plataforma de experiencia del dispositivo proporciona a las aplicaciones acceso a dispositivos como teléfonos móviles y reproductores multimedia que implementan servicios a través del *Protocolo de transferencia multimedia (MTP)* o el modelo de controladores de [dispositivos portátiles de Windows](https://www.bing.com/search?q=Windows+Portable+Devices) .

Para habilitar la sincronización de información personal entre un equipo y un dispositivo, la plataforma de experiencia del dispositivo hospeda una nueva plataforma de sincronización para los dispositivos conectados y proporciona una interfaz de usuario para seleccionar las aplicaciones de destino para la sincronización de datos, como **contactos**, **calendario** y **tareas**. (Consulte [experiencia del dispositivo Windows](https://www.microsoft.com/whdc/device/DeviceExperience/default.mspx)).

## <a name="windows-biometric-framework"></a>Marco biométrico de Windows

El Plataforma de biometría de Windows (WBF) proporciona una API que permite a las aplicaciones usar dispositivos de huellas digitales para inscribir, identificar y comprobar las identidades de los usuarios sin tener acceso directo a los ejemplos o al hardware de huellas digitales biométricos. Puede usar WBF con dispositivos de huellas digitales que tengan controladores de la interfaz de dispositivo biométrico de Windows (WBDI). WBF es extensible a través de adaptadores de complementos que administran las comunicaciones del sensor, la coincidencia biométrica y el almacenamiento de plantillas. Esto garantiza que WBF puede usarse con una amplia gama de sensores de huellas digitales. En Windows 7, los lectores de huellas digitales pueden usar WBF para la autenticación durante el inicio de sesión de Windows y *UAC* . (Consulte [plataforma de biometría de Windows API](../secbiomet/biometric-service-api-portal.md)).

 

 
