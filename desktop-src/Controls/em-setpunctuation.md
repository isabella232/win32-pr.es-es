---
title: Mensaje EM_SETPUNCTUATION (RichEdit. h)
description: Establece los caracteres de puntuación para un control Rich Edit.
ms.assetid: c0c8ad14-63e2-4be8-8fc0-6b8ef9be4522
keywords:
- EM_SETPUNCTUATION controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150915"
---
# <a name="em_setpunctuation-message"></a>\_Mensaje SETPUNCTUATION em

Establece los caracteres de puntuación para un control Rich Edit.

> [!Note]  
> Este mensaje solo se admite en las versiones en idioma asiático de Microsoft Rich Edit 1,0. No se admite en las versiones posteriores.

 

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el tipo de puntuación, que puede ser uno de los valores siguientes.



| Value                                                                                                                                                      | Significado                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <dt>**EQUIPOS \_ líderes**</dt> </dl>       | Caracteres de puntuación iniciales.<br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <dt>**PC \_ después**</dt> </dl> | Siguientes caracteres de puntuación.<br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <dt>**delimitador de PC \_**</dt> </dl> | Delimitador.<br/>                        |
| <span id="PC_OVERFLOW_"></span><span id="pc_overflow_"></span><dl> <dt>**PC \_ de DESBORDAMIENTO** de</dt> </dl> | No se admite.<br/>                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura de [**puntuación**](/windows/desktop/api/Richedit/ns-richedit-punctuation) que contiene los caracteres de puntuación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si se produce un error en la operación, el valor devuelto es cero.

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

[**\_GETPUNCTUATION em**](em-getpunctuation.md)
</dt> <dt>

[**PUNTUACIÓN**](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





