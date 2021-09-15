---
description: Indica que el usuario ha presionado la tecla F1.
ms.assetid: 6a090125-67dd-4267-9973-10e32c6e4f1f
title: WM_HELP mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dd1b042a2e57fb64eb3aa81f38cec336e33efab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468034"
---
# <a name="wm_help-message"></a>Mensaje DE AYUDA DE WM \_

Indica que el usuario ha presionado la tecla F1. Si un menú está activo cuando se presiona F1, **WM \_ HELP** se envía a la ventana asociada al menú; de lo contrario, **WM \_ HELP** se envía a la ventana que tiene el foco del teclado. Si ninguna ventana tiene el foco de teclado, **WM \_ HELP** se envía a la ventana activa actualmente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lfos* 
</dt> <dd>

Dirección de una estructura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) que contiene información sobre el elemento de menú, el control, el cuadro de diálogo o la ventana para la que se solicita ayuda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE.**

## <a name="remarks"></a>Observaciones

La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pasa **WM \_ HELP** a la ventana primaria de una ventana secundaria o al propietario de una ventana de nivel superior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



 

 
