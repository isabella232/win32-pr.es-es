---
title: D3DPERF_BeginEvent función)
description: Marca el principio de un evento definido por el usuario. PIX puede utilizar este evento para desencadenar una acción.
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
- D3DPERF_BeginEvent
targetos: Windows
ms.openlocfilehash: f6732d4ce969cbd26cdb32f4750654c7baacd324
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2020
ms.locfileid: "104420397"
---
# <a name="d3dperf_beginevent-function"></a>D3DPERF_BeginEvent función)

Marca el principio de un evento definido por el usuario. PIX puede utilizar este evento para desencadenar una acción.

## <a name="syntax"></a>Sintaxis

```cpp
int WINAPI D3DPERF_BeginEvent(
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

Nivel de base cero de la jerarquía en la que se inicia este evento. Si se produce un error, el valor devuelto será negativo.

## <a name="remarks"></a>Observaciones

Los eventos definidos por el usuario agrupan otros eventos de una manera significativa para el programa de destino, de modo que puedan representarse mejor en las herramientas de generación de perfiles de rendimiento. Por ejemplo, un evento de *espacio de dibujo* podría corchete varias llamadas de Direct3D que controlan el espacio de un juego. Los eventos se pueden anidar.

Cada llamada **D3DPERF_BeginEvent** debe tener una llamada **D3DPERF_EndEvent** coincidente. Los eventos instantáneos (que no corcheten otros eventos) deben etiquetarse mediante **D3DPERF_SetMarker** en lugar de **D3DPERF_BeginEvent** y **D3DPERF_EndEvent**.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de destino** | Windows |
| **Header** | d3d9. h |
| **Library** | d3d9. lib |
| **DLL** | d3d9.dll |