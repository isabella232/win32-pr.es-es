---
title: COLUMNA. columnID
description: El atributo columnID especifica o recupera un identificador de columna en el control de lista de reproducción.
ms.assetid: c7b51f0b-e347-46be-a26d-aaa0bce83e0c
keywords:
- COLUMNA. columnID Windows Media Player
topic_type:
- apiref
api_name:
- COLUMN.columnID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4bc9aa6485443ae17486616b030b903a911a8e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699945"
---
# <a name="columncolumnid"></a>COLUMNA. columnID

El atributo **columnID** especifica o recupera un identificador de columna en el control de **lista de reproducción** .

``` syntax
        elementID.columnID
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura.

## <a name="remarks"></a>Observaciones

Los valores de **columnID** son los mismos que los que se usan con el método **getItemInfo** en un objeto **multimedia** . Se puede obtener una lista mediante el uso de los *medios*. la propiedad **attributeCount** para determinar el número de atributos disponibles para un objeto **multimedia** determinado. Los números de índice se pueden usar con los *medios*. método **getAttributeName** para determinar los nombres de los atributos, que a su vez se pueden pasar a los *elementos multimedia*. **getItemInfo**. La propiedad **columnID** solo se puede establecer en estos valores, con la excepción de algunos valores que no pueden ser devueltos por los *medios*. **getAttributeName**. Estos valores se muestran a continuación.



| Value     | Descripción                                                                        |
|-----------|------------------------------------------------------------------------------------|
| name      | Muestra el nombre del objeto **multimedia** .                                         |
| duration  | Muestra la duración del objeto **multimedia** .                                     |
| sourceURL | Muestra la dirección URL del objeto **multimedia** .                                          |
| status    | Muestra el estado de copia de archivos.                                              |
| tamaño      | Muestra el tamaño del archivo que representa el objeto **multimedia** .                |
| extensión | Muestra la extensión de nombre de archivo del archivo que representa el objeto **multimedia** . |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COLUMN, elemento**](column-element.md)
</dt> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Media. attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media. getAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> </dl>

 

 





