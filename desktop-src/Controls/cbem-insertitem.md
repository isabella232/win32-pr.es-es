---
title: CBEM_INSERTITEM mensaje (Commctrl.h)
description: Inserta un nuevo elemento en un control ComboBoxEx.
ms.assetid: c99db676-204d-44c9-aaa3-81b70fe2cf44
keywords:
- CBEM_INSERTITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- CBEM_INSERTITEM
- CBEM_INSERTITEMA
- CBEM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4d9627efef4796554dfdbe1d7263747cc6b1c32b2cc00d5619a7cb7953024cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699315"
---
# <a name="cbem_insertitem-message"></a>Mensaje \_ INSERTITEM de CBEM

Inserta un nuevo elemento en un control ComboBoxEx.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) que contiene información sobre el elemento que se va a insertar. Cuando se envía el mensaje, el **miembro iItem** debe establecerse para indicar el índice de base cero en el que se va a insertar el elemento. Para insertar un elemento al final de la lista, establezca el **miembro iItem** en -1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice en el que se insertó el nuevo elemento si se ha realizado correctamente o -1 en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **CBEM \_ INSERTITEMW** (Unicode) y **CBEM \_ INSERTITEMA** (ANSI)<br/>           |



 

 





