---
title: CBEM_SETITEM mensaje (Commctrl.h)
description: Establece los atributos de un elemento en un control ComboBoxEx.
ms.assetid: 752df8ea-fd5e-47fa-b729-d019bdde0904
keywords:
- CBEM_SETITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- CBEM_SETITEM
- CBEM_SETITEMA
- CBEM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b1010c090283a47404ee93ef5f3bc1cf2d5ffe71a646d6d734cb443152bdd64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527935"
---
# <a name="cbem_setitem-message"></a>Mensaje \_ SETITEM de CBEM

Establece los atributos de un elemento en un control ComboBoxEx.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) que contiene la información de elemento que se va a establecer. Cuando se envía el mensaje, se debe establecer el miembro **mask** de la estructura para indicar qué atributos son válidos y el miembro **iItem** debe especificar el índice de base cero del elemento que se va a modificar. Si se **establece el miembro iItem** en -1, se modificará el elemento que se muestra en el control de edición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **CBEM \_ SETITEMW** (Unicode) y **CBEM \_ SETITEMA** (ANSI)<br/>                 |



 

 





