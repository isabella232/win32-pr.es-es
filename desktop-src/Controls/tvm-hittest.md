---
title: Mensaje de TVM_HITTEST (commctrl. h)
description: Determina la ubicación del punto especificado con respecto al área cliente de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro de TreeView \_ HitTest.
ms.assetid: 18ea3737-f429-4c10-9133-3b5729aa36fa
keywords:
- TVM_HITTEST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50b91a11892a2bb904d2cd7d82b5b08cea18331b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079112"
---
# <a name="tvm_hittest-message"></a>TVM \_ HITTEST (mensaje)

Determina la ubicación del punto especificado con respecto al área cliente de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro de [**TreeView \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) . Cuando se envía el mensaje, el miembro **PT** especifica las coordenadas del punto que se va a probar. Cuando el mensaje vuelve, el miembro **hItem** es el identificador del elemento en el punto especificado o **null** si ningún elemento ocupa el punto. Además, cuando el mensaje vuelve, el miembro **Flags** es un valor de prueba de posicionamiento que indica la ubicación del punto especificado. Para obtener una lista de los valores de las pruebas de posicionamiento, vea la descripción de la estructura **TVHITTESTINFO** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del elemento de vista de árbol que ocupa el punto especificado, o **null** si ningún elemento ocupa el punto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





