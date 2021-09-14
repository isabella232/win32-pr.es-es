---
title: TCM_ADJUSTRECT mensaje (Commctrl.h)
description: Calcula el área de presentación de un control de pestaña dado un rectángulo de ventana, o calcula el rectángulo de ventana que correspondería a un área de presentación especificada. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ AdjustRect.
ms.assetid: 2f14201a-e4a3-4ae5-b9cf-4a674c52f24a
keywords:
- TCM_ADJUSTRECT controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166293"
---
# <a name="tcm_adjustrect-message"></a>Mensaje \_ ADJUSTRECT de TCM

Calcula el área de presentación de un control de pestaña dado un rectángulo de ventana, o calcula el rectángulo de ventana que correspondería a un área de presentación especificada. Puede enviar este mensaje explícitamente o mediante la [**macro TabCtrl \_ AdjustRect.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Operación que se realizará. Si este parámetro es **TRUE,** *lParam especifica* un rectángulo para mostrar y recibe el rectángulo de ventana correspondiente. Si este parámetro es **FALSE,** *lParam* especifica un rectángulo de ventana y recibe el área de presentación correspondiente.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que especifica el rectángulo especificado y recibe el rectángulo calculado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este mensaje solo se aplica a los controles de tabulación que se encuentran en la parte superior. No se aplica a los controles de tabulación que están en los lados o en la parte inferior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

