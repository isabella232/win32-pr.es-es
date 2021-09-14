---
title: EM_SETPARAFORMAT mensaje (Richedit.h)
description: Establece el formato de párrafo para la selección actual en un control de edición enriquecido.
ms.assetid: 2d612e1b-1489-4055-929b-e0b2719f6ec2
keywords:
- EM_SETPARAFORMAT controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8780ed79650a90a8d85ee8025dbe97e9af36aa1a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062076"
---
# <a name="em_setparaformat-message"></a>Mensaje \_ EM SETPARAFORMAT

Establece el formato de párrafo para la selección actual en un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) que especifica los nuevos atributos de formato de párrafo. Solo se cambian los atributos especificados por el **miembro dwMask.**

Microsoft Rich Edit 2.0 y versiones posteriores: este parámetro puede ser un puntero a una estructura [**PARAFORMAT2,**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) que es una extensión de la [**estructura PARAFORMAT.**](/windows/desktop/api/Richedit/ns-richedit-paraformat) Antes de enviar **el \_ mensaje EM SETPARAFORMAT,** establezca el miembro **cbSize** de la estructura para indicar la versión de la estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si se produce un error en la operación, el valor devuelto es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





