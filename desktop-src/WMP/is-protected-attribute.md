---
title: Is_Protected atributo)
description: El \_ atributo is protected indica si el contenido está protegido mediante administración de derechos digitales (DRM).
ms.assetid: 049d4116-7ba6-49f5-ad54-82a98b79d6bc
keywords:
- Is_Protected Media Player de atributos de Windows
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba626e72e139a5373973edea581f0f8462eee32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691088"
---
# <a name="is_protected-attribute"></a>\_Atributo protegido

El atributo **is \_ Protected** indica si el contenido está protegido mediante administración de derechos digitales (DRM).

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Archivos de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en la biblioteca y en el archivo multimedia digital.

**DigitallySecure** es un alias para este atributo.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMProtected.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





