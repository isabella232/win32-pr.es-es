---
title: Atributo WM/MCDI
description: El atributo WM/MCDI es el identificador de CD de música del CD del que se copió el archivo o la pista.
ms.assetid: f0bec14d-416c-477f-98df-dece0bf85ea4
keywords:
- Atributo WM/MCDI Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 738ce8d5af7351b30fd986323db01d4dd335fa7307d2da88e48f4b2456eba1f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053861"
---
# <a name="wmmcdi-attribute"></a>Atributo WM/MCDI

El **atributo WM/MCDI** es el identificador de CD de música del CD del que se copió el archivo o la pista.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo se almacena tanto en la biblioteca (o caché) como en el archivo multimedia digital.

**TOC** es un alias para este atributo.

La Windows DEL SDK de formato multimedia para este atributo es g \_ wszWMMCDI.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





