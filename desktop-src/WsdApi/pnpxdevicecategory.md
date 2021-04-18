---
description: Especifica la categoría PnP-X a la que pertenece el dispositivo. Se puede especificar más de una categoría.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: Elemento PnPXDeviceCategory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 731dd78fbe366fc9c7923686d3d9ac90b772c23d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697217"
---
# <a name="pnpxdevicecategory-element"></a>Elemento PnPXDeviceCategory

Especifica la categoría PnP-X a la que pertenece el dispositivo. Se puede especificar más de una categoría.

## <a name="usage"></a>Uso

``` syntax
<PnPXDeviceCategory/>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                   | Descripción                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**thisModelMetadata**](thismodelmetadata.md)<br/> | Define los metadatos del fabricante y del modelo para el dispositivo que se va a implementar.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Los dispositivos también pueden especificar una subcategoría de dispositivo para una categoría de dispositivo más descriptiva. Por ejemplo, "Phone. WindowsMobile cameras. DigitalStillCamera MediaDevices. MusicPlayer" identifica un dispositivo que es un dispositivo móvil de Microsoft Windows con una cámara y un reproductor de música. La categoría de dispositivo principal de este dispositivo sería "teléfonos".

Para especificar más de una categoría de dispositivo, separe las categorías con un espacio. Por ejemplo, "almacenamiento de impresoras" identifica un dispositivo con una categoría principal de "impresoras" y una categoría secundaria de "almacenamiento".

Si hay un elemento **PnPXDeviceCategory** , al menos un elemento [**hospedado**](hosted.md) debe contener los elementos [**PnPXHardwareId**](pnpxhardwareid.md) y [**PnPXCompatibleId**](pnpxcompatibleid.md) . Del mismo modo, si los elementos **PnPXHardwareId** y **PnPXCompatibleId** están presentes en un elemento **hospedado** , al menos un elemento **PnPXDeviceCategory** debe estar presente dentro del elemento [**thisModelMetadata**](thismodelmetadata.md) .

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




