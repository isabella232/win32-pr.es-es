---
title: TCM_SETEXTENDEDSTYLE mensaje (Commctrl.h)
description: Establece los estilos extendidos que usará el control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetExtendedStyle.
ms.assetid: 96ccebe1-2836-4198-8cd7-858401562c21
keywords:
- TCM_SETEXTENDEDSTYLE controles de Windows mensaje
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
ms.openlocfilehash: 5a4a28bcf4cffe9aa2559f96a990d23511ece9fbbfc65468f84a4a874dce678a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876455"
---
# <a name="tcm_setextendedstyle-message"></a>Mensaje \_ TCM SETEXTENDEDSTYLE

Establece los estilos extendidos que usará el control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetExtendedStyle.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor **DWORD** que indica qué estilos de *lParam* se verán afectados. Solo se cambiarán los estilos extendidos de *wParam.* Todos los demás estilos se mantendrán tal y como están. Si este parámetro es cero, todos los estilos de *lParam* se verán afectados.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor que especifica los estilos de control de tabulación extendidos. Este valor es una combinación de estilos extendidos de control [de tabulación.](tab-control-extended-styles.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor DWORD** que contiene los estilos extendidos del control de pestaña anterior.

## <a name="remarks"></a>Comentarios

El *parámetro wParam* permite modificar uno o varios estilos extendidos sin tener que recuperar primero los estilos existentes. Por ejemplo, si pasa [**TCS \_ EX \_ FLATSEPARATORS**](tab-control-extended-styles.md) para *wParam* y 0 para *lParam*, se borrará el estilo **\_ TCS EX \_ FLATSEPARATORS,** pero todos los demás estilos seguirán siendo los mismos.

Por motivos de compatibilidad con versiones anteriores, la macro [**\_ TabCtrl SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) no se ha actualizado para usar *dwExMask*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TCM \_ GETEXTENDEDSTYLE**](tcm-getextendedstyle.md)
</dt> </dl>

 

 





