---
title: TCM_SETPADDING mensaje (Commctrl.h)
description: Establece la cantidad de espacio (relleno) alrededor del icono y la etiqueta de cada pestaña en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetPadding.
ms.assetid: c7f84c0d-8bf4-429a-b403-a0019575e72e
keywords:
- TCM_SETPADDING controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353cde946944bda7dc8d285f863d976e29353996
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166189"
---
# <a name="tcm_setpadding-message"></a>Mensaje \_ SETPADDING de TCM

Establece la cantidad de espacio (relleno) alrededor del icono y la etiqueta de cada pestaña en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetPadding.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

LOWORD [**es**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) un valor **INT** que especifica la cantidad de relleno horizontal, en píxeles. [**HIWORD es**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) un valor **INT** que especifica la cantidad de relleno vertical, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

