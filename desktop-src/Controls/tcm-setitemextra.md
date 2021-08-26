---
title: TCM_SETITEMEXTRA mensaje (Commctrl.h)
description: Establece el número de bytes por tabulación reservados para los datos definidos por la aplicación en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetItemExtra.
ms.assetid: 8315f1fd-8eca-48bd-bb4a-71b09e8aa2c4
keywords:
- TCM_SETITEMEXTRA controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_SETITEMEXTRA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f92fb85f7133053392bee39119c91b55240f84f0a51c8acc7dc9c732b596526c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104765"
---
# <a name="tcm_setitemextra-message"></a>Mensaje \_ SETITEMEXTRA de TCM

Establece el número de bytes por tabulación reservados para los datos definidos por la aplicación en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetItemExtra.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de bytes adicionales.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Comentarios

De forma predeterminada, el número de bytes adicionales es cuatro. Una aplicación que cambia el número de bytes adicionales no puede usar la [**estructura TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) para recuperar y establecer los datos definidos por la aplicación para una pestaña. En su lugar, debe definir una nueva estructura que consta de la [**estructura TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) seguida de miembros definidos por la aplicación.

Una aplicación solo debe cambiar el número de bytes adicionales cuando un control de ficha no contiene ninguna pestaña.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





