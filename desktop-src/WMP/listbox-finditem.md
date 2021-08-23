---
title: LISTBOX.findItem
description: El método findItem busca una cadena determinada a partir del elemento que sigue al índice de elemento especificado.
ms.assetid: 8d112d99-1866-45e5-b0ef-5d4a3c8b388d
keywords:
- ListBOX.findItem Reproductor de Windows Media
topic_type:
- apiref
api_name:
- LISTBOX.findItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3625c8d8e9993d09e7b5b41911ead8df857c257a7a2354d71c8d81c1fecc645
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135328"
---
# <a name="listboxfinditem"></a>LISTBOX.findItem

El **método findItem** busca una cadena determinada a partir del elemento que sigue al índice de elemento especificado.

``` syntax
        elementID.findItem(startIndex, searchString)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*Startindex*
</dt> <dd>

**Number** (**long**) que contiene el índice del elemento en el que se va a iniciar la búsqueda.

</dd> <dt>

<span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*
</dt> <dd>

**Cadena** que contiene el texto que se buscará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor Number** (**long**) que contiene el índice del elemento que contiene la cadena.

## <a name="remarks"></a>Comentarios

Para iniciar la búsqueda en la primera línea del control de cuadro de lista, use 1 como *startIndex*. Para seguir buscando texto después de encontrar la primera línea, use el índice de línea devuelto como *startIndex* y la búsqueda se iniciará en la línea siguiente. Este método buscará subcadenas y no distingue mayúsculas de minúsculas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media para Windows XP o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> </dl>

 

 





