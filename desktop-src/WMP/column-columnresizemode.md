---
title: COLUMN.columnResizeMode
description: El atributo columnResizeMode especifica o recupera el modo de cambio de tamaño de esta columna.
ms.assetid: 95ece2a3-20a6-4b9d-a2eb-fc69fc612f29
keywords:
- COLUMN.columnResizeMode Reproductor de Windows Media
topic_type:
- apiref
api_name:
- COLUMN.columnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c59046aa76c01a1439e5db8f0fb6850e7df74d874cba555d1f9c3829f09d9598
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764005"
---
# <a name="columncolumnresizemode"></a>COLUMN.columnResizeMode

El **atributo columnResizeMode** especifica o recupera el modo de cambio de tamaño de esta columna.

``` syntax
        elementID.columnResizeMode
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura que contiene uno de los valores siguientes.



| Valor          | Descripción                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| AutosizeHeader | Predeterminada. El tamaño de la columna cambia de tamaño para dar cabida a todos los datos de la columna y del encabezado.                         |
| AutosizeData   | El tamaño de la columna cambia de tamaño para dar cabida solo a todos los datos de la columna.                                                 |
| Fijo          | La columna tiene un tamaño fijo.                                                                                    |
| Se extiende      | La columna cambia de tamaño para usar el espacio restante en el control **PLAYLIST** después de cambiar el tamaño de todas las demás columnas. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO COLUMN**](column-element.md)
</dt> </dl>

 

 





