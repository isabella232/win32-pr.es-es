---
description: Recupera la superficie compartida de DirectX que hace una copia de seguridad de una ventana determinada. Esta superficie se puede escribir en para actualizar el contenido de la ventana.
ms.assetid: 500CF5B4-0D56-4201-91F4-7333E45DACEE
title: Función DwmDxGetWindowSharedSurface
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
- DwmDxGetWindowSharedSurface
ms.openlocfilehash: 47f8c75ee55521c0f1da4151f5161cf44a63dc51aab5658edbca288cb8edce24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280135"
---
# <a name="dwmdxgetwindowsharedsurface-function"></a>Función DwmDxGetWindowSharedSurface

Recupera la superficie compartida de DirectX que hace una copia de seguridad de una ventana determinada. Esta superficie se puede escribir en para actualizar el contenido de la ventana.

## <a name="syntax"></a>Sintaxis

```C++
HRESULT WINAPI DwmDxGetWindowSharedSurface(
  _In_     HWND        hwnd,
  _In_     LUID        luidAdapter,
  _In_opt_ HMONITOR    hmonitorAssociation,
  _In_     DWORD       dwFlags,
  _Inout_  DXGI_FORMAT *pfmtWindow,
  _Out_    HANDLE      *phDxSurface,
  _Out_    UINT64      *puiUpdateId
);
```

## <a name="parameters"></a>Parámetros

`hwnd`

HWND [**que**](/windows/desktop/winprog/windows-data-types) especifica la ventana que se va a actualizar.

`luidAdapter`

EL [**LUID del**](/previous-versions/bb401655(v%3dmsdn.10)) adaptador donde se debe localizar la superficie.

`hmonitorAssociation`

Reservado.

`dwFlags`

Este parámetro puede ser uno de los siguientes valores o una combinación OR bit a bit de varios valores cuando corresponda.

| Valor | Significado |
|-|-|
| <span id="DWM_REDIRECTION_FLAG_WAIT"></span><span id="dwm_redirection_flag_wait"></span><dl> <dt>**DWM \_ MARCA DE \_ REDIRECCIÓN \_ WAIT**</dt> <dt>0</dt> </dl> | Hace que la función se bloquee hasta que haya pasado una sincronización vertical (VSync) desde la última vez que se llamó a la función correctamente. |
| <span id="DWM_REDIRECTION_FLAG_SUPPORT_PRESENT_TO_GDI_SURFACE"></span><span id="dwm_redirection_flag_support_present_to_gdi_surface"></span><dl> <dt>**DWM \_ COMPATIBILIDAD CON \_ LA \_ MARCA DE \_ REDIRECCIONAMIENTO PRESENTE EN LOS \_ \_ \_ DISPOSITIVOS SURFACE**</dt> <dt>0X10</dt> </dl> | Indica que la aplicación que realiza la llamada es capaz de presentarse en una superficie compartida de GDI. |

`pfmtWindow`

En la entrada, el formato deseado de la superficie. En la salida, el formato real de la superficie devuelta.

`phDxSurface`

En la salida, el identificador compartido a la superficie.

`puiUpdateId`

En la salida, el identificador de la actualización.

## <a name="return-value"></a>Valor devuelto

Esta función puede devolver uno de estos valores.

| Código devuelto | Descripción |
|-|-|
| **S \_ OK** | La llamada se ha producido correctamente y debe actualizar la superficie, con la seguridad de pasar el identificador de actualización a [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) (en el miembro **PresentHistoryToken** de la estructura RENDER de **D3DKMT \_** cuando se envía la actualización y, a continuación, se debe llamar a [**DwmDxUpdateWindowSharedSurface**](dwmdxupdatewindowsharedsurface.md) con el mismo identificador de actualización. Tenga en **cuenta que se debe llamar a DwmDxUpdateWindowSharedSurface** independientemente de si la superficie se actualizó realmente o no. |
| **SUPERFICIE DE REDIRECCIÓN \_ \_ DE GDI \_ DE \_ DWM** | La llamada se ha hecho correctamente y debe actualizar la superficie llamando a [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent)y estableciendo el modelo del miembro **PresentHistoryToken** en **D3DKMT \_ PM REDIRECTED \_ \_ BLT** y proporcionando el identificador de actualización en el **miembro Blt** de la unión.  Este valor solo se devuelve si *dwFlags* especificó COMPATIBILIDAD CON LA MARCA DE REDIRECCIÓN DE DWM PRESENT **TO \_ \_ \_ \_ \_ \_ GDI \_ SURFACE.** |
| **ADAPTADOR DE \_ DWM E \_ NO \_ \_ ENCONTRADO** | El valor *de luidAdapter* no es válido. |
| **DWM \_ E \_ COMPOSITIONDISABLED** | DWM no está habilitado actualmente y la aplicación tendrá que presentar otra manera. |

## <a name="remarks"></a>Comentarios

Esta API está pensada para implementar un controlador de gráficos o un entorno de ejecución. Es posible que una aplicación no llame a este método. Esta documentación solo es válida para Windows 7 y no se garantiza que esta API exista ni se comporte de forma similar en otras versiones de Windows. Esta función no está presente en ningún encabezado o biblioteca de vínculos estáticos y se encuentra en el ordinal 100 en dwmapi.dll.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Cliente mínimo compatible | Windows solo 7 \[ aplicaciones de escritorio\] |
| Servidor mínimo compatible | No se admite ninguno |
| Fin de compatibilidad de cliente | Windows 7 |
| Encabezado | N/D |
| Archivo DLL | Dwmapi.dll |
