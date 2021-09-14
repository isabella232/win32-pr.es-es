---
description: Acceso a las propiedades del objeto de servicio
ms.assetid: 66d9802b-ad28-47a4-8151-9df7aff07d61
title: Acceso a las propiedades del objeto de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 028ffc178f29f21aa60295b137b48c0fa2357a28
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266916"
---
# <a name="accessing-service-object-properties"></a>Acceso a las propiedades del objeto de servicio

Una aplicación puede leer y escribir propiedades para un único objeto en un servicio, para varios objetos identificados por identificadores de objeto o para varios objetos del mismo tipo. En [el tema Retrieving Object Properties (Recuperar](retrieving-content-object-properties.md) propiedades de objeto) se describen las propiedades de lectura de un único objeto en un servicio. En [el tema Writing Object Properties (Escribir](writing-content-object-properties.md) propiedades de objeto) se describen las propiedades de escritura de un único objeto en un servicio.

Consulte la sección [Tareas avanzadas para](advanced-tasks.md) obtener una descripción de la recuperación de propiedades para varios objetos.

## <a name="when-to-use-service-property-definitions"></a>Cuándo usar definiciones de propiedad de servicio

Las llamadas API de WPD usadas para recuperar y establecer propiedades de objeto para un servicio son las mismas que las llamadas para recuperar propiedades de objeto para un dispositivo (compare "Recuperación de propiedades para un único objeto" para ver un ejemplo). La diferencia clave es que se usa un conjunto diferente de PROPERTYKEYs para consultar las propiedades del objeto. Para WpdServiceApiSample, se usan propertykeys del servicio de dispositivo (como **PKEY \_ GenericObj \_ Name);** para WpdApiSample, se usan PROPERTYKEYs de WPD (por **ejemplo, WPD \_ OBJECT \_ NAME**).

Los PROPERTYKEY del servicio de dispositivo se definen en BridgeDeviceServices.h (incluido por cada archivo de encabezado de servicio) y representan el conjunto común de PROPERTYKEYS empleados por las aplicaciones de servicios de dispositivo y la implementación de firmware en el dispositivo. Esto permite un conjunto coherente de definiciones en toda la pila de dispositivos con traducción mínima, grupos PROPERTYKEYs basados en el servicio y permite que los nuevos servicios se definan más fácilmente sin tener que actualizar el esquema de WPD.

El conjunto de PROPERTYKEYs usado dependerá de las necesidades de la aplicación:

-   Si la aplicación se comunica con el dispositivo mediante una llamada a [**IPortableDevice::Open,**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)use las PROPIEDADES DEFINIDAs en PortableDevice.h. Un ejemplo de este tipo de aplicación es WpdApiSample.
-   Si la aplicación se comunica con los servicios de dispositivo mediante una llamada a [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open), use las PROPERTYKEYS definidas en BridgeDeviceServices.h. Un ejemplo de este tipo de aplicación es WpdServicesApiSample.
-   Si está escribiendo una aplicación compleja que necesita admitir un híbrido entre los servicios de dispositivo y el dispositivo (esto significa que la aplicación llama a **IPortableDevice::Open** e **IPortableDeviceService::Open),** deberá usar los PROPERTYKEY de WPD al usar IPortableDevice y sus interfaces derivadas, y el servicio de dispositivo PROPERTYKEYs al usar [IPortableDeviceService](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) y sus interfaces derivadas.

La mayoría de las aplicaciones WPD deben incluirse en la primera o segunda categoría.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[Recuperar propiedades de objeto](retrieving-content-object-properties.md)
</dt> <dt>

[Escribir propiedades de objeto](writing-content-object-properties.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



