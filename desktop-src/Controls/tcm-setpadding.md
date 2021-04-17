---
title: Mensaje de TCM_SETPADDING (commctrl. h)
description: Establece la cantidad de espacio (relleno) alrededor de la etiqueta y el icono de cada pestaña en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetPadding.
ms.assetid: c7f84c0d-8bf4-429a-b403-a0019575e72e
keywords:
- TCM_SETPADDING controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656458"
---
# <a name="tcm_setpadding-message"></a>\_Mensaje SETPADDING de TCM

Establece la cantidad de espacio (relleno) alrededor de la etiqueta y el icono de cada pestaña en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetPadding**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es un valor **int** que especifica la cantidad de relleno horizontal, en píxeles. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) es un valor **int** que especifica la cantidad de relleno vertical, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

