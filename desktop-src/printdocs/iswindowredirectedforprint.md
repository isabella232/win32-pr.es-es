---
description: La función IsWindowRedirectedForPrint determina si la ventana especificada se redirige actualmente para imprimirla.
ms.assetid: 49FD0D63-0F7F-48C6-81B6-25715294E7B7
title: IsWindowRedirectedForPrint función)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720728"
---
# <a name="iswindowredirectedforprint-function"></a>IsWindowRedirectedForPrint función)

La función **IsWindowRedirectedForPrint** determina si la ventana especificada se redirige actualmente para imprimirla.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI IsWindowRedirectedForPrint(
  _In_   HWND hWnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hWnd* \[ de\]
</dt> <dd>

Controlador de la ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la ventana se redirige actualmente para imprimirla, la función devuelve un valor distinto de cero; de lo contrario, devuelve cero.

## <a name="remarks"></a>Observaciones

Una ventana se redirige para imprimir cuando procesa una llamada a [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow). En una llamada a **PrintWindow**, una ventana representa su contenido en un contexto de dispositivo fuera de la pantalla.

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>User32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**impresión de WM \_**](/windows/desktop/gdi/wm-print)
</dt> <dt>

[**PRINTCLIENT de WM \_**](/windows/desktop/gdi/wm-printclient)
</dt> </dl>

 

