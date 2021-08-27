---
title: TCM_SETCURSEL mensaje (Commctrl.h)
description: Selecciona una pestaña en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetCurSel.
ms.assetid: cf709d8c-c522-47c8-8ff3-463dc8e924b5
keywords:
- TCM_SETCURSEL controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bdfd0861f5249a823d9406b437fd0efbca64a757a4bcadd7991155a87ddbc59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104855"
---
# <a name="tcm_setcursel-message"></a>Mensaje \_ SETCURSEL de TCM

Selecciona una pestaña en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetCurSel.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de la pestaña que se selecciona.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de la pestaña seleccionada anteriormente si se realiza correctamente o -1 en caso contrario.

## <a name="remarks"></a>Comentarios

Un control de pestaña no envía un código de [notificación TCN \_ SELCHANGING](tcn-selchanging.md) o [TCN \_ SELCHANGE](tcn-selchange.md) cuando se selecciona una pestaña con este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





