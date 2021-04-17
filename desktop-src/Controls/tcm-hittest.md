---
title: Mensaje de TCM_HITTEST (commctrl. h)
description: Determina qué pestaña, si la hay, está en la posición de pantalla especificada. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ HitTest.
ms.assetid: 0334f616-8d39-4460-a7f8-692a9ffab012
keywords:
- TCM_HITTEST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04787662e417513d8c9c93e45cecd0d8bddc6cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658352"
---
# <a name="tcm_hittest-message"></a>\_Mensaje HITTEST de TCM

Determina qué pestaña, si la hay, está en la posición de pantalla especificada. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**TCHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) que especifica la posición de la pantalla que se va a probar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de la pestaña o-1 si no hay ninguna tabulación en la posición especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





