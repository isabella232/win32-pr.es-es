---
description: Indica que el usuario ha presionado la tecla F1.
ms.assetid: 6a090125-67dd-4267-9973-10e32c6e4f1f
title: WM_HELP mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d95f1573888d378a8a60d2e6cef08581600a5f0526ab40675eb0ce7d9d0d0a2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941105"
---
# <a name="wm_help-message"></a>Mensaje DE AYUDA DE WM \_

Indica que el usuario ha presionado la tecla F1. Si un menú está activo cuando se presiona F1, **WM \_ HELP** se envía a la ventana asociada al menú; de lo contrario, **WM \_ HELP** se envía a la ventana que tiene el foco del teclado. Si ninguna ventana tiene el foco del teclado, **WM \_ HELP** se envía a la ventana activa actualmente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lfos* 
</dt> <dd>

Dirección de una [**estructura HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) que contiene información sobre el elemento de menú, control, cuadro de diálogo o ventana para el que se solicita ayuda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE.**

## <a name="remarks"></a>Comentarios

La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pasa **WM \_ HELP** a la ventana primaria de una ventana secundaria o al propietario de una ventana de nivel superior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



 

 
