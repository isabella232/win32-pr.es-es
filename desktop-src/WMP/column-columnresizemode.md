---
title: COLUMN. columnResizeMode
description: El atributo columnResizeMode especifica o recupera el modo de cambiar el tamaño de esta columna.
ms.assetid: 95ece2a3-20a6-4b9d-a2eb-fc69fc612f29
keywords:
- COLUMN. columnResizeMode Windows Media Player
topic_type:
- apiref
api_name:
- COLUMN.columnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52d17b1a2edd878fb15e69c595e3c061c1963a5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699669"
---
# <a name="columncolumnresizemode"></a>COLUMN. columnResizeMode

El atributo **columnResizeMode** especifica o recupera el modo de cambiar el tamaño de esta columna.

``` syntax
        elementID.columnResizeMode
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene uno de los valores siguientes.



| Value          | Descripción                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| AutosizeHeader | Predeterminada. La columna cambia de tamaño para dar cabida a todos los datos de la columna y del encabezado.                         |
| AutosizeData   | La columna cambia de tamaño para alojar solo todos los datos de la columna.                                                 |
| Fijo          | La columna tiene un tamaño fijo.                                                                                    |
| Se expande      | La columna cambia de tamaño para usar el espacio restante en el control de la **lista de reproducción** después de cambiar el tamaño de todas las demás columnas. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COLUMN, elemento**](column-element.md)
</dt> </dl>

 

 





