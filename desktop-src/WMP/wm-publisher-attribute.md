---
title: Atributo WM/Publisher
description: El atributo WM/Publisher es el nombre de la empresa que publicó el contenido.
ms.assetid: 5f3aa5de-237e-449c-918e-8750481adc6f
keywords:
- Atributo WM/Publisher Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/Publisher
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22aa04eecb3999b3029948739eef51dab094d0ebf9b65ba01ccdcf6de59efc18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053793"
---
# <a name="wmpublisher-attribute"></a>Atributo WM/Publisher

El **atributo WM/Publisher** es el nombre de la empresa que publicó el contenido.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Listas de reproducción de CD](cd-playlist-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [DVDs](dvd-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo se almacena tanto en la biblioteca (o caché) como en el archivo multimedia digital.

**Label**, **ReleasedBy** y **Studio son** alias para este atributo.

La constante Windows SDK de formato multimedia para este atributo es g \_ wszWMPublisher.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





