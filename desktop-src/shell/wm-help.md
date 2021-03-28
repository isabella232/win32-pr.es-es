---
description: Indica que el usuario presionó la tecla F1.
ms.assetid: 6a090125-67dd-4267-9973-10e32c6e4f1f
title: Mensaje de WM_HELP (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dd1b042a2e57fb64eb3aa81f38cec336e33efab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985391"
---
# <a name="wm_help-message"></a>Mensaje de ayuda de WM \_

Indica que el usuario presionó la tecla F1. Si un menú está activo cuando se presiona F1, **la \_ ayuda de WM** se envía a la ventana asociada al menú; de lo contrario, la **\_ ayuda de WM** se envía a la ventana que tiene el foco de teclado. Si ninguna ventana tiene el foco de teclado, la **\_ ayuda de WM** se envía a la ventana activa actualmente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lphi* 
</dt> <dd>

La dirección de una estructura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) que contiene información sobre el elemento de menú, el control, el cuadro de diálogo o la ventana para la que se solicita ayuda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true**.

## <a name="remarks"></a>Observaciones

La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pasa **la \_ ayuda de WM** a la ventana primaria de una ventana secundaria o al propietario de una ventana de nivel superior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

 
