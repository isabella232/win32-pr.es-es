---
title: D3DPERF_SetRegion función)
description: Marque una serie de fotogramas con el color y el nombre especificados en el archivo PIXRun. Esta función no es compatible actualmente con PIX.
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
- D3DPERF_SetRegion
targetos: Windows
ms.openlocfilehash: 650cc6063865da5ce30b97ed1468c1718ace5da6
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2020
ms.locfileid: "105720137"
---
# <a name="d3dperf_setregion-function"></a>D3DPERF_SetRegion función)

Marque una serie de fotogramas con el color y el nombre especificados en el archivo PIXRun. Esta función no es compatible actualmente con PIX.

## <a name="syntax"></a>Sintaxis

```cpp
void WINAPI D3DPERF_SetRegion(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a>Parámetros

`col`

Color del evento. Este es el color para mostrar el evento en la vista de eventos.

`wszName`

Nombre del evento.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve un valor.

## <a name="remarks"></a>Observaciones

Para facilitar el análisis, el programa de destino puede usar el color para marcar cada nivel de un programa de destino.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de destino** | Windows |
| **Header** | d3d9. h |
| **Library** | d3d9. lib |
| **DLL** | d3d9.dll |