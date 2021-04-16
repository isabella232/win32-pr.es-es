---
description: Habilita o deshabilita la lectura previa en un origen de multimedia.
ms.assetid: b2b8711f-ba63-4fba-bb88-8d254135eb21
title: Propiedad MFPKEY_MediaSource_DisableReadAhead (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d06fe354431a24e15152268ba0ea6352e535c5e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649832"
---
# <a name="mfpkey_mediasource_disablereadahead-property"></a>\_Propiedad MFPKEY MediaSource \_ DisableReadAhead

Habilita o deshabilita la lectura previa en un origen de multimedia.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**VARIANTE \_ bool**

VT \_ bool

**boolVal**



## <a name="remarks"></a>Observaciones

Las aplicaciones pueden utilizar esta propiedad para configurar algunos orígenes de medios. Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen. Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).

Si el valor es **Variant \_ true**, el origen del medio no se leerá con anterioridad en el flujo de bytes. Esta configuración puede optimizar el rendimiento si tiene previsto leer una cantidad limitada de datos del origen de medios, por ejemplo, para obtener una imagen en miniatura de un archivo de vídeo.

Para la reproducción de audio/vídeo típica, esta propiedad debe establecerse en **variante \_ falsa**. El valor predeterminado es **Variant \_ false**.

No todos los orígenes multimedia admiten esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Remoto<br/> | Windows 7<br/>                                                               |
| Encabezado<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




