---
title: Lista de reproducción. setColumnResizeMode
description: El método setColumnResizeMode especifica cómo se ajusta el tamaño de las columnas indizadas.
ms.assetid: 84ca0e60-ca24-4058-ae08-5b9cf3d7c38f
keywords:
- Windows Media Player de lista de reproducción. setColumnResizeMode
topic_type:
- apiref
api_name:
- PLAYLIST.setColumnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a1b83020f4400f4f1095c84e281fe498f2b67da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709266"
---
# <a name="playlistsetcolumnresizemode"></a>Lista de reproducción. setColumnResizeMode

El método **setColumnResizeMode** especifica cómo se ajusta el tamaño de las columnas indizadas.

``` syntax
        elementID.setColumnResizeMode(column, mode)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="column"></span><span id="COLUMN"></span>*artículo*
</dt> <dd>

**Número** (**largo**) que indica el índice de la columna que se va a cambiar.

</dd> <dt>

<span id="mode"></span><span id="MODE"></span>*modo*
</dt> <dd>

**Cadena** que indica el modo de ajuste de tamaño. Contiene uno de los valores siguientes.



| Value          | Descripción                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| AutosizeHeader | La columna cambia de tamaño para dar cabida a todos los datos de la columna y del encabezado.                                  |
| AutosizeData   | La columna cambia de tamaño para alojar solo todos los datos de la columna.                                                 |
| Fijo          | La columna tiene un tamaño fijo.                                                                                    |
| Se expande      | La columna cambia de tamaño para usar el espacio restante en el elemento de **lista de reproducción** después de cambiar el tamaño de todas las demás columnas. |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





