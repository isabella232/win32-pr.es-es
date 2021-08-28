---
title: EM_GETPARAFORMAT mensaje (Richedit.h)
description: Recupera el formato de párrafo de la selección actual en un control de edición enriquecido.
ms.assetid: 79a7d34f-5da1-452d-b31f-b2eec913f5cb
keywords:
- EM_GETPARAFORMAT controles de Windows mensaje
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
ms.openlocfilehash: eda99d1fefc0e2a13cc989726c86588103b7f94d7042b98393709cf4a2cd5f29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048855"
---
# <a name="em_getparaformat-message"></a>Mensaje \_ GETPARAFORMAT DE EM

Recupera el formato de párrafo de la selección actual en un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) que recibe los atributos de formato de párrafo de la selección actual.

Si se selecciona más de un párrafo, la estructura recibe los atributos del primer párrafo y el **miembro dwMask** especifica qué atributos son coherentes en toda la selección.

Microsoft Rich Edit 2.0 y versiones posteriores: este parámetro puede ser un puntero a una estructura [**PARAFORMAT2,**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) que es una extensión de la [**estructura PARAFORMAT.**](/windows/desktop/api/Richedit/ns-richedit-paraformat) Antes de enviar **el mensaje EM \_ GETPARAFORMAT,** establezca el miembro **cbSize** de la estructura para indicar la versión de la estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve el valor del miembro **dwMask** de la [**estructura PARAFORMAT.**](/windows/desktop/api/Richedit/ns-richedit-paraformat)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





