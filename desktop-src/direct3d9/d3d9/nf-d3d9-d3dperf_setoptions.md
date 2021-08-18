---
title: D3DPERF_SetOptions función
description: Establezca las opciones del profiler especificadas por el programa de destino.
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
- D3DPERF_SetOptions
targetos: Windows
ms.openlocfilehash: 579c07d8f93696e4e3c83b1e61c1ff5fca65e12b5a7cf0a5937a254ecc6dc306
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805740"
---
# <a name="d3dperf_setoptions-function"></a>D3DPERF_SetOptions función

Establezca las opciones del profiler especificadas por el programa de destino.

## <a name="syntax"></a>Sintaxis

```cpp
int WINAPI D3DPERF_SetOptions(
  DWORD dwOptions
);
```

## <a name="parameters"></a>Parámetros

`dwOptions`

Opciones de usuario reconocibles porNB. Establezca esta opción en 1 para notificar a LALE que el programa de destino no concede permiso para el perfil.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve un valor.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de destino** | Windows |
| **Header** | d3d9.h |
| **Library** | d3d9.lib |
| **Dll** | d3d9.dll |