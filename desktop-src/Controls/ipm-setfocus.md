---
title: Mensaje de IPM_SETFOCUS (commctrl. h)
description: Establece el foco de teclado en el campo especificado en el control de dirección IP. Se seleccionará todo el texto de ese campo.
ms.assetid: 4b975eb2-85e1-4e33-a803-99b48d2ff5e8
keywords:
- IPM_SETFOCUS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- IPM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d713e0a8b7eb838a2db5c4738c801d4fb76b782
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150546"
---
# <a name="ipm_setfocus-message"></a>Mensaje de SETFOCUS de IPM \_

Establece el foco de teclado en el campo especificado en el control de dirección IP. Se seleccionará todo el texto de ese campo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de campo basado en cero en el que se debe establecer el foco. Si este valor es mayor que el número de campos, el foco se establece en el primer campo en blanco. Si todos los campos no están en blanco, el foco se establece en el primer campo.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





