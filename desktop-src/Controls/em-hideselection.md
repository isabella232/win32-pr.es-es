---
title: Mensaje EM_HIDESELECTION (RichEdit. h)
description: El \_ mensaje HIDESELECTION de EM oculta o muestra la selección en un control Rich Edit.
ms.assetid: 1245618f-c9e6-4876-9133-6009370cdb97
keywords:
- EM_HIDESELECTION controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996004"
---
# <a name="em_hideselection-message"></a>\_Mensaje de HIDESELECTION em

El **mensaje \_ HIDESELECTION de EM** oculta o muestra la selección en un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica si se va a ocultar o Mostrar la selección. Si este parámetro es cero, se muestra la selección. De lo contrario, la selección está oculta.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





