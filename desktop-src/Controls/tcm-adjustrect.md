---
title: Mensaje de TCM_ADJUSTRECT (commctrl. h)
description: Calcula el área de presentación de un control de ficha dado un rectángulo de ventana o calcula el rectángulo de ventana que se correspondería con un área de presentación especificada. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ AdjustRect.
ms.assetid: 2f14201a-e4a3-4ae5-b9cf-4a674c52f24a
keywords:
- TCM_ADJUSTRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c1612a4f6c2fc436f858807fca59112c376a35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658359"
---
# <a name="tcm_adjustrect-message"></a>\_Mensaje ADJUSTRECT de TCM

Calcula el área de presentación de un control de ficha dado un rectángulo de ventana o calcula el rectángulo de ventana que se correspondería con un área de presentación especificada. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ AdjustRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Operación que se va a realizar. Si este parámetro es **true**, *lParam* especifica un rectángulo de presentación y recibe el rectángulo de ventana correspondiente. Si este parámetro es **false**, *lParam* especifica un rectángulo de ventana y recibe el área de presentación correspondiente.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica el rectángulo dado y recibe el rectángulo calculado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este mensaje solo se aplica a los controles de ficha que se encuentran en la parte superior. No se aplica a los controles de ficha que se encuentran en los lados o en la parte inferior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

