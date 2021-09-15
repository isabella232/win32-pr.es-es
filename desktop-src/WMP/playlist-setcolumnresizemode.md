---
title: PLAYLIST.setColumnResizeMode
description: El método setColumnResizeMode especifica el tamaño de las columnas indizadas.
ms.assetid: 84ca0e60-ca24-4058-ae08-5b9cf3d7c38f
keywords:
- Playlist.setColumnResizeMode Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359480"
---
# <a name="playlistsetcolumnresizemode"></a>PLAYLIST.setColumnResizeMode

El **método setColumnResizeMode** especifica el tamaño de las columnas indizadas.

``` syntax
        elementID.setColumnResizeMode(column, mode)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="column"></span><span id="COLUMN"></span>*Columna*
</dt> <dd>

**Number** (**long**) que indica el índice de la columna que se va a cambiar.

</dd> <dt>

<span id="mode"></span><span id="MODE"></span>*Modo*
</dt> <dd>

**Cadena** que indica el modo de ajuste de tamaño. Contiene uno de los valores siguientes.



| Value          | Descripción                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| AutosizeHeader | El tamaño de la columna cambia para dar cabida a todos los datos de la columna y del encabezado.                                  |
| AutosizeData   | El tamaño de la columna se ajusta solo a todos los datos de la columna.                                                 |
| Fijo          | La columna tiene un tamaño fijo.                                                                                    |
| Se extiende      | Cambia el tamaño de la columna para usar el espacio restante en el elemento **PLAYLIST** después de cambiar el tamaño de todas las demás columnas. |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





