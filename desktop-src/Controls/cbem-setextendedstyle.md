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
ms.openlocfilehash: efd1083e838d85f9cb659acb9a28b74a1d8605934be4c53fd72993e7470fad2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527975"
---
# <a name="cbem_setextendedstyle-message"></a>Mensaje \_ CBEM SETEXTENDEDSTYLE

Establece estilos extendidos dentro de un control ComboBoxEx.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor **DWORD** que indica qué estilos de *lParam* se verán afectados. Solo se cambiarán los estilos extendidos de *wParam.* Si este parámetro es cero, todos los estilos de *lParam* se verán afectados.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor **DWORD** que contiene los estilos extendidos del [control ComboBoxEx](comboboxex-control-extended-styles.md) que se establecerán para el control.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor DWORD** que contiene los estilos extendidos usados anteriormente para el control.

## <a name="remarks"></a>Comentarios

*wParam* permite modificar uno o varios estilos extendidos sin tener que recuperar primero los estilos existentes. Por ejemplo, si pasa [**CBES \_ EX \_ NOEDITIMAGE**](comboboxex-control-extended-styles.md) para *wParam* y 0 para *lParam*, se borrará el estilo **CBES \_ EX \_ NOEDITIMAGE,** pero todos los demás estilos seguirán siendo los mismos.

Si intenta establecer un estilo extendido para un control ComboBoxEx creado con el estilo SIMPLE de [**CBS, \_**](combo-box-styles.md) es posible que no se vuelva a dibujar correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





