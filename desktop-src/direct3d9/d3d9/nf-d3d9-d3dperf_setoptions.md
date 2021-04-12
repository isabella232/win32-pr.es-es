---
title: D3DPERF_SetOptions función)
description: Establezca las opciones del generador de perfiles especificadas por el programa de destino.
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
ms.openlocfilehash: 8bd877469864ccdaa833ce80d00eb06ae5fc18de
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2020
ms.locfileid: "104487330"
---
# <a name="d3dperf_setoptions-function"></a>D3DPERF_SetOptions función)

Establezca las opciones del generador de perfiles especificadas por el programa de destino.

## <a name="syntax"></a>Sintaxis

```cpp
int WINAPI D3DPERF_SetOptions(
  DWORD dwOptions
);
```

## <a name="parameters"></a>Parámetros

`dwOptions`

Opciones de usuario reconocibles por PIX. Establézcalo en 1 para notificar a PIX que el programa de destino no concede permiso para el que se va a crear el archivo.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve un valor.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de destino** | Windows |
| **Header** | d3d9. h |
| **Library** | d3d9. lib |
| **DLL** | d3d9.dll |