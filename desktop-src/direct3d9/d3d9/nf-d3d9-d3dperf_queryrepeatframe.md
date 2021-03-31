---
title: D3DPERF_QueryRepeatFrame función)
description: Determine si un generador de perfiles de rendimiento solicita que el marco actual se vuelva a enviar a Direct3D para el análisis de rendimiento. Esta función no es compatible actualmente con PIX.
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
ms.openlocfilehash: c4054a0704fd0258483ee0d3d3d555cb5eabe7f9
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2020
ms.locfileid: "103789046"
---
# <a name="d3dperf_queryrepeatframe-function"></a>D3DPERF_QueryRepeatFrame función)

Determine si un generador de perfiles de rendimiento solicita que el marco actual se vuelva a enviar a Direct3D para el análisis de rendimiento. Esta función no es compatible actualmente con PIX.

## <a name="syntax"></a>Sintaxis

```cpp
BOOL WINAPI D3DPERF_QueryRepeatFrame( void );
```

## <a name="return-value"></a>Valor devuelto

Si el valor devuelto es TRUE, el llamador debe repetir la misma secuencia de llamadas. Si es FALSE, el llamador debe continuar.

## <a name="remarks"></a>Observaciones

Se debe llamar a la función inmediatamente después de que se llame a **IDirect3DDevice9::P reenviar** .

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de destino** | Windows |
| **Header** | d3d9. h |
| **Library** | d3d9. lib |
| **DLL** | d3d9.dll |