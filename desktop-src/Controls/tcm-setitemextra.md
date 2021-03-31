---
title: Mensaje de TCM_SETITEMEXTRA (commctrl. h)
description: Establece el número de bytes por pestaña reservado para los datos definidos por la aplicación en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetItemExtra.
ms.assetid: 8315f1fd-8eca-48bd-bb4a-71b09e8aa2c4
keywords:
- TCM_SETITEMEXTRA controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149881"
---
# <a name="tcm_setitemextra-message"></a>\_Mensaje SETITEMEXTRA de TCM

Establece el número de bytes por pestaña reservado para los datos definidos por la aplicación en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetItemExtra**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de bytes adicionales.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

De forma predeterminada, el número de bytes adicionales es cuatro. Una aplicación que cambia el número de bytes adicionales no puede usar la estructura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) para recuperar y establecer los datos definidos por la aplicación para una pestaña. En su lugar, debe definir una nueva estructura que conste de la estructura [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) seguido de los miembros definidos por la aplicación.

Una aplicación solo debe cambiar el número de bytes adicionales cuando un control de ficha no contiene ninguna pestaña.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





