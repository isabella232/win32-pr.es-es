---
description: Notifica al DWM una actualización entrante en una superficie compartida de ventana.
ms.assetid: 8357D977-E501-47D7-85BC-7C8954C6D166
title: Función DwmDxUpdateWindowSharedSurface
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
ms.openlocfilehash: 9eac390cd6ccf79ed3f916f4c9605b938ab9fd338df3643301d7f5e5c900c0d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280125"
---
# <a name="dwmdxupdatewindowsharedsurface-function"></a>Función DwmDxUpdateWindowSharedSurface

Notifica al DWM una actualización entrante en una superficie compartida de ventana.

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

HWND [**que**](/windows/desktop/winprog/windows-data-types) especifica la ventana que se va a actualizar.

`uiUpdateId`

Identificador de actualización recuperado de [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md).

`dwFlags`

Reservado.

`hmonitorAssociation`

Reservado.

`prc`

El rect de la ventana que se está actualizando, en el espacio de coordenadas de la ventana. Un rectángulo NULL indica que no se ha actualizado ninguna región.

## <a name="return-value"></a>Valor devuelto

**S \_ Correcto si** se realiza correctamente; en caso contrario, error **HRESULT.**

## <a name="remarks"></a>Comentarios

Esta API está pensada para implementar un controlador de gráficos o un entorno de ejecución. Es posible que una aplicación no llame a este método. Esta documentación solo es válida para Windows 7 y no se garantiza que esta API exista ni se comporte de forma similar en otras versiones de Windows. Esta función no está presente en ningún encabezado o biblioteca de vínculos estáticos, y se encuentra en el ordinal 101 en dwmapi.dll.

Solo se debe llamar a este método después de que [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md) devuelva **S \_ OK** y se debe llamar a en ese escenario, independientemente de si la superficie está actualizada o no.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Cliente mínimo compatible | Windows 7 aplicaciones \[ de escritorio\] |
| Servidor mínimo compatible | No se admite ninguno |
| Fin de compatibilidad de cliente | Windows 7 |
| Encabezado | N/D |
| Archivo DLL | Dwmapi.dll |
