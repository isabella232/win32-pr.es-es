---
title: Mensaje de CBEM_SETEXTENDEDSTYLE (commctrl. h)
description: Establece los estilos extendidos dentro de un control ComboBoxEx.
ms.assetid: 00848bd0-5a2f-4bfb-ae1f-ee3aa88ac57a
keywords:
- CBEM_SETEXTENDEDSTYLE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658379"
---
# <a name="cbem_setextendedstyle-message"></a>CBEM \_ SETEXTENDEDSTYLE

Establece los estilos extendidos dentro de un control ComboBoxEx.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor **DWORD** que indica qué estilos de *lParam* se van a ver afectados. Solo se cambiarán los estilos extendidos de *wParam* . Si este parámetro es cero, se verán afectados todos los estilos de *lParam* .

</dd> <dt>

*lParam* 
</dt> <dd>

Valor **DWORD** que contiene los [estilos extendidos del control ComboBoxEx](comboboxex-control-extended-styles.md) que se van a establecer para el control.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **DWORD** que contiene los estilos extendidos utilizados previamente para el control.

## <a name="remarks"></a>Observaciones

*wParam* permite modificar uno o más estilos extendidos sin tener que recuperar primero los estilos existentes. Por ejemplo, si pasa [**CBES \_ ex \_ NOEDITIMAGE**](comboboxex-control-extended-styles.md) para *wParam* y 0 para *lParam*, se borrará el estilo **CBES \_ ex \_ NOEDITIMAGE** , pero el resto de los estilos permanecerán iguales.

Si intenta establecer un estilo extendido para un control ComboBoxEx creado con el estilo [**\_ simple CBS**](combo-box-styles.md) , es posible que no se vuelva a dibujar correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





