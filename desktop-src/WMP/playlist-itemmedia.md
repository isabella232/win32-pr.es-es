---
title: PLAYLIST.itemMedia
description: El atributo itemMedia recupera el objeto Media correspondiente al índice especificado en el elemento PLAYLIST.
ms.assetid: 38085798-7986-432f-8c88-de886bfc2ac5
keywords:
- PLAYLIST.itemMedia Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.itemMedia
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52b3061ef83ec246878d51528e88a12b4f10dcb3085f584a2266dc64a163b866
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746880"
---
# <a name="playlistitemmedia"></a>PLAYLIST.itemMedia

El **atributo itemMedia** recupera el objeto **Media** correspondiente al índice especificado en el elemento **PLAYLIST.**

``` syntax
        elementID.itemMedia(index)
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un objeto **Multimedia de solo** lectura.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Índice*
</dt> <dd>

**Number**(**long**) que contiene el índice de un elemento de lista de reproducción.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **propiedad itemMedia** devolverá objetos multimedia que se expanden en el elemento **PLAYLIST.** Por ejemplo, si hay una lista de reproducción que contiene tres clips multimedia que no se expanden en el elemento **PLAYLIST,** **itemMedia**(0) devolverá la lista de reproducción como el objeto multimedia. Si la lista de reproducción está expandida, **itemMedia**(0) devolverá el primer clip multimedia de la lista de reproducción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**ELEMENTO PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





