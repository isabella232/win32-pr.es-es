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
ms.openlocfilehash: 50ae19287e3e30810b1d8c558be9b6153a86ab6b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173937"
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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **CBEM \_ SETITEMW** (Unicode) y **CBEM \_ SETITEMA** (ANSI)<br/>                 |



 

 





