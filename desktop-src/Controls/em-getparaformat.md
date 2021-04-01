---
title: Mensaje EM_GETPARAFORMAT (RichEdit. h)
description: Recupera el formato de párrafo de la selección actual en un control Rich Edit.
ms.assetid: 79a7d34f-5da1-452d-b31f-b2eec913f5cb
keywords:
- EM_GETPARAFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49060861a955e85d153fc9041c9b364db109f83a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996929"
---
# <a name="em_getparaformat-message"></a>\_Mensaje GETPARAFORMAT em

Recupera el formato de párrafo de la selección actual en un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura de [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) que recibe los atributos de formato de párrafo de la selección actual.

Si se selecciona más de un párrafo, la estructura recibe los atributos del primer párrafo y el miembro **dwMask** especifica qué atributos son coherentes en toda la selección.

Microsoft Rich Edit 2,0 y versiones posteriores: este parámetro puede ser un puntero a una estructura [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) , que es una extensión de la estructura [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) . Antes de enviar el mensaje **\_ GETPARAFORMAT em** , establezca el miembro **cbSize** de la estructura para indicar la versión de la estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve el valor del miembro **dwMask** de la estructura [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





