---
title: Atributo LibraryName
description: El atributo LibraryName es el nombre de la biblioteca a la que pertenece el elemento.
ms.assetid: 70ce2de1-6c7b-427a-ba48-a9f69bacd015
keywords:
- Atributo LibraryName Reproductor de Windows Media
topic_type:
- apiref
api_name:
- LibraryName
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d2b86a1b551fab103db732dd5405187c06395f37b1ae59c030c3a75a05f275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054793"
---
# <a name="libraryname-attribute"></a>Atributo LibraryName

El atributo LibraryName es el nombre de la biblioteca a la que pertenece el elemento.

## <a name="applies-to"></a>Se aplica a

-   [**Elementos de audio**](audio-item-attributes.md)
-   [**Elementos de fotos**](photo-item-attributes.md)
-   [**Elementos de lista de reproducción**](playlist-attributes-ref.md)
-   [**Elementos de vídeo**](video-item-attributes.md)

## <a name="remarks"></a>Comentarios

Un elemento multimedia puede pertenecer a la biblioteca local del usuario actual o puede pertenecer a una biblioteca que otro usuario haya puesto a disposición de otro usuario en una red doméstica.

El valor de este atributo es el mismo que el valor devuelto por el [**método IWMPLibrary::get \_**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name) name.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versión<br/> | Reproductor de Windows Media 12<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





