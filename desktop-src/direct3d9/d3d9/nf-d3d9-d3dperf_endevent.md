---
title: D3DPERF_EndEvent función
description: Marca el final de un evento definido por el usuario. PIXEL puede usar este evento para desencadenar una acción.
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
- D3DPERF_EndEvent
targetos: Windows
ms.openlocfilehash: bd12780dfdfcb86e83495ae877d8debf1e768517826329ccee8d40ffaa88fbbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989255"
---
# <a name="d3dperf_endevent-function"></a>D3DPERF_EndEvent función

Marca el final de un evento definido por el usuario. PIXEL puede usar este evento para desencadenar una acción.

## <a name="syntax"></a>Sintaxis

```cpp
int WINAPI D3DPERF_EndEvent(void);
```

## <a name="return-value"></a>Valor devuelto

Nivel de la jerarquía en la que finaliza el evento. Si se produce un error, este valor es negativo.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de destino** | Windows |
| **Header** | d3d9.h |
| **Library** | d3d9.lib |
| **Dll** | d3d9.dll |