---
title: D3DPERF_SetMarker función)
description: Marque un evento instantáneo. PIX puede utilizar este evento para desencadenar una acción.
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
ms.openlocfilehash: 8eef59b9914ce30b95751641c16becf1963b19e0
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2020
ms.locfileid: "104420398"
---
# <a name="d3dperf_setmarker-function"></a>D3DPERF_SetMarker función)

Marque un evento instantáneo. PIX puede utilizar este evento para desencadenar una acción.

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

## <a name="remarks"></a>Observaciones

Los eventos de usuario instantáneos no se corcheten ni agrupan otros eventos. Por ejemplo, cuando el usuario activa un arma en un juego, una llamada **D3DPERF_SetMarker** podría crear un evento *Shot desencadenado* . Para agrupar varios eventos con un único nombre definido por el usuario, use **D3DPERF_BeginEvent** y **D3DPERF_EndEvent** en lugar de **D3DPERF_SetMarker**.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de destino** | Windows |
| **Header** | d3d9. h |
| **Library** | d3d9. lib |
| **DLL** | d3d9.dll |