---
description: En este tema se describe lo que debe hacer para empezar a crear programas que usan la API de sensor.
ms.assetid: a8d3228a-5f8b-4850-9e47-5dfb2335e655
title: Requisitos generales para el desarrollo de aplicaciones (API de sensor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ec328f659bb51eddf93cc69beb2fe6236113ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361128"
---
# <a name="general-requirements-for-application-development-sensor-api"></a>Requisitos generales para el desarrollo de aplicaciones (API de sensor)

En este tema se describe lo que debe hacer para empezar a crear programas que usan la API de sensor.

Para crear una aplicación de API de sensor, debe instalar Windows 7 y el kit de desarrollo de software (SDK) de Windows 7 en el equipo. En la tabla siguiente se describen los archivos específicos que necesitará.



| Nombre de archivo               | Descripción                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| Sensorsapi. h            | El archivo de encabezado principal de la API del sensor. Este archivo de encabezado contiene las definiciones de interfaz.               |
| Sensors. h               | El archivo de encabezado que contiene las definiciones de las constantes definidas por la plataforma.                                    |
| Initguid. h              | El archivo de encabezado que contiene definiciones para controlar la inicialización de **GUID** .                          |
| FunctionDiscoveryKeys. h | El archivo de encabezado que define las claves de propiedad de identificador de dispositivo que son necesarias cuando se conecta a sensores lógicos. |
| Sensorsapi. lib          | Biblioteca estática que contiene definiciones **GUID** para la API del sensor.                                     |
| PortableDeviceGuids. lib | Biblioteca estática que contiene definiciones **GUID** para objetos de dispositivos portátiles de Windows.                   |



 

El programa puede requerir archivos adicionales.

## <a name="supported-operating-systems"></a>Sistemas operativos compatibles

Las aplicaciones de API de sensor se ejecutarán en todas las ediciones de Windows 7, excepto para Windows 7 Starter Edition.

## <a name="windows-portable-devices-interfaces"></a>Interfaces de dispositivos portátiles de Windows

La API de sensor usa ciertos objetos de dispositivos portátiles de Windows (WPD) para encapsular valores y claves de propiedad. En la tabla siguiente se describen las interfaces de estos objetos.



| Interfaz                                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))        | Esta interfaz proporciona una forma cómoda de crear un contenedor de propiedades de pares nombre-valor. Los nombres se representan mediante **PROPERTYKEY** s y los valores se representan mediante **PROPVARIANT** s. <br/> La API usa esta interfaz para establecer y recuperar valores únicos y conjuntos de valores. Esta interfaz se puede recuperar de un método o, si se requiere un nuevo objeto, llamando a **CoCreateInstance** con CLSID \_ PortableDeviceValues.<br/> |
| [IPortableDeviceKeyCollection](/previous-versions//ms739549(v=vs.85)) | Esta interfaz contiene una colección de **PROPERTYKEY** s. Estas claves representan nombres de propiedad que pueden almacenarse mediante **IPortableDeviceValues**. La API usa este objeto de colección para establecer y recuperar los nombres de propiedad única y los conjuntos de nombres de propiedad.<br/> Esta interfaz se puede recuperar de un método o, si se requiere un nuevo objeto, llamando a **CoCreateInstance** con CLSID \_ PortableDeviceKeyCollection. <br/>    |



 

 

