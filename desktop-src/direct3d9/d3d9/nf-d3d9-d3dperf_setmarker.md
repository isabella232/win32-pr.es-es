---
title: D3DPERF_SetMarker función
description: Marque un evento instantáneo. PIXEL puede usar este evento para desencadenar una acción.
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
- D3DPERF_SetMarker
targetos: Windows
ms.openlocfilehash: ecd51374a127ab60872d6e6440abef03bde1bf3e5ec53cdc14c41e58640d6f6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096917"
---
# <a name="d3dperf_setmarker-function"></a>D3DPERF_SetMarker función

Marque un evento instantáneo. PIXEL puede usar este evento para desencadenar una acción.

## <a name="syntax"></a>Sintaxis

```cpp
void WINAPI D3DPERF_SetMarker(
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

Los eventos de usuario instantáneos no se entre corchetes ni agrupan otros eventos. Por ejemplo, cuando el usuario desencadena un incendio en un juego, una llamada a un evento *Shot Fired* **podría crearse mediante una D3DPERF_SetMarker** acción. Para agrupar varios eventos con un único nombre definido por el usuario, **use** D3DPERF_BeginEvent y **D3DPERF_EndEvent** en lugar **de D3DPERF_SetMarker**.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de destino** | Windows |
| **Header** | d3d9.h |
| **Library** | d3d9.lib |
| **Dll** | d3d9.dll |