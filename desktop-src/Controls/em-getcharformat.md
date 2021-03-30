---
title: Mensaje EM_GETCHARFORMAT (RichEdit. h)
description: Determina el formato de caracteres en un control Rich Edit.
ms.assetid: 210b8719-5ed7-49f2-bd93-8a4e1efab1e8
keywords:
- EM_GETCHARFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd71db4d3a13f2acfe33c2843b0d9aad46c6f9fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079456"
---
# <a name="em_getcharformat-message"></a>\_Mensaje GETCHARFORMAT em

Determina el formato de caracteres en un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el intervalo de texto del que se va a recuperar el formato. Puede ser uno de los siguientes valores.



| Value                                                                                                                                                         | Significado                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <dt>**\_valor predeterminado de SCF**</dt> </dl>       | El formato de caracteres predeterminado.<br/>             |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <dt>**selección de SCF \_**</dt> </dl> | Formato de caracteres de la selección actual.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Estructura [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) que recibe los atributos del primer carácter. El miembro **dwMask** especifica qué atributos son coherentes en toda la selección. Por ejemplo, si toda la selección está en cursiva o no en cursiva, \_ se establece cfm cursiva; si la selección está en parte en cursiva y no en parte, cfm \_ cursiva no se establece.

Microsoft Rich Edit 2,0 y versiones posteriores: este parámetro puede ser un puntero a una estructura [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) , que es una extensión de la estructura [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) . Antes de enviar el mensaje **\_ GETCHARFORMAT em** , establezca el miembro **cbSize** de la estructura para indicar la versión de la estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve el valor del miembro **dwMask** de la estructura [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) .

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

[**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





