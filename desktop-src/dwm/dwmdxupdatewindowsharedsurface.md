---
description: Notifica a DWM una actualización entrante de una superficie compartida de ventana.
ms.assetid: 8357D977-E501-47D7-85BC-7C8954C6D166
title: DwmDxUpdateWindowSharedSurface función)
ms.topic: reference
ms.date: 11/27/2018
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dwmapi.dll
api_name:
- DwmDxUpdateWindowSharedSurface
ms.openlocfilehash: 7649e96fb3a16458b518d0fc2c6dd09725a4b0ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544198"
---
# <a name="dwmdxupdatewindowsharedsurface-function"></a>DwmDxUpdateWindowSharedSurface función)

Notifica a DWM una actualización entrante de una superficie compartida de ventana.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT WINAPI DwmDxUpdateWindowSharedSurface(
  _In_     HWND     hwnd,
  _In_     UINT64   uiUpdateId,
  _In_     DWORD    dwFlags,
  _In_opt_ HMONITOR hmonitorAssociation,
  _In_     RECT     *prc
);
```

## <a name="parameters"></a>Parámetros

`hwnd`

[**HWnd**](/windows/desktop/winprog/windows-data-types) que especifica la ventana que se está actualizando.

`uiUpdateId`

IDENTIFICADOR de actualización recuperado de [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md).

`dwFlags`

Reservado.

`hmonitorAssociation`

Reservado.

`prc`

Rectángulo de la ventana que se está actualizando, en el espacio de coordenadas de la ventana. Un rectángulo nulo indica que no se ha actualizado ninguna región.

## <a name="return-value"></a>Valor devuelto

**S \_ Correcto si se** realiza correctamente, de lo contrario, un **HRESULT erróneo.**

## <a name="remarks"></a>Observaciones

Esta API está pensada para implementar un controlador de gráficos o un entorno de tiempo de ejecución. Una aplicación no puede llamar a este método. Esta documentación solo es válida para Windows 7 y no se garantiza que esta API exista ni se comporte de forma similar en otras versiones de Windows. Esta función no está presente en ningún encabezado ni en una biblioteca de vínculos estáticos, y se encuentra en el ordinal 101 en dwmapi.dll.

Solo se debe llamar a este método después de que [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md) devuelva **S \_ OK** y se debe llamar en ese escenario, independientemente de si la superficie está actualizada o no.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Cliente mínimo compatible | Solo aplicaciones de escritorio de Windows 7 \[\] |
| Servidor mínimo compatible | No se admite ninguno |
| Fin de compatibilidad de cliente | Windows 7 |
| Encabezado | N/D |
| Archivo DLL | Dwmapi.dll |
