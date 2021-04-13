---
title: StringCollection (objeto)
description: El objeto StringCollection proporciona una manera de manipular una colección de cadenas.
ms.assetid: bd4f82e7-1a6a-47c5-b019-7aff520e621a
keywords:
- Objeto StringCollection Media Player de Windows
topic_type:
- apiref
api_name:
- StringCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0d1872bec7e00e87ada845f7518608ea4149f137
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104358343"
---
# <a name="stringcollection-object"></a>StringCollection (objeto)

El objeto **StringCollection** proporciona una manera de manipular una colección de cadenas.

El objeto **StringCollection** admite la siguiente propiedad.



| Propiedad                            | Descripción                                             |
|-------------------------------------|---------------------------------------------------------|
| [count](stringcollection-count.md) | Recupera el número de elementos de la colección de cadenas. |



 

El objeto **StringCollection** admite los métodos siguientes.



| Método                                                                  | Descripción                                                                                                                     |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [getAttributeCountByType](stringcollection-getattributecountbytype.md) | Recupera el número de atributos asociados con el índice del elemento **StringCollection** , el nombre de atributo y el idioma especificados. |
| [getItemInfo](stringcollection-getiteminfo.md)                         | Recupera la cadena correspondiente al índice y el nombre del elemento **StringCollection** especificado.                                   |
| [getItemInfoByType](stringcollection-getiteminfobytype.md)             | Recupera la cadena correspondiente al índice del elemento **StringCollection** , el nombre, el idioma y el índice de atributo especificados.       |
| [isIdentical](stringcollection-isidentical.md)                         | Recupera un valor que indica si el objeto proporcionado es igual que el actual.                                        |
| [item](stringcollection-item.md)                                       | Recupera la cadena en el índice especificado.                                                                                    |



 

Se tiene acceso al objeto **StringCollection** mediante el método siguiente.



| Object                                        | Método                                                                           |
|-----------------------------------------------|----------------------------------------------------------------------------------|
| [MediaCollection](mediacollection-object.md) | [getAttributeStringCollection](mediacollection-getattributestringcollection.md) |



 

Para fines de Ilustración, *reproductor*. *mediaCollection*. **getAttributeStringCollection**(*Attribute*, *mediaType*) se usa en las secciones de sintaxis de referencia.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




