---
title: elemento querySet
description: El elemento querySet contiene elementos que definen qué elementos multimedia se seleccionarán de la biblioteca.
ms.assetid: 18b5a509-a56b-4fd1-812f-60b8efd5136b
keywords:
- Elemento querySet Reproductor de Windows Media
topic_type:
- apiref
api_name:
- querySet Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4971c2a7f601132640d7654a95dd288f1740a467
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070949"
---
# <a name="queryset-element"></a>elemento querySet

El **elemento querySet** contiene elementos que definen qué elementos multimedia se seleccionarán de la biblioteca.

``` syntax
<querySet>
</querySet>
```

## <a name="attributes"></a>Atributos

Este elemento no tiene atributos.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos                                   |
|-----------|--------------------------------------------|
| Parent    | [smartPlaylist](smartplaylist-element.md) |
| Elemento secundario     | [sourceFilter](sourcefilter-element.md)   |



 

## <a name="remarks"></a>Observaciones

El **elemento querySet** especifica qué elementos multimedia se deben seleccionar de la biblioteca, sin tener en cuenta el tamaño del conjunto de resultados. Por **otro** lado, el elemento filter limita el tamaño del conjunto de resultados.

## <a name="examples"></a>Ejemplos


```
<querySet>
    <sourceFilter 
        type = "smartFilterObject" 
        id = "{4202947A-A563-4B05-A754-A1B4B5989849}"
        name = "Windows Media Local Music Library Filter">
            <fragment name = "Genre">
                <argument name = "Condition">Equals</argument>
                <argument name = "Value">Rock</argument>
            </fragment>
            <fragment name = "Artist">
                <argument name = "Condition">Does Not Equal</argument>
                <argument name = "Value">Brenda Diaz</argument>
            </fragment>
    </sourceFilter>
</querySet>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**elemento argument**](argument-element.md)
</dt> <dt>

[**elemento filter**](filter-element.md)
</dt> <dt>

[**elemento fragment**](fragment-element.md)
</dt> <dt>

[**elemento smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**elemento sourceFilter**](sourcefilter-element.md)
</dt> <dt>

[**Windows Referencia de elementos de lista de reproducción multimedia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





