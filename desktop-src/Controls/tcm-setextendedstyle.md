---
title: Mensaje de TCM_SETEXTENDEDSTYLE (commctrl. h)
description: Establece los estilos extendidos que usará el control de pestaña. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetExtendedStyle.
ms.assetid: 96ccebe1-2836-4198-8cd7-858401562c21
keywords:
- TCM_SETEXTENDEDSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4c789b45eaae6cb3b1bc4fed6f216ec5010b463
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079394"
---
# <a name="tcm_setextendedstyle-message"></a>\_Mensaje SETEXTENDEDSTYLE de TCM

Establece los estilos extendidos que usará el control de pestaña. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor **DWORD** que indica qué estilos de *lParam* se van a ver afectados. Solo se cambiarán los estilos extendidos de *wParam* . Todos los demás estilos se conservarán tal como están. Si este parámetro es cero, se verán afectados todos los estilos de *lParam* .

</dd> <dt>

*lParam* 
</dt> <dd>

Valor que especifica los estilos de control de pestaña extendido. Este valor es una combinación de [estilos extendidos](tab-control-extended-styles.md)de control de pestaña.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **DWORD** que contiene los estilos extendidos del control de pestaña anterior.

## <a name="remarks"></a>Observaciones

El parámetro *wParam* permite modificar uno o más estilos extendidos sin tener que recuperar primero los estilos existentes. Por ejemplo, si pasa los [**ect \_ ex \_ FLATSEPARATORS**](tab-control-extended-styles.md) para *wParam* y 0 para *lParam*, se borrará el estilo **TCS \_ ex \_ FLATSEPARATORS** , pero el resto de los estilos permanecerán iguales.

Por motivos de compatibilidad con versiones anteriores, la macro [**TabCtrl \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) no se ha actualizado para usar *dwExMask*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETEXTENDEDSTYLE TCM**](tcm-getextendedstyle.md)
</dt> </dl>

 

 





