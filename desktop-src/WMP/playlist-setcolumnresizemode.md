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
ms.openlocfilehash: 72f356108ff016c404468a9b152b4adac247cd72ee089a9e82ea3206c4c2ffea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335807"
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
| AutosizeData   | El tamaño de la columna cambia para alojar solo todos los datos de la columna.                                                 |
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

 

 





