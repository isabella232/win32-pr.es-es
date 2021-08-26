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
ms.openlocfilehash: 0bf0aa17e16a4274b69e80580c0615ed055dd97a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917959"
---
# <a name="d3d12sdkversion-symbol"></a>Símbolo D3D12SDKVersion

Número de versión del SDK de Direct3D 12.

## <a name="syntax"></a>Sintaxis

```cpp
extern "C" { _declspec(dllexport) extern const UINT D3D12SDKVersion = n;}
```

## <a name="return-value"></a>Valor devuelto

UINT [que](/windows/win32/winprog/windows-data-types) contiene el número de versión del SDK de Direct3D 12.

## <a name="remarks"></a>Comentarios

**D3D12SDKVersion** no está asociado a una biblioteca de importación ni a un archivo de encabezado.

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de destino** | Windows |
| **Header** | N/A |
| **Library** | N/A |
| **DLL** | d3d12core.dll |

## <a name="see-also"></a>Consulte también
