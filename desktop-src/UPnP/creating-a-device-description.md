---
title: Crear una descripción del dispositivo
description: Una descripción del dispositivo basada en UPnP es un documento XML que describe las propiedades de un dispositivo y la jerarquía de dispositivos anidados que contiene.
ms.assetid: b2a7d342-958c-439d-8b17-b4fdc5fbad12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7949bf275416f8d4754028f0cd0fe9ac70e3a18c381107cba94569a0b1ec4dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008105"
---
# <a name="creating-a-device-description"></a>Crear una descripción del dispositivo

Una descripción del dispositivo [](d-gly.md) basada en UPnP es un documento XML que describe las propiedades de un dispositivo y la jerarquía de dispositivos anidados que contiene. El esquema de las descripciones de dispositivos basadas en UPnP, conocido como lenguaje de plantilla UPnP (UTL) para dispositivos, se define en la arquitectura del dispositivo UPnP. Las descripciones de dispositivos contienen [*vínculos a descripciones de servicio.*](s-gly.md) El esquema para las descripciones de servicio y el UTL para servicios también se definen en la especificación "Arquitectura de dispositivos UPnP".

> [!Note]  
> Puede haber problemas al usar la descripción del servicio de www.upnp.org.

 

El desarrollador de un dispositivo debe proporcionar descripciones de dispositivos y servicios para el dispositivo.

Los elementos de una descripción de dispositivo que el desarrollador de un dispositivo hospedado debe proporcionar son los mismos que los definidos en la especificación "Arquitectura de dispositivo UPnP", con las siguientes excepciones:

-   Los **elementos controlURL** **y eventSubURL** son necesarios y deben estar vacíos. El host de dispositivo rellena los valores de estos campos cuando el dispositivo se publica y se anuncia.
-   El **elemento UDN** debe contener un identificador que sea único para el documento de descripción del dispositivo (es decir, no debe ser único globalmente). Este identificador se usa para buscar el UDN generado por el host del dispositivo.
-   Los **elementos SCPDURL** no deben contener direcciones URL para las descripciones del servicio. En su lugar, deben contener el nombre del archivo de descripción del servicio. El archivo de descripción del servicio debe encontrarse en el [*directorio de recursos*](r-gly.md). La ubicación de este directorio debe proporcionarse al host del dispositivo durante el proceso de registro, como el uso de un programa de instalación. Esta ruta de acceso y todas las siguientes son rutas de acceso relativas, basadas en la ruta de acceso registrada.
-   El **elemento url** dentro del elemento **icon** no debe contener direcciones URL para los iconos de dispositivo. En su lugar, deben contener el nombre del archivo de icono. Si está presente, el archivo de icono debe encontrarse en el directorio de recursos. Esta ruta de acceso y todas las siguientes son rutas de acceso relativas, basadas en la ruta de acceso registrada.
-   El **elemento URLBase** no debe estar presente.

> [!Note]  
> Todas las direcciones URL generadas por el host del dispositivo son direcciones URL relativas. Las direcciones URL son relativas a la ubicación del documento de descripción del dispositivo, que se envía en el anuncio inicial del dispositivo.

 

> [!IMPORTANT]
> No agregue comentarios al documento de descripción del dispositivo, ya que puede provocar errores de registro cuando el host de dispositivo de Plug and Play universal intenta analizar el documento.

 

## <a name="string-length-limitations"></a>Limitaciones de longitud de cadena

Las siguientes longitudes de cadena se usan en device host API con tecnología UPnP:

-   **deviceType:** 64 bytes
-   **friendlyName:** 64 bytes
-   **fabricante:** 64 bytes
-   **modelDescription:** 128 bytes
-   **modelName:** 32 bytes
-   **modelNumber:** 32 bytes
-   **serialNumber:** 64 bytes
-   **UPC:** 12 bytes
-   **serviceType:** 64 bytes
-   **serviceId:** 64 bytes

 

 




