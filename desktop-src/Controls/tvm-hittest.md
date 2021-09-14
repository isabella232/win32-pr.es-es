---
title: TVM_HITTEST mensaje (Commctrl.h)
description: Determina la ubicación del punto especificado en relación con el área cliente de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ HitTest.
ms.assetid: 18ea3737-f429-4c10-9133-3b5729aa36fa
keywords:
- TVM_HITTEST controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165685"
---
# <a name="tvm_hittest-message"></a>Mensaje \_ DE TVM HITTEST

Determina la ubicación del punto especificado en relación con el área cliente de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ HitTest.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TVHITTESTINFO.**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) Cuando se envía el mensaje, el **miembro pt** especifica las coordenadas del punto que se va a probar. Cuando el mensaje vuelve, el **miembro hItem** es el identificador del elemento en el punto especificado o **NULL** si ningún elemento ocupa el punto. Además, cuando el mensaje vuelve, el **miembro flags** es un valor de prueba de posición que indica la ubicación del punto especificado. Para obtener una lista de valores de prueba de acceso, vea la descripción de la **estructura TVHITTESTINFO.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador al elemento de vista de árbol que ocupa el punto especificado, o **NULL** si ningún elemento ocupa el punto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





