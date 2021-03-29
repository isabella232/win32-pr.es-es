---
title: Código de notificación de DL_DROPPED (commctrl. h)
description: Indica que el usuario ha completado una operación de arrastre soltando el botón primario del mouse. Un cuadro de lista de arrastre envía este código de notificación a su ventana primaria en forma de mensaje de la lista de arrastre. Para obtener más información, vea arrastrar mensajes de cuadro de lista.
ms.assetid: 81b9b424-2735-407d-bac9-f03ea2f48b4e
keywords:
- DL_DROPPED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- DL_DROPPED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b2480360ea38a00c4dd8efe6eb84eed8999890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905706"
---
# <a name="dl_dropped-notification-code"></a>\_Código de notificación DL quitado

Indica que el usuario ha completado una operación de arrastre soltando el botón primario del mouse. Un cuadro de lista de arrastre envía este código de notificación a su ventana primaria en forma de mensaje de la lista de arrastre. Para obtener más información, vea [arrastrar mensajes de cuadro de lista](about-list-boxes.md).


```C++
DL_DROPPED

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) que contiene el código de \_ notificación DL quitado, el identificador del cuadro de lista de arrastre y la posición del cursor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Normalmente, este código de notificación se procesa insertando el elemento que se está arrastrando a la lista delante del elemento bajo el cursor. Para recuperar el índice del elemento en la posición del cursor, utilice la función [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) . Tenga en cuenta que el \_ código de notificación DL quitado se envía incluso si el cursor no está en un elemento de lista. En ese caso, **LBItemFromPt** devuelve-1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





