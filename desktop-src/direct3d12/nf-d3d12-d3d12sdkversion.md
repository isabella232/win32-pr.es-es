---
title: Símbolo D3D12SDKVersion
description: Número de versión del SDK de Direct3D 12.
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/25/2021
req.lib: ''
req.dll: d3d12core.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d12core.dll
api_name:
- D3D12SDKVersion
targetos: Windows
ms.openlocfilehash: f77786d0a057d8922923913984149c4b8ecd3bc8
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520041"
---
# <a name="d3d12sdkversion-symbol"></a>Símbolo D3D12SDKVersion

Número de versión del SDK de Direct3D 12.

## <a name="syntax"></a>Sintaxis

```cpp
extern "C" { _declspec(dllexport) extern const UINT D3D12SDKVersion = n;}
```

## <a name="return-value"></a>Valor devuelto

UINT [que](../winprog/windows-data-types.md) contiene el número de versión del SDK de Direct3D 12.

## <a name="remarks"></a>Comentarios

**D3D12SDKVersion** no está asociado a una biblioteca de importación ni a un archivo de encabezado.

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de destino** | Windows |
| **Header** | N/D |
| **Library** | N/D |
| **Archivo DLL** | d3d12core.dll |

## <a name="see-also"></a>Consulte también
