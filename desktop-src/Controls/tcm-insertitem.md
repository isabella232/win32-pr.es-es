---
title: Mensaje de TCM_INSERTITEM (commctrl. h)
description: Inserta una nueva pestaña en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ InsertItem.
ms.assetid: e547c49a-699c-4137-8680-20391d138d54
keywords:
- TCM_INSERTITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_INSERTITEM
- TCM_INSERTITEMA
- TCM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58002006944a221571e37c37d25259d0aaa74fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658351"
---
# <a name="tcm_insertitem-message"></a>\_Mensaje INSERTITEM TCM

Inserta una nueva pestaña en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de la nueva pestaña.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) que especifica los atributos de la pestaña. Este mensaje omite los miembros **dwState** y **dwStateMask** de esta estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de la nueva pestaña si se realiza correctamente, o-1 en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TCM \_ INSERTITEMW** (Unicode) y **TCM \_ INSERTITEMA** (ANSI)<br/>             |



 

 





