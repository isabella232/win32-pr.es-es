---
title: Mensaje de HDM_SETORDERARRAY (commctrl. h)
description: Establece el orden de izquierda a derecha de los elementos de encabezado. Puede enviar este mensaje explícitamente o utilizar la \_ macro header SetOrderArray.
ms.assetid: 094c424f-10bd-484d-8236-937811b703a6
keywords:
- HDM_SETORDERARRAY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_SETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f07874bfc102babec18b142a087b14e330044ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490865"
---
# <a name="hdm_setorderarray-message"></a>HDM \_ SETORDERARRAY

Establece el orden de izquierda a derecha de los elementos de encabezado. Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ SetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tamaño del búfer en *lParam*, en elementos. Este valor debe ser igual al valor devuelto por [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz que especifica el orden en el que se deben mostrar los elementos, de izquierda a derecha. Por ejemplo, si el contenido de la matriz es {2,0,1} , el control muestra el elemento 2, el elemento 0 y el elemento 1, de izquierda a derecha.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





