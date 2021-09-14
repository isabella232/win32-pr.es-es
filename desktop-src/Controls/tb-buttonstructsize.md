---
title: TB_BUTTONSTRUCTSIZE mensaje (Commctrl.h)
description: Especifica el tamaño de la estructura TBBUTTON.
ms.assetid: 4e63a075-4191-44c1-8df6-38fce51d4be5
keywords:
- TB_BUTTONSTRUCTSIZE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_BUTTONSTRUCTSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7187c1f4cb45306fd293c7eb74ef8807f395ba22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166897"
---
# <a name="tb_buttonstructsize-message"></a>Mensaje \_ BUTTONSTRUCTSIZE de TB

Especifica el tamaño de la [**estructura TBBUTTON.**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tamaño, en bytes, de la [**estructura TBBUTTON.**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El sistema usa el tamaño para determinar qué versión de la biblioteca de vínculos dinámicos (DLL) de control común se está utilizando.

Si una aplicación usa la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear la barra de herramientas, la aplicación debe enviar este mensaje a la barra de herramientas antes de enviar el mensaje [**\_ TB ADDBITMAP**](tb-addbitmap.md) o [**TB \_ ADDBUTTONS.**](tb-addbuttons.md) La [**función CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) envía automáticamente **TB \_ BUTTONSTRUCTSIZE** y el tamaño de la estructura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) es un parámetro de la función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

