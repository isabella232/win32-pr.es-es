---
title: HDM_SETORDERARRAY mensaje (Commctrl.h)
description: Establece el orden de izquierda a derecha de los elementos de encabezado. Puede enviar este mensaje explícitamente o usar la macro \_ SetOrderArray de encabezado.
ms.assetid: 094c424f-10bd-484d-8236-937811b703a6
keywords:
- HDM_SETORDERARRAY controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061971"
---
# <a name="hdm_setorderarray-message"></a>Mensaje \_ SETORDERARRAY de HDM

Establece el orden de izquierda a derecha de los elementos de encabezado. Puede enviar este mensaje explícitamente o usar la macro [**\_ SetOrderArray de**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) encabezado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tamaño del búfer en *lParam*, en elementos . Este valor debe ser igual al valor devuelto [**por HDM \_ GETITEMCOUNT**](hdm-getitemcount.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz que especifica el orden en el que se deben mostrar los elementos, de izquierda a derecha. Por ejemplo, si el contenido de la matriz es , el control muestra el elemento 2, el elemento 0 y el {2,0,1} elemento 1, de izquierda a derecha.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





