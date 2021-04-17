---
title: Lista de reproducción. itemMedia
description: El atributo itemMedia recupera el objeto multimedia correspondiente al índice especificado en el elemento de lista de reproducción.
ms.assetid: 38085798-7986-432f-8c88-de886bfc2ac5
keywords:
- Windows Media Player de lista de reproducción. itemMedia
topic_type:
- apiref
api_name:
- PLAYLIST.itemMedia
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 269e9011ade69ee61d99c29c1fa5bd1b9fa3deeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660543"
---
# <a name="playlistitemmedia"></a>Lista de reproducción. itemMedia

El atributo **itemMedia** recupera el objeto **multimedia** correspondiente al índice especificado en el elemento de **lista de reproducción** .

``` syntax
        elementID.itemMedia(index)
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un objeto **multimedia** de solo lectura.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*ajustar*
</dt> <dd>

**Número**(**largo**) que contiene el índice de un elemento de lista de reproducción.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La propiedad **itemMedia** devolverá los objetos multimedia que se expanden en el elemento de **lista de reproducción** . Por ejemplo, si hay una lista de reproducción que contiene tres clips multimedia que no se expanden en el elemento de **lista de reproducción** , **itemMedia**(0) devolverá la lista de reproducción como el objeto multimedia. Si se expande la lista de reproducción, **itemMedia**(0) devolverá el primer clip multimedia en la lista de reproducción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





