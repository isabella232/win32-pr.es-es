---
title: HDM_INSERTITEM mensaje (Commctrl.h)
description: Inserta un nuevo elemento en un control de encabezado. Puede enviar este mensaje explícitamente o usar la macro Header \_ InsertItem.
ms.assetid: aececf32-090d-4cd4-a239-4435a322f72e
keywords:
- HDM_INSERTITEM controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061990"
---
# <a name="hdm_insertitem-message"></a>Mensaje \_ INSERTITEM de HDM

Inserta un nuevo elemento en un control de encabezado. Puede enviar este mensaje explícitamente o usar la macro [**Header \_ InsertItem.**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento después del cual se va a insertar el nuevo elemento. El nuevo elemento se inserta al final del control de encabezado si *wParam* es mayor o igual que el número de elementos del control . Si *wParam es* cero, el nuevo elemento se inserta al principio del control de encabezado.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) que contiene información sobre el nuevo elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del nuevo elemento si se realiza correctamente o -1 en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDM \_ INSERTITEMW** (Unicode) y **HDM \_ INSERTITEMA** (ANSI)<br/>             |



 

 





