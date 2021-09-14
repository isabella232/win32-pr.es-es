---
description: En este tema se describe lo que debe hacer para empezar a crear programas que usan sensor API.
ms.assetid: a8d3228a-5f8b-4850-9e47-5dfb2335e655
title: Requisitos generales para el desarrollo de aplicaciones (SENSOR API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ec328f659bb51eddf93cc69beb2fe6236113ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265223"
---
# <a name="general-requirements-for-application-development-sensor-api"></a>Requisitos generales para el desarrollo de aplicaciones (SENSOR API)

En este tema se describe lo que debe hacer para empezar a crear programas que usan sensor API.

Para crear una aplicación de Sensor API, debe instalar Windows 7 y el Kit de desarrollo de software (SDK) de Windows 7 en el equipo. En la tabla siguiente se describen los archivos específicos que necesitará.



| Nombre de archivo               | Descripción                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| Sensorsapi.h            | Archivo de encabezado principal para sensor API. Este archivo de encabezado contiene las definiciones de interfaz.               |
| Sensors.h               | Archivo de encabezado que contiene definiciones de constantes definidas por la plataforma.                                    |
| Initguid.h              | Archivo de encabezado que contiene definiciones para controlar la **inicialización de GUID.**                          |
| FunctionDiscoveryKeys.h | Archivo de encabezado que define las claves de propiedad de id. de dispositivo que son necesarias al conectarse a sensores lógicos. |
| Sensorsapi.lib          | Una biblioteca estática que contiene **definiciones de GUID** para sensor API.                                     |
| PortableDeviceGuids.lib | Biblioteca estática que contiene **definiciones de GUID** para Windows dispositivos portátiles.                   |



 

El programa puede requerir archivos adicionales.

## <a name="supported-operating-systems"></a>Sistemas operativos compatibles

Las aplicaciones de SENSOR API se ejecutarán en todas las ediciones de Windows 7, excepto Windows 7 Starter Edition.

## <a name="windows-portable-devices-interfaces"></a>Windows Interfaces de dispositivos portátiles

Sensor API usa determinados Windows portable Devices (WPD) para encapsular valores y claves de propiedad. En la tabla siguiente se describen las interfaces de estos objetos.



| Interfaz                                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))        | Esta interfaz proporciona una manera cómoda de crear un bolsa de propiedades de pares nombre-valor. Los nombres se representan **mediante PROPERTYKEY** y los valores se representan **mediante PROPVARIANT** s. <br/> La API usa esta interfaz para establecer y recuperar valores únicos y conjuntos de valores. Esta interfaz se puede recuperar de un método o, si se requiere un nuevo objeto, llamando a **CoCreateInstance** con CLSID \_ PortableDeviceValues.<br/> |
| [IPortableDeviceKeyCollection](/previous-versions//ms739549(v=vs.85)) | Esta interfaz contiene una colección de **PROPERTYKEY** s. Estas claves representan nombres de propiedad que **IPortableDeviceValues** puede almacenar. La API usa este objeto de colección para establecer y recuperar nombres de propiedad única y conjuntos de nombres de propiedad.<br/> Esta interfaz se puede recuperar de un método o, si se requiere un nuevo objeto, llamando a **CoCreateInstance** con CLSID \_ PortableDeviceKeyCollection. <br/>    |



 

 

