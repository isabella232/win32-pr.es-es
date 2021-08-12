---
title: EM_SETCHARFORMAT mensaje (Richedit.h)
description: Establece el formato de caracteres en un control de edición enriquecido.
ms.assetid: 5e7a545d-4ca4-4dc6-badb-584c11194982
keywords:
- EM_SETCHARFORMAT controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100cfb1d322cde2d411a0298ee86c224899669defc585826b16bf96751bb4639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118673135"
---
# <a name="em_setcharformat-message"></a>Mensaje \_ SETCHARFORMAT EM

Establece el formato de caracteres en un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Formato de caracteres que se aplica al control. Si este parámetro es cero, se establece el formato de caracteres predeterminado. De lo contrario, puede ser uno de los siguientes valores.



| Value                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SCF_ALL"></span><span id="scf_all"></span><dl> <dt>**SCF \_ ALL**</dt> </dl>                                     | Aplica el formato a todo el texto del control . No es válido con **SCF \_ SELECTION** o **SCF \_ WORD**.<br/>                                                                                                                                                                                         |
| <span id="SCF_ASSOCIATEFONT"></span><span id="scf_associatefont"></span><dl> <dt>**SCF \_ ASSOCIATEFONT**</dt> </dl>       | **RichEdit 4.1:** Asocia una fuente a un script determinado, cambiando así la fuente predeterminada para ese script. Para especificar la fuente, use los siguientes miembros de [**CHARFORMAT2:**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) **yHeight**, **bCharSet**, **bPitchAndFamily,** **szFaceName** y **lcid**.<br/>                     |
| <span id="SCF_ASSOCIATEFONT2"></span><span id="scf_associatefont2"></span><dl> <dt>**SCF \_ ASSOCIATEFONT2**</dt> </dl>    | **RichEdit 4.1:** Asocia una fuente suplente (plane-2) a un script determinado, cambiando así la fuente predeterminada para ese script. Para especificar la fuente, use los siguientes miembros de [**CHARFORMAT2:**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) **yHeight**, **bCharSet**, **bPitchAndFamily,** **szFaceName** y **lcid**.<br/> |
| <span id="SCF_CHARREPFROMLCID"></span><span id="scf_charrepfromlcid"></span><dl> <dt>**SCF \_ CHARREPFROMLCID**</dt> </dl> | Obtiene el carácter del LCID.<br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <dt>**SCF \_ DEFAULT**</dt> </dl>                         | **RichEdit 4.1:** Establece la fuente predeterminada para el control. <br/>                                                                                                                                                                                                                                      |
| <span id="SPF_DONTSETDEFAULT"></span><span id="spf_dontsetdefault"></span><dl> <dt>**SPF \_ DONTSETDEFAULT**</dt> </dl>    | Impide establecer el formato de párrafo predeterminado cuando el control de edición enriquecido está vacío.<br/>                                                                                                                                                                                                             |
| <span id="SCF_NOKBUPDATE"></span><span id="scf_nokbupdate"></span><dl> <dt>**SCF \_ NOKBUPDATE**</dt> </dl>                | **RichEdit 4.1:** Impide que el cambio de teclado coincida con la fuente. Por ejemplo, si se establece una fuente árabe, normalmente la característica de teclado automático para idiomas de Bidi cambia el teclado a un teclado árabe.<br/>                                                                                 |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <dt>**SELECCIÓN DE \_ SCF**</dt> </dl>                   | Aplica el formato a la selección actual. Si la selección está vacía, el formato de caracteres se aplica al punto de inserción y el nuevo formato de caracteres solo está en vigor hasta que cambia el punto de inserción.<br/>                                                                      |
| <span id="SPF_SETDEFAULT"></span><span id="spf_setdefault"></span><dl> <dt>**SPF \_ SETDEFAULT**</dt> </dl>                | Establece los atributos de formato de párrafo predeterminados.<br/>                                                                                                                                                                                                                                              |
| <span id="SCF_SMARTFONT"></span><span id="scf_smartfont"></span><dl> <dt>**SCF \_ SMARTFONT**</dt> </dl>                   | Aplique la fuente solo si puede controlar el script.<br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_USEUIRULES"></span><span id="scf_useuirules"></span><dl> <dt>**SCF \_ USEUIRULES**</dt> </dl>                | **RichEdit 4.1:** Se usa con **SCF \_ SELECTION**. Indica que el formato provenía de una barra de herramientas u otra herramienta de interfaz de usuario, por lo que se deben usar reglas de formato de interfaz de usuario en lugar de formato literal.<br/>                                                                                                               |
| <span id="SCF_WORD"></span><span id="scf_word"></span><dl> <dt>**SCF \_ WORD**</dt> </dl>                                  | Aplica el formato a la palabra o palabras seleccionadas. Si la selección está vacía pero el punto de inserción está dentro de una palabra, el formato se aplica a la palabra. El **valor de SCF \_ WORD** debe usarse junto con el **valor de SCF \_ SELECTION.**<br/>                                        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) que especifica el formato de caracteres que se usará. Solo se cambian los atributos de formato especificados por **el miembro dwMask.**

Microsoft Rich Edit 2.0 y versiones posteriores: este parámetro puede ser un puntero a una estructura [**CHARFORMAT2,**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) que es una extensión de la [**estructura CHARFORMAT.**](/windows/win32/api/richedit/ns-richedit-charformata) Antes de enviar **el mensaje EM \_ SETCHARFORMAT,** establezca el miembro **cbSize** de la estructura en o indique qué versión de la estructura `sizeof(CHARFORMAT)` se está `sizeof(CHARFORMAT2)` utilizando.

Los **miembros szFaceName** y **bCharSet** se pueden invalidar cuando no son válidos para los caracteres, por ejemplo: Arial en caracteres kanji.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si se produce un error en la operación, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Si este mensaje se envía más de una vez con los mismos parámetros, se alterna el efecto en el texto. Es decir, enviar el mensaje una vez produce el efecto, enviar el mensaje dos veces cancela el efecto, etc.

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

[**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





