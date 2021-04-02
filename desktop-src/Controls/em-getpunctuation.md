---
title: Mensaje EM_GETPUNCTUATION (RichEdit. h)
description: Obtiene los caracteres de puntuación actuales para el control Rich Edit.
ms.assetid: 1c04967b-d75e-4f54-b35b-cd50bac9cdfa
keywords:
- EM_GETPUNCTUATION controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 158c26deca3328d9cdbed7ffe7cf885b0582d1a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150825"
---
# <a name="em_getpunctuation-message"></a>\_Mensaje GETPUNCTUATION em

Obtiene los caracteres de puntuación actuales para el control Rich Edit.

> [!Note]  
> Este mensaje solo se admite en las versiones en idioma asiático de Microsoft Rich Edit 1,0. No se admite en las versiones posteriores de Rich Edit.

 

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

El tipo de puntuación puede ser uno de los valores siguientes.



| Value                                                                                                                                                      | Significado                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <dt>**EQUIPOS \_ líderes**</dt> </dl>       | Caracteres de puntuación iniciales<br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <dt>**PC \_ después**</dt> </dl> | Caracteres de puntuación siguientes<br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <dt>**delimitador de PC \_**</dt> </dl> | Delimitador<br/>                        |
| <span id="PC_OVERFLOW"></span><span id="pc_overflow"></span><dl> <dt>**desbordamiento de equipo \_**</dt> </dl>    | No compatible<br/>                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura de [**puntuación**](/windows/desktop/api/Richedit/ns-richedit-punctuation) que recibe los caracteres de puntuación.

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

[**\_SETPUNCTUATION em**](em-setpunctuation.md)
</dt> <dt>

[**PUNTUACIÓN**](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





