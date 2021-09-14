---
title: EM_SETPUNCTUATION mensaje (Richedit.h)
description: Establece los caracteres de puntuación para un control de edición enriquecido.
ms.assetid: c0c8ad14-63e2-4be8-8fc0-6b8ef9be4522
keywords:
- EM_SETPUNCTUATION controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710392cee7f7a1fb04fce59d6549134255499172
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062074"
---
# <a name="em_setpunctuation-message"></a>Mensaje \_ SETPUNCTUATION DE EM

Establece los caracteres de puntuación para un control de edición enriquecido.

> [!Note]  
> Este mensaje solo se admite en versiones en idioma asiático de Microsoft Rich Edit 1.0. No se admite en versiones posteriores.

 

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el tipo de puntuación, que puede ser uno de los valores siguientes.



| Value                                                                                                                                                      | Significado                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <dt>**PC \_ LEADING**</dt> </dl>       | Caracteres de puntuación iniciales.<br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <dt>**PC \_ FOLLOWING**</dt> </dl> | Caracteres de puntuación siguientes.<br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <dt>**DELIMITADOR \_ DE PC**</dt> </dl> | Delimitador.<br/>                        |
| <span id="PC_OVERFLOW_"></span><span id="pc_overflow_"></span><dl> <dt>**PC \_ OVERFLOW**</dt> </dl> | No compatible.<br/>                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura PUNCTUATION**](/windows/desktop/api/Richedit/ns-richedit-punctuation) que contiene los caracteres de puntuación.

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

[**EM \_ GETPUNCTUATION**](em-getpunctuation.md)
</dt> <dt>

[**PUNTUACIÓN**](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





