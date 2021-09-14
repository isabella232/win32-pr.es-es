---
title: TB_SETANCHORHIGHLIGHT mensaje (Commctrl.h)
description: Establece el valor de resaltado de delimitador para una barra de herramientas.
ms.assetid: d31652d5-e9cf-4bf3-8f90-818eb078fa87
keywords:
- TB_SETANCHORHIGHLIGHT controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166661"
---
# <a name="tb_setanchorhighlight-message"></a>Mensaje \_ DE TB SETANCHORHIGHLIGHT

Establece el valor de resaltado de delimitador para una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

**Valor BOOL** que especifica si el resaltado de delimitadores está habilitado o deshabilitado. Si este valor es distinto de cero, se habilitará el resaltado de delimitadores. Si este valor es cero, se deshabilitará el resaltado de delimitadores.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la configuración de resaltado de delimitador anterior. Si este valor es distinto de cero, se ha habilitado el resaltado de delimitadores. Si este valor es cero, se deshabilitó el resaltado de delimitadores.

## <a name="remarks"></a>Observaciones

El resaltado de delimitadores en una barra de herramientas significa que el último elemento resaltado permanecerá resaltado hasta que se resalte otro elemento. Esto sucede incluso si el cursor deja el control de la barra de herramientas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





