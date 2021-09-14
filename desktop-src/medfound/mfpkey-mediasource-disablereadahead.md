---
description: Habilita o deshabilita la lectura adelantada en un origen multimedia.
ms.assetid: b2b8711f-ba63-4fba-bb88-8d254135eb21
title: MFPKEY_MediaSource_DisableReadAhead propiedad (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d06fe354431a24e15152268ba0ea6352e535c5e7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268911"
---
# <a name="mfpkey_mediasource_disablereadahead-property"></a>Propiedad MFPKEY \_ MediaSource \_ DisableReadAhead

Habilita o deshabilita la lectura adelantada en un origen multimedia.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**VARIANT \_ BOOL**

VT \_ BOOL

**boolVal**



## <a name="remarks"></a>Observaciones

Las aplicaciones pueden usar esta propiedad para configurar algunos orígenes multimedia. Para establecer la propiedad , pase un **puntero IPropertyStore** al solucionador de origen. Para obtener más información, vea [Configuring a Media Source](configuring-a-media-source.md).

Si el valor es **VARIANT \_ TRUE**, el origen del medio no se leerá con antelación en la secuencia de bytes. Esta configuración puede optimizar el rendimiento si planea leer una cantidad limitada de datos del origen multimedia, por ejemplo, para obtener una imagen en miniatura de un archivo de vídeo.

Para la reproducción típica de audio y vídeo, esta propiedad debe establecerse en **VARIANT \_ FALSE.** El valor predeterminado es **VARIANT \_ FALSE.**

No todos los orígenes de medios admiten esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Remoto<br/> | Windows 7<br/>                                                               |
| Encabezado<br/> | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




