---
title: CBEM_SETEXTENDEDSTYLE mensaje (Commctrl.h)
description: Establece estilos extendidos dentro de un control ComboBoxEx.
ms.assetid: 00848bd0-5a2f-4bfb-ae1f-ee3aa88ac57a
keywords:
- CBEM_SETEXTENDEDSTYLE controles de Windows mensaje
topic_type:
- apiref
api_name:
- CBEM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a60518d2f6130c2c89e379125308fc2e647c6a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173941"
---
# <a name="cbem_setextendedstyle-message"></a>Mensaje \_ CBEM SETEXTENDEDSTYLE

Establece estilos extendidos dentro de un control ComboBoxEx.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor **DWORD** que indica qué estilos de *lParam* se van a ver afectados. Solo se cambiarán los estilos extendidos de *wParam.* Si este parámetro es cero, todos los estilos de *lParam* se verán afectados.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor **DWORD** que contiene los estilos extendidos del [control ComboBoxEx](comboboxex-control-extended-styles.md) que se establecerán para el control .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor DWORD** que contiene los estilos extendidos usados anteriormente para el control.

## <a name="remarks"></a>Observaciones

*wParam* permite modificar uno o varios estilos extendidos sin tener que recuperar primero los estilos existentes. Por ejemplo, si pasa [**CBES \_ EX \_ NOEDITIMAGE**](comboboxex-control-extended-styles.md) para *wParam* y 0 para *lParam*, se borrará el estilo **CBES \_ EX \_ NOEDITIMAGE,** pero todos los demás estilos seguirán siendo los mismos.

Si intenta establecer un estilo extendido para un control ComboBoxEx creado con el estilo SIMPLE de [**CBS, \_**](combo-box-styles.md) es posible que no se vuelva a dibujar correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





