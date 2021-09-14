---
title: TTM_ADDTOOL mensaje (Commctrl.h)
description: Registra una herramienta con un control de información sobre herramientas.
ms.assetid: c974866b-20e7-45bc-914e-9dcf9af161e0
keywords:
- TTM_ADDTOOL controles de Windows mensaje
topic_type:
- apiref
api_name:
- TTM_ADDTOOL
- TTM_ADDTOOLA
- TTM_ADDTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29dad3e297f8c3430f18286afa9a998eaf578a26
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165946"
---
# <a name="ttm_addtool-message"></a>Mensaje \_ ADDTOOL de TTM

Registra una herramienta con un control de información sobre herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que contiene información que el control de información sobre herramientas necesita para mostrar texto para la herramienta. El **miembro cbSize** de esta estructura debe rellenarse antes de enviar este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TTM \_ ADDTOOLW** (Unicode) y **TTM \_ ADDTOOLA** (ANSI)<br/>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DELTOOL DE TTM \_**](ttm-deltool.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Acerca de los controles de información sobre herramientas](tooltip-controls.md)
</dt> </dl>

 

 





