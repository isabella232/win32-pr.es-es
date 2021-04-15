---
description: Recupera la superficie compartida de DirectX que respalda una ventana determinada. Esta superficie se puede escribir en para actualizar el contenido de la ventana.
ms.assetid: 500CF5B4-0D56-4201-91F4-7333E45DACEE
title: DwmDxGetWindowSharedSurface función)
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
ms.openlocfilehash: 15e7829383ce23e5bc06bb61ab9c0c224ab18182
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715647"
---
# <a name="dwmdxgetwindowsharedsurface-function"></a>DwmDxGetWindowSharedSurface función)

Recupera la superficie compartida de DirectX que respalda una ventana determinada. Esta superficie se puede escribir en para actualizar el contenido de la ventana.

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

[**HWnd**](/windows/desktop/winprog/windows-data-types) que especifica la ventana que se va a actualizar.

`luidAdapter`

[**LUID**](/previous-versions/bb401655(v%3dmsdn.10)) del adaptador donde se debe ubicar la superficie.

`hmonitorAssociation`

Reservado.

`dwFlags`

Este parámetro puede ser uno de los valores siguientes, o una combinación OR bit a bit de varios valores cuando sea necesario.

| Value | Significado |
|-|-|
| <span id="DWM_REDIRECTION_FLAG_WAIT"></span><span id="dwm_redirection_flag_wait"></span><dl> <dt>**DWM \_ \_ \_ Espera de la marca de redireccionamiento**</dt> <dt>0</dt> </dl> | Hace que la función se bloquee hasta que haya transcurrido una sincronización vertical (VSync) desde la última vez que se llamó a la función correctamente. |
| <span id="DWM_REDIRECTION_FLAG_SUPPORT_PRESENT_TO_GDI_SURFACE"></span><span id="dwm_redirection_flag_support_present_to_gdi_surface"></span><dl> <dt>**DWM \_ \_Compatibilidad con la marca de REdireccionamiento \_ \_ presente \_ en la \_ \_ superficie de GDI**</dt> <dt>0x10</dt> </dl> | Indica que la aplicación que realiza la llamada es capaz de presentar en una superficie compartida de GDI. |

`pfmtWindow`

En la entrada, el formato deseado de la superficie. En la salida, el formato real de la superficie devuelta.

`phDxSurface`

En la salida, el identificador compartido de la superficie.

`puiUpdateId`

En la salida, identificador de la actualización.

## <a name="return-value"></a>Valor devuelto

Esta función puede devolver uno de estos valores.

| Código devuelto | Descripción |
|-|-|
| **S \_ correcto** | La llamada se realizó correctamente y debe actualizar la superficie, asegurándose de pasar el identificador de la actualización a [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) (en el miembro **PresentHistoryToken** de la estructura de **\_ representación D3DKMT** cuando se envía la actualización y, a continuación, se debe llamar a [**DwmDxUpdateWindowSharedSurface**](dwmdxupdatewindowsharedsurface.md) con el mismo identificador de actualización. Tenga en cuenta que se debe llamar a **DwmDxUpdateWindowSharedSurface** independientemente de si la superficie se actualizó realmente o no. |
| **\_superficie de \_ \_ redirección GDI \_ de DWM S** | La llamada se realizó correctamente y debe actualizar la superficie llamando a [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent)y estableciendo el **modelo** de miembro de **PresentHistoryToken** en **D3DKMT \_ PM \_ Redirigido \_ BLT** y proporcionando el identificador de actualización en el miembro **BLT** de la Unión. Este valor solo se devuelve si **la \_ \_ compatibilidad con la marca de redirección \_ de DWM presente en la \_ \_ \_ \_ superficie de GDI** se especificó en *dwFlags*. |
| **\_ \_ \_ no \_ se encontró el adaptador de DWM E** | El valor de *luidAdapter* no es válido. |
| **COMPOSITIONDISABLED de DWM \_ \_** | DWM no está habilitado actualmente y la aplicación tendrá que presentar otra manera. |

## <a name="remarks"></a>Observaciones

Esta API está pensada para implementar un controlador de gráficos o un entorno de tiempo de ejecución. Una aplicación no puede llamar a este método. Esta documentación solo es válida para Windows 7 y no se garantiza que esta API exista ni se comporte de forma similar en otras versiones de Windows. Esta función no está presente en ningún encabezado ni en una biblioteca de vínculos estáticos, y se encuentra en el ordinal 100 en dwmapi.dll.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Cliente mínimo compatible | Solo aplicaciones de escritorio de Windows 7 \[\] |
| Servidor mínimo compatible | No se admite ninguno |
| Fin de compatibilidad de cliente | Windows 7 |
| Encabezado | N/D |
| Archivo DLL | Dwmapi.dll |
