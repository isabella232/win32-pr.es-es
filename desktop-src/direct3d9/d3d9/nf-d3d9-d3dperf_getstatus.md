---
title: D3DPERF_GetStatus función)
description: Determine el estado actual del generador de perfiles desde el programa de destino.
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
- D3DPERF_GetStatus
targetos: Windows
ms.openlocfilehash: 626d56dd449b0a0aa92e85c82dabda119900680d
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2020
ms.locfileid: "104358750"
---
# <a name="d3dperf_getstatus-function"></a>D3DPERF_GetStatus función)

Determine el estado actual del generador de perfiles desde el programa de destino.

## <a name="syntax"></a>Sintaxis

```cpp
DWORD WINAPI D3DPERF_GetStatus( void );
```

## <a name="return-value"></a>Valor devuelto

Un valor distinto de cero cuando PIX está generando perfiles del programa de destino; de lo contrario, es cero.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de destino** | Windows |
| **Header** | d3d9. h |
| **Library** | d3d9. lib |
| **DLL** | d3d9.dll |