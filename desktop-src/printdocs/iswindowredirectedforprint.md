---
description: La función IsWindowRedirectedForPrint determina si la ventana especificada se redirige actualmente para la impresión.
ms.assetid: 49FD0D63-0F7F-48C6-81B6-25715294E7B7
title: Función IsWindowRedirectedForPrint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsWindowRedirectedForPrint
api_type:
- DllExport
api_location:
- user32.dll
ms.openlocfilehash: b6648e5638ec6f05a2677ce279b0c3d7b160b49b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568633"
---
# <a name="iswindowredirectedforprint-function"></a>Función IsWindowRedirectedForPrint

La **función IsWindowRedirectedForPrint** determina si la ventana especificada se redirige actualmente para la impresión.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI IsWindowRedirectedForPrint(
  _In_   HWND hWnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hWnd* \[ En\]
</dt> <dd>

Controlador de la ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la ventana se redirige actualmente para la impresión, la función devuelve un valor distinto de cero; de lo contrario, devuelve cero.

## <a name="remarks"></a>Observaciones

Se redirige una ventana para imprimir cuando procesa una llamada a [**PrintWindow.**](/windows/desktop/api/Winuser/nf-winuser-printwindow) En una llamada a **PrintWindow**, una ventana representa su contenido en un contexto de dispositivo fuera de la pantalla.

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress.**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>User32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**WM \_ PRINT**](/windows/desktop/gdi/wm-print)
</dt> <dt>

[**WM \_ PRINTCLIENT**](/windows/desktop/gdi/wm-printclient)
</dt> </dl>

 

