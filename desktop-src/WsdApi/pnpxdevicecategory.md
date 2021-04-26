---
description: Especifica la categoría PnP-X a la que pertenece el dispositivo. Se puede especificar más de una categoría.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: PnPXDeviceCategory, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08084d780c26d2f7fab902156939fd14a3e60c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996592"
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

Los dispositivos también pueden especificar una subcategoría de dispositivo para una categoría de dispositivo más descriptiva. Por ejemplo, "Phones.WindowsMobile Cameras.DigitalStcamera MediaDevices.MusicPlayer" identifica un dispositivo que es un dispositivo de Microsoft Windows Mobile con una cámara y un reproductor de música. La categoría de dispositivo principal para este dispositivo sería "Teléfonos".

Para especificar más de una categoría de dispositivo, separe las categorías con un espacio. Por ejemplo, "Almacenamiento de impresoras" identifica un dispositivo con una categoría principal de "Impresoras" y una categoría secundaria de "Almacenamiento".

Si hay **un elemento PnPXDeviceCategory** presente, al menos un elemento hospedado debe contener los elementos [**PnPXHardwareId**](pnpxhardwareid.md) y [**PnPXCompatibleId.**](pnpxcompatibleid.md) [](hosted.md) Del mismo modo, si los elementos **PnPXHardwareId** y  **PnPXCompatibleId** están presentes en un elemento hospedado, debe haber al menos un elemento **PnPXDeviceCategory** dentro del elemento [**thisModelMetadata.**](thismodelmetadata.md)

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




