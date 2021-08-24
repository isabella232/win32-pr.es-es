---
title: D3DPERF_QueryRepeatFrame función
description: Determine si un profiler de rendimiento solicita que el marco actual se vuelva a enviar a Direct3D para el análisis de rendimiento. Esta función no es compatible actualmente con PIXEL.
ms.localizationpriority: low
ms.topic: reference
ms.date: 04/06/2020
req.lib: d3d9.lib
req.dll: d3d9.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d9.dll
api_name:
- D3DPERF_QueryRepeatFrame
targetos: Windows
ms.openlocfilehash: dbc46ff05b6fa1846bb0e1ffc1fca928ca1d68ee38a43708c77a109b61a405da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751245"
---
# <a name="d3dperf_queryrepeatframe-function"></a>D3DPERF_QueryRepeatFrame función

Determine si un profiler de rendimiento solicita que el marco actual se vuelva a enviar a Direct3D para el análisis de rendimiento. Esta función no es compatible actualmente con PIXEL.

## <a name="syntax"></a>Sintaxis

```cpp
BOOL WINAPI D3DPERF_QueryRepeatFrame( void );
```

## <a name="return-value"></a>Valor devuelto

Si el valor devuelto es TRUE, el autor de la llamada debe repetir la misma secuencia de llamadas. Si es FALSE, el autor de la llamada debe continuar.

## <a name="remarks"></a>Comentarios

Se debe llamar a la función inmediatamente después de llamar a **IDirect3DDevice9::P resent.**

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de destino** | Windows |
| **Header** | d3d9.h |
| **Library** | d3d9.lib |
| **Dll** | d3d9.dll |