---
description: Especifica la categoría PnP-X a la que pertenece el dispositivo. Se puede especificar más de una categoría.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: PnPXDeviceCategory, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42a34a3f63333a2d33266991c0e028e7d42a7244c962617974c9cc15e290d03c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897365"
---
# <a name="pnpxdevicecategory-element"></a>PnPXDeviceCategory, elemento

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



## <a name="remarks"></a>Comentarios

Los dispositivos también pueden especificar una subcategoría de dispositivo para una categoría de dispositivo más descriptiva. Por ejemplo, "Phones.WindowsMobile Cameras.DigitalStcamera MediaDevices.MusicPlayer" identifica un dispositivo que es un dispositivo móvil de Microsoft Windows con una cámara y un reproductor de música. La categoría de dispositivo principal para este dispositivo sería "Teléfonos".

Para especificar más de una categoría de dispositivo, separe las categorías con un espacio. Por ejemplo, "Impresoras Storage" identifica un dispositivo con una categoría principal de "Impresoras" y una categoría secundaria de "Storage".

Si hay **un elemento PnPXDeviceCategory** presente, al menos un elemento hospedado debe contener los elementos [**PnPXHardwareId**](pnpxhardwareid.md) y [**PnPXCompatibleId.**](pnpxcompatibleid.md) [](hosted.md) Del mismo modo, si los elementos **PnPXHardwareId** y  **PnPXCompatibleId** están presentes en un elemento hospedado, debe haber al menos un elemento **PnPXDeviceCategory** dentro del elemento [**thisModelMetadata.**](thismodelmetadata.md)

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




