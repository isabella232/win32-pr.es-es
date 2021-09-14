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
ms.openlocfilehash: 9dd6c7fdb47483ae0ddc841ae5f79b8f913e6a4f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166206"
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

## <a name="remarks"></a>Observaciones

De forma predeterminada, el número de bytes adicionales es cuatro. Una aplicación que cambia el número de bytes adicionales no puede usar la [**estructura TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) para recuperar y establecer los datos definidos por la aplicación para una pestaña. En su lugar, debe definir una nueva estructura que consta de la [**estructura TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) seguida de miembros definidos por la aplicación.

Una aplicación solo debe cambiar el número de bytes adicionales cuando un control de ficha no contiene ninguna pestaña.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





