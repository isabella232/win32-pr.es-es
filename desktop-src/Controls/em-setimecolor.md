---
title: EM_SETIMECOLOR mensaje (Richedit.h)
description: Establece el color de composición del Editor de métodos de entrada (IME) para un control de edición enriquecido.
ms.assetid: ea5449c9-7d0f-4340-8e3e-1e0b77d443f6
keywords:
- EM_SETIMECOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c020bb3af2b1197afc005bd0b6efec82b609b88
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062098"
---
# <a name="em_setimecolor-message"></a>Mensaje \_ EM SETIMECOLOR

Establece el color de composición del Editor de métodos de entrada (IME) para un control de edición enriquecido.

> [!Note]  
> Este mensaje solo se admite en las versiones en idioma asiático de Microsoft Rich Edit 1.0. No se admite en versiones posteriores.

 

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) que contiene el color de composición que se va a establecer.

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

[**EM \_ GETIMECOLOR**](em-getimecolor.md)
</dt> <dt>

[**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





