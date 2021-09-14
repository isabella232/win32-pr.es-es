---
description: No aplica una aplicación cuando un IME seleccionado necesita información sobre la ventana candidata. La aplicación recibe este comando a través del mensaje WM \_ IME \_ REQUEST con la configuración de parámetros, como se muestra a continuación.
ms.assetid: 35849290-a5be-406f-82f5-4a7e2af48586
title: IMR_CANDIDATEWINDOW de notificación (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb905acace27cc9bb04ce2b14dc6a685b7c4f8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063111"
---
# <a name="imr_candidatewindow-notification-code"></a>Código de notificación DE IMR \_ CANDIDATEWINDOW

No aplica una aplicación cuando un IME seleccionado necesita información sobre la ventana candidata. La aplicación recibe este comando a través del mensaje [**WM \_ IME \_ REQUEST**](wm-ime-request.md) con la configuración de parámetros, como se muestra a continuación.


```C++
LRESULT IMR_CANDIDATEWINDOW
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Establezca en IMR \_ CANDIDATEWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Puntero a un búfer que contiene una [**estructura CANDIDATEFORM.**](/windows/win32/api/imm/ns-imm-candidateform) Su **miembro dwIndex** contiene el índice de la ventana candidata a la que se hace referencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si la aplicación rellena la [**estructura CANDIDATEFORM.**](/windows/win32/api/imm/ns-imm-candidateform) De lo contrario, el comando devuelve 0.

## <a name="remarks"></a>Observaciones

El IME puede enviar este comando a una ventana que ha borrado la marca SHOWUICANDIDATEWINDOW de ISC en el controlador de mensajes SETCONTEXT de \_ [**WM \_ IME. \_**](wm-ime-setcontext.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>Imm.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Administrador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Comandos del Administrador de métodos de entrada](input-method-manager-commands.md)
</dt> <dt>

[**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[**SOLICITUD \_ DE WM IME \_**](wm-ime-request.md)
</dt> <dt>

[**SETCONTEXT \_ de WM IME \_**](wm-ime-setcontext.md)
</dt> </dl>

 

 




