---
title: Mensaje de HDM_INSERTITEM (commctrl. h)
description: Inserta un nuevo elemento en un control de encabezado. Puede enviar este mensaje explícitamente o utilizar el encabezado \_ InsertItem macro.
ms.assetid: aececf32-090d-4cd4-a239-4435a322f72e
keywords:
- HDM_INSERTITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_INSERTITEM
- HDM_INSERTITEMA
- HDM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9cabf86fea79fd437b3e9fb7e32890b3ba1a780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490709"
---
# <a name="hdm_insertitem-message"></a>HDM \_ INSERTITEM Message

Inserta un nuevo elemento en un control de encabezado. Puede enviar este mensaje explícitamente o utilizar el [**encabezado \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) macro.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento después del cual se va a insertar el nuevo elemento. El nuevo elemento se inserta al final del control de encabezado si *wParam* es mayor o igual que el número de elementos del control. Si *wParam* es cero, el nuevo elemento se inserta al principio del control de encabezado.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) que contiene información sobre el nuevo elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del nuevo elemento si se realiza correctamente, o-1 en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDM \_ INSERTITEMW** (Unicode) y **HDM \_ INSERTITEMA** (ANSI)<br/>             |



 

 





