---
title: D3DPERF_SetRegion función
description: Marque una serie de fotogramas con el color y el nombre especificados en el archivo DEEjeqRun. Actualmente, ESTA función no es compatible con LAV.
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
ms.openlocfilehash: 05884fe8a3b104588a941dcaf3089a1c0f6f8eab4f4a01e143470f73454ad4ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989272"
---
# <a name="d3dperf_setregion-function"></a>D3DPERF_SetRegion función

Marque una serie de fotogramas con el color y el nombre especificados en el archivo DEEjeqRun. Actualmente, ESTA función no es compatible con LAV.

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

## <a name="remarks"></a>Comentarios

Para facilitar el análisis, el programa de destino puede usar el color para marcar cada nivel de un programa de destino.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de destino** | Windows |
| **Header** | d3d9.h |
| **Library** | d3d9.lib |
| **Dll** | d3d9.dll |