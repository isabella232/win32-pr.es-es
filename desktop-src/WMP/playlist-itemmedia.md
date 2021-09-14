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
ms.openlocfilehash: 269e9011ade69ee61d99c29c1fa5bd1b9fa3deeb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243165"
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

## <a name="remarks"></a>Observaciones

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

 

 





