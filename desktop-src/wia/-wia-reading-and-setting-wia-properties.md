---
description: La interfaz IWiaPropertyStorage proporciona métodos para leer y escribir las propiedades de un elemento de adquisición de imágenes de Windows (WIA). Las propiedades del elemento incluyen comandos del dispositivo, información de formato del elemento e información del dispositivo.
ms.assetid: 268d2298-bc9c-479b-b078-a8180cd38bc3
title: Leer y establecer propiedades de WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51df3e8fdb4b29abb6f64743ab8f7f2dd3776358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154388"
---
# <a name="reading-and-setting-wia-properties"></a>Leer y establecer propiedades de WIA

La interfaz [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) proporciona métodos para leer y escribir las propiedades de un elemento de adquisición de imágenes de Windows (WIA). Las propiedades del elemento incluyen comandos del dispositivo, información de formato del elemento e información del dispositivo.

Una aplicación puede obtener un puntero a una interfaz [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) de un elemento, ya sea enumerando la información del dispositivo o la información del evento del elemento llamando a [**IWiaItem:: EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) o [**IWiaItem:: EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) o consultando la interfaz [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) del elemento. (En WIA 2,0, haga esto llamando a [**IWiaItem2:: EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) o [**IWiaItem2:: EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) o consultando la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) del elemento).

[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) hereda de [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) y los métodos heredados se implementan como se describe en la sección de referencia de almacenamiento estructurado en el kit de desarrollo de software (SDK) de Windows.

> [!Note]
>
> Las aplicaciones WIA siempre deberían leer los encabezados de datos de imagen para obtener información precisa sobre la imagen. El controlador WIA puede modificar las propiedades de WIA y los encabezados de datos de imagen durante la transferencia de datos.
>
> Si no se proporciona ningún encabezado de datos de imagen con el formato especificado, la aplicación WIA debe usar las propiedades de WIA como origen de información sobre la transferencia de datos. La aplicación WIA debe volver a leer las propiedades de WIA necesarias después de que se complete el examen o la captura para obtener la configuración actualizada.

 

En las secciones siguientes se describen las distintas propiedades de WIA:

-   [Validación de propiedades de WIA](-wia-wia-property-validation.md)
-   [Propiedades de información del dispositivo](-wia-device-information-properties-wia-dip-xxxx.md)
-   [Propiedades de dispositivos](-wia-device-properties.md)
-   [Propiedades del elemento](-wia-item-properties.md)
-   [Propiedades de WIA adicionales](-wia-additional-wia-properties.md)
-   [Definir propiedades personalizadas](-wia-defining-custom-properties.md)
-   [Usar propiedades personalizadas](-wia-using-custom-properties.md)
-   [Esquema de análisis de perfil](-wia-scan-profile-schema.md)

 

 
