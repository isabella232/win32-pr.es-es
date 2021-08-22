---
title: Atributo WM/MediaClassPrimaryID
description: El atributo WM/MediaClassPrimaryID es un GUID que especifica una de las clases multimedia principales music, non-music audio, video u otro.
ms.assetid: eb78f4a9-7c18-4cad-bb34-fd1ff15bad4f
keywords:
- Atributo WM/MediaClassPrimaryID Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aebc52488ebcabfca843a8fdfdfbb51307cd96be4fe923386c718bab8752c61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506465"
---
# <a name="wmmediaclassprimaryid-attribute"></a>Atributo WM/MediaClassPrimaryID

El **atributo WM/MediaClassPrimaryID** es un GUID que especifica una de las clases multimedia principales: música, audio que no es música, vídeo u otro.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [Otros elementos](other-item-attributes.md)
-   [Elementos de fotos](photo-item-attributes.md)
-   [Listas](playlist-attributes-ref.md)
-   [Elementos de radio](radio-item-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo se almacena tanto en la biblioteca como en el archivo multimedia digital.

**MediaClassPrimaryID** es un alias para este atributo.

La Windows SDK de formato multimedia para este atributo es g \_ wszWMMediaClassPrimaryID.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior (el elemento de foto solo se admite en Reproductor de Windows Media 10 o posterior)<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





