---
title: Mensaje de HDM_SETITEM (commctrl. h)
description: Establece los atributos del elemento especificado en un control de encabezado. Puede enviar este mensaje explícitamente o utilizar la \_ macro header setItem.
ms.assetid: c8f0d526-3ebe-48c5-8aea-ea3703e2d983
keywords:
- HDM_SETITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_SETITEM
- HDM_SETITEMA
- HDM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b03a05b909cf8c7887edd2031f5346c419f1cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492160"
---
# <a name="hdm_setitem-message"></a>HDM \_ SETITEM

Establece los atributos del elemento especificado en un control de encabezado. Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice actual del elemento cuyos atributos se van a cambiar.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) que contiene información del elemento. Cuando se envía este mensaje, se debe establecer el miembro de **máscara** de la estructura para indicar los atributos que se van a establecer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se ejecuta correctamente o cero en caso contrario.

## <a name="remarks"></a>Observaciones

La estructura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) que admite este mensaje es compatible con la información de la lista de imágenes y el orden de los elementos. Mediante el uso de estos miembros, puede controlar el orden en que se muestran los elementos y especificar las imágenes que aparecerán con los elementos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDM \_ SETITEMW** (Unicode) y **HDM \_ SETITEMA** (ANSI)<br/>                   |



 

 





