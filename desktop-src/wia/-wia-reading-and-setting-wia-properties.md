---
description: La interfaz IWiaPropertyStorage proporciona métodos para leer y escribir Windows propiedades de un elemento de adquisición de imágenes (WIA). Las propiedades del elemento incluyen comandos de dispositivo, información de formato de elemento e información del dispositivo.
ms.assetid: 268d2298-bc9c-479b-b078-a8180cd38bc3
title: Leer y establecer propiedades de WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607e319723023a00c4159687c3dff13fedab8275a0522fdb2254b36b8e62edb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439879"
---
# <a name="reading-and-setting-wia-properties"></a>Leer y establecer propiedades de WIA

La [**interfaz IWiaPropertyStorage proporciona**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) métodos para leer y escribir Windows propiedades de un elemento de adquisición de imágenes (WIA). Las propiedades del elemento incluyen comandos de dispositivo, información de formato de elemento e información del dispositivo.

Una aplicación puede obtener un puntero a una interfaz [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) de un elemento enumerando la información del dispositivo del elemento o la información de eventos llamando a [**IWiaItem::EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) o [**IWiaItem::EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) o consultando la [**interfaz IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) del elemento. (En WIA 2.0, para ello, llame a [**IWiaItem2::EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) o [**IWiaItem2::EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) o consulte la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) del elemento).

[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) hereda de [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) y los métodos heredados se implementan como se describe en la sección de referencia de Structured Storage en el Kit de desarrollo de software (SDK) de Windows.

> [!Note]
>
> Las aplicaciones WIA siempre deben leer encabezados de datos de imagen para obtener información precisa de la imagen. El controlador WIA puede modificar las propiedades de WIA y los encabezados de datos de imagen durante la transferencia de datos.
>
> Si no hay ningún encabezado de datos de imagen proporcionado con el formato especificado, la aplicación WIA debe usar las propiedades de WIA como origen de información sobre la transferencia de datos. La aplicación WIA debe volver a leer las propiedades de WIA necesarias una vez completado el examen o la captura para obtener la configuración actualizada.

 

En las secciones siguientes se describen las distintas propiedades de WIA:

-   [Validación de propiedades de WIA](-wia-wia-property-validation.md)
-   [Propiedades de la información del dispositivo](-wia-device-information-properties-wia-dip-xxxx.md)
-   [Propiedades de dispositivos](-wia-device-properties.md)
-   [Propiedades del elemento](-wia-item-properties.md)
-   [Propiedades adicionales de WIA](-wia-additional-wia-properties.md)
-   [Definir propiedades personalizadas](-wia-defining-custom-properties.md)
-   [Uso de propiedades personalizadas](-wia-using-custom-properties.md)
-   [Esquema de perfil de examen](-wia-scan-profile-schema.md)

 

 
