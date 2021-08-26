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
ms.openlocfilehash: ceed10eec9038b338d060f28acdab8a10aa88aecef6b264b6d6d0682168f4937
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919145"
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

## <a name="remarks"></a>Comentarios

El sistema usa el tamaño para determinar qué versión de la biblioteca de vínculos dinámicos (DLL) de control común se está utilizando.

Si una aplicación usa la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear la barra de herramientas, la aplicación debe enviar este mensaje a la barra de herramientas antes de enviar el mensaje [**\_ ADDBITMAP**](tb-addbitmap.md) o [**TB \_ ADDBUTTONS de TB.**](tb-addbuttons.md) La [**función CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) envía automáticamente **TB \_ BUTTONSTRUCTSIZE** y el tamaño de la [**estructura TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) es un parámetro de la función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

