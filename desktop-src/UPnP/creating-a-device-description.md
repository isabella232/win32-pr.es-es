---
title: Creación de una descripción del dispositivo
description: Una descripción de dispositivo basado en UPnP es un documento XML que describe las propiedades de un dispositivo y la jerarquía de dispositivos anidados dentro de él.
ms.assetid: b2a7d342-958c-439d-8b17-b4fdc5fbad12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52df95de15481c7004704b6f67cd9478083ac88
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994100"
---
# <a name="creating-a-device-description"></a>Creación de una descripción del dispositivo

Una [*Descripción de dispositivo*](d-gly.md) basado en UPnP es un documento XML que describe las propiedades de un dispositivo y la jerarquía de dispositivos anidados dentro de él. El esquema para las descripciones de dispositivos basados en UPnP, conocido como el lenguaje de plantillas UPnP (UTL) para dispositivos, se define en la arquitectura del dispositivo UPnP. Las descripciones de dispositivos contienen vínculos a [*descripciones de servicios*](s-gly.md). El esquema para las descripciones de servicio y el UTL para los servicios también se definen en la especificación "arquitectura de dispositivo UPnP".

> [!Note]  
> Puede haber problemas al usar la descripción del servicio de www.upnp.org.

 

El desarrollador de un dispositivo debe proporcionar descripciones de dispositivos y servicios para el dispositivo.

Los elementos de una descripción del dispositivo que debe proporcionar el desarrollador de un dispositivo hospedado son los mismos que los definidos en la especificación de "arquitectura de dispositivo UPnP", con las siguientes excepciones:

-   Los elementos **controlURL** y **eventSubURL** son obligatorios y deben estar vacíos. El host del dispositivo rellena los valores de estos campos cuando se publica y anuncia el dispositivo.
-   El elemento **UDN** debe contener un identificador que sea único en el documento de Descripción del dispositivo (es decir, no es necesario que sea globalmente único). Este identificador se usa para buscar el UDN generado por el host del dispositivo.
-   Los elementos **SCPDURL** no deben contener las direcciones URL a las descripciones del servicio. En su lugar, deben contener el nombre del archivo de descripción de servicio. El archivo de descripción de servicio debe estar ubicado en el [*Directorio de recursos*](r-gly.md). La ubicación de este directorio se debe proporcionar al host del dispositivo durante el proceso de registro, como el uso de un programa de instalación. Esta ruta de acceso y todas ellas debajo son rutas de acceso relativas, en función de la ruta de acceso registrada.
-   El elemento **URL** del elemento **Icon** no debe contener las direcciones URL a los iconos de dispositivo. En su lugar, deben contener el nombre del archivo de icono. Si está presente, el archivo de icono debe estar ubicado en el directorio de recursos. Esta ruta de acceso y todas ellas debajo son rutas de acceso relativas, en función de la ruta de acceso registrada.
-   El elemento **URLBase** no debe estar presente.

> [!Note]  
> Todas las direcciones URL generadas por el host del dispositivo son direcciones URL relativas. Las direcciones URL son relativas a la ubicación del documento de Descripción del dispositivo, que se envía en el anuncio de dispositivo inicial.

 

> [!IMPORTANT]
> No agregue comentarios al documento de Descripción del dispositivo, ya que puede provocar errores de registro cuando el host del dispositivo de Plug and Play universal intenta analizar el documento.

 

## <a name="string-length-limitations"></a>Limitaciones de longitud de cadena

Las siguientes longitudes de cadena se utilizan en la API de host del dispositivo con tecnología UPnP:

-   **DeviceType** – 64 bytes
-   **friendlyName** : 64 bytes
-   **fabricante** : 64 bytes
-   **modelDescription** : 128 bytes
-   **modelName** : 32 bytes
-   **modelNumber** : 32 bytes
-   **SerialNumber** : 64 bytes
-   **UPC** : 12 bytes
-   **serviceType** : 64 bytes
-   **serviceId** : 64 bytes

 

 




