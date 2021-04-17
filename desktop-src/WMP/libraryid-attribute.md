---
title: IdBiblioteca (atributo)
description: El atributo IdBiblioteca es el identificador de la biblioteca a la que pertenece el elemento.
ms.assetid: 680d9374-8729-4258-8672-b4b93b65e20a
keywords:
- IdBiblioteca Media Player de Windows de atributos
topic_type:
- apiref
api_name:
- LibraryID Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ae9e5ad097bc188b8de1e76a09448c57aa9b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699658"
---
# <a name="libraryid-attribute"></a>IdBiblioteca (atributo)

El atributo **IdBiblioteca** es el identificador de la biblioteca a la que pertenece el elemento.

## <a name="applies-to"></a>Se aplica a

-   [**Elementos de audio**](audio-item-attributes.md)
-   [**Elementos de fotografía**](photo-item-attributes.md)
-   [**Elementos de lista de reproducción**](playlist-attributes-ref.md)
-   [**Elementos de vídeo**](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Un elemento multimedia puede pertenecer a la biblioteca local del usuario actual o puede pertenecer a una biblioteca que otro usuario ha puesto a disposición en la red doméstica o en Internet.

El valor de este atributo es el mismo que el valor devuelto por el método [**IWMPLibrary2:: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------|
| Versión<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





