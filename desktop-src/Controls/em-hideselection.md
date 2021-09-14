---
title: EM_HIDESELECTION mensaje (Richedit.h)
description: El mensaje EM \_ HIDESELECTION oculta o muestra la selección en un control de edición enriquecido.
ms.assetid: 1245618f-c9e6-4876-9133-6009370cdb97
keywords:
- EM_HIDESELECTION controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_HIDESELECTION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a5690e52c2a25f5a359de205ac1584e1ef45ed4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062173"
---
# <a name="em_hideselection-message"></a>Mensaje \_ EM HIDESELECTION

El **mensaje EM \_ HIDESELECTION** oculta o muestra la selección en un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica si se va a ocultar o mostrar la selección. Si este parámetro es cero, se muestra la selección. De lo contrario, la selección está oculta.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





