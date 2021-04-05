---
title: D3DPERF_EndEvent función)
description: Marca el final de un evento definido por el usuario. PIX puede utilizar este evento para desencadenar una acción.
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
ms.openlocfilehash: 91c2a6a19b926cd9f5549fae084ce8973432b0f2
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2020
ms.locfileid: "104420399"
---
# <a name="d3dperf_endevent-function"></a>D3DPERF_EndEvent función)

Marca el final de un evento definido por el usuario. PIX puede utilizar este evento para desencadenar una acción.

## <a name="syntax"></a>Sintaxis

```cpp
int WINAPI D3DPERF_EndEvent(void);
```

## <a name="return-value"></a>Valor devuelto

Nivel de la jerarquía en la que el evento finaliza. Si se produce un error, este valor es negativo.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de destino** | Windows |
| **Header** | d3d9. h |
| **Library** | d3d9. lib |
| **DLL** | d3d9.dll |