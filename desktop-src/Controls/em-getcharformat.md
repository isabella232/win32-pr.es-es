---
title: EM_GETCHARFORMAT mensaje (Richedit.h)
description: Determina el formato de caracteres en un control de edición enriquecido.
ms.assetid: 210b8719-5ed7-49f2-bd93-8a4e1efab1e8
keywords:
- EM_GETCHARFORMAT controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062200"
---
# <a name="em_getcharformat-message"></a>Mensaje \_ GETCHARFORMAT EM

Determina el formato de caracteres en un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el intervalo de texto del que se va a recuperar el formato. Puede ser uno de los siguientes valores.



| Value                                                                                                                                                         | Significado                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <dt>**SCF \_ DEFAULT**</dt> </dl>       | Formato de caracteres predeterminado.<br/>             |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <dt>**SELECCIÓN DE \_ SCF**</dt> </dl> | Formato de caracteres de la selección actual.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Estructura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) que recibe los atributos del primer carácter. El **miembro dwMask** especifica qué atributos son coherentes en toda la selección. Por ejemplo, si toda la selección está en cursiva o no en cursiva, se establece CFM ITALIC; si la selección está parcialmente en cursiva y, en parte, no, no se establece \_ CFM \_ ITALIC.

Microsoft Rich Edit 2.0 y versiones posteriores: este parámetro puede ser un puntero a una estructura [**CHARFORMAT2,**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) que es una extensión de la [**estructura CHARFORMAT.**](/windows/win32/api/richedit/ns-richedit-charformata) Antes de enviar **el mensaje EM \_ GETCHARFORMAT,** establezca el miembro **cbSize** de la estructura para indicar la versión de la estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve el valor del miembro **dwMask** de la [**estructura CHARFORMAT.**](/windows/win32/api/richedit/ns-richedit-charformata)

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

[**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





