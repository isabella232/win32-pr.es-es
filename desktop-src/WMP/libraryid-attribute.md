---
title: Atributo LibraryID
description: El atributo LibraryID es el identificador de la biblioteca a la que pertenece el elemento.
ms.assetid: 680d9374-8729-4258-8672-b4b93b65e20a
keywords:
- Atributo LibraryID Reproductor de Windows Media
topic_type:
- apiref
api_name:
- LibraryID Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ae9e5ad097bc188b8de1e76a09448c57aa9b83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360558"
---
# <a name="libraryid-attribute"></a>Atributo LibraryID

El **atributo LibraryID** es el identificador de la biblioteca a la que pertenece el elemento.

## <a name="applies-to"></a>Se aplica a

-   [**Elementos de audio**](audio-item-attributes.md)
-   [**Elementos de fotos**](photo-item-attributes.md)
-   [**Elementos de lista de reproducción**](playlist-attributes-ref.md)
-   [**Elementos de vídeo**](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Un elemento multimedia puede pertenecer a la biblioteca local del usuario actual o pertenecer a una biblioteca que otro usuario haya puesto a disposición de otro usuario en la red principal o en Internet.

El valor de este atributo es el mismo que el valor devuelto por el [**método IWMPLibrary2::getItemInfo.**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------|
| Versión<br/> | Reproductor de Windows Media 12<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





