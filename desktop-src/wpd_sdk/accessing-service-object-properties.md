---
description: Obtener acceso a las propiedades del objeto de servicio
ms.assetid: 66d9802b-ad28-47a4-8151-9df7aff07d61
title: Obtener acceso a las propiedades del objeto de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 028ffc178f29f21aa60295b137b48c0fa2357a28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696316"
---
# <a name="accessing-service-object-properties"></a>Obtener acceso a las propiedades del objeto de servicio

Una aplicación puede leer y escribir propiedades para un solo objeto en un servicio, para varios objetos identificados por identificadores de objeto o para varios objetos del mismo tipo. El tema [recuperar propiedades de objeto](retrieving-content-object-properties.md) describe cómo leer propiedades de un solo objeto en un servicio. El tema [Writing Object Properties](writing-content-object-properties.md) describe cómo escribir propiedades para un solo objeto en un servicio.

Consulte la sección [tareas avanzadas](advanced-tasks.md) para obtener una descripción de la recuperación de propiedades de varios objetos.

## <a name="when-to-use-service-property-definitions"></a>Cuándo usar las definiciones de propiedad de servicio

Las llamadas API de WPD usadas para recuperar y establecer las propiedades de los objetos de un servicio son las mismas que las llamadas para recuperar las propiedades de los objetos de un dispositivo (Comparar "recuperar propiedades de un solo objeto" para obtener un ejemplo). La diferencia clave es que se usa un conjunto diferente de PROPERTYKEYs para consultar las propiedades del objeto. En el caso de WpdServiceApiSample, se usan los PROPERTYKEYs de servicio del dispositivo (como el **\_ \_ nombre** de la GenericObj de PKEY); para WpdApiSample, se usan los propertykeys de la WPD (como **\_ \_ el nombre del objeto WPD**).

Los PROPERTYKEYs de servicio de dispositivo se definen en BridgeDeviceServices. h (incluido en cada archivo de encabezado de servicio) y representan el conjunto común de los PROPERTYKEYS utilizados por las aplicaciones de servicios de dispositivos y la implementación de firmware en el dispositivo. Esto permite un conjunto coherente de definiciones a lo largo de la pila de dispositivos con una traducción mínima, grupos de PROPERTYKEYs basados en el servicio y permite definir nuevos servicios más fácilmente sin tener que actualizar el esquema de WPD.

El conjunto de PROPERTYKEYs utilizado dependerá de las necesidades de la aplicación:

-   Si la aplicación se comunica con el dispositivo mediante una llamada a [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), use los PROPERTYKEYs definidos en PortableDevice. h. Un ejemplo de este tipo de aplicación es WpdApiSample.
-   Si la aplicación se comunica con los servicios de dispositivo mediante una llamada a [**IPortableDeviceService:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open), use los PROPERTYKEYS definidos en BridgeDeviceServices. h. Un ejemplo de este tipo de aplicación es WpdServicesApiSample.
-   Si está escribiendo una aplicación compleja que necesita admitir un híbrido de los servicios de dispositivo y el dispositivo (esto significa que la aplicación llama a **IPortableDevice:: Open** y **IPortableDeviceService:: Open**), deberá usar las propertykeys de la carga de usuario al usar IPortableDevice y sus interfaces derivadas y las propertykeys de servicio de dispositivo al usar [IPortableDeviceService](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) y sus interfaces derivadas.

La mayoría de las aplicaciones de WPD deben entrar en la primera o en la segunda categoría.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[Recuperación de propiedades de objeto](retrieving-content-object-properties.md)
</dt> <dt>

[Escribir propiedades de objeto](writing-content-object-properties.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



