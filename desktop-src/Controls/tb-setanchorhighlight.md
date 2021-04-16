---
title: Mensaje de TB_SETANCHORHIGHLIGHT (commctrl. h)
description: Establece la configuración de resaltado de delimitador de una barra de herramientas.
ms.assetid: d31652d5-e9cf-4bf3-8f90-818eb078fa87
keywords:
- TB_SETANCHORHIGHLIGHT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETANCHORHIGHLIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 809f71e446f7768d637258152db1dd2d56346dfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656465"
---
# <a name="tb_setanchorhighlight-message"></a>\_Mensaje SETANCHORHIGHLIGHT TB

Establece la configuración de resaltado de delimitador de una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor **booleano** que especifica si está habilitado o deshabilitado el resaltado de delimitadores. Si este valor es distinto de cero, se habilitará el resaltado de delimitadores. Si este valor es cero, se deshabilitará el resaltado de delimitadores.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor anterior de resaltado de delimitador. Si este valor es distinto de cero, se ha habilitado el resaltado de delimitadores. Si este valor es cero, se deshabilitó el resaltado de delimitadores.

## <a name="remarks"></a>Observaciones

El resaltado de delimitadores en una barra de herramientas significa que el último elemento resaltado permanecerá resaltado hasta que se resalte otro elemento. Esto sucede incluso si el cursor deja el control de barra de herramientas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





