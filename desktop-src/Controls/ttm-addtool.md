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
ms.openlocfilehash: bb66c43033e54ce51b396ff5bb11efe3b2a99e8eb2578a2e9fe4d4bc4487ccf0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769545"
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

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
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

 

 





