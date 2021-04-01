---
title: Mensaje EM_SETCHARFORMAT (RichEdit. h)
description: Establece el formato de caracteres en un control Rich Edit.
ms.assetid: 5e7a545d-4ca4-4dc6-badb-584c11194982
keywords:
- EM_SETCHARFORMAT controles de mensajes de Windows
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
ms.openlocfilehash: ba8f37960659f29dd33d5b8f27f0b5a2e3d35eb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150921"
---
# <a name="em_setcharformat-message"></a>\_Mensaje SETCHARFORMAT em

Establece el formato de caracteres en un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Formato de caracteres que se aplica al control. Si este parámetro es cero, se establece el formato de carácter predeterminado. De lo contrario, puede ser uno de los valores siguientes.



| Value                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SCF_ALL"></span><span id="scf_all"></span><dl> <dt>**SCF \_ todo**</dt> </dl>                                     | Aplica el formato a todo el texto del control. No es válido con la **\_ selección SCF** o la **\_ palabra SCF**.<br/>                                                                                                                                                                                         |
| <span id="SCF_ASSOCIATEFONT"></span><span id="scf_associatefont"></span><dl> <dt>**SCF \_ ASSOCIATEFONT**</dt> </dl>       | **RichEdit 4,1:** Asocia una fuente a un script determinado, con lo que se cambia la fuente predeterminada para ese script. Para especificar la fuente, use los siguientes miembros de [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** y **LCID**.<br/>                     |
| <span id="SCF_ASSOCIATEFONT2"></span><span id="scf_associatefont2"></span><dl> <dt>**SCF \_ ASSOCIATEFONT2**</dt> </dl>    | **RichEdit 4,1:** Asocia una fuente suplente (plano 2) a un script determinado, con lo que se cambia la fuente predeterminada para ese script. Para especificar la fuente, use los siguientes miembros de [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** y **LCID**.<br/> |
| <span id="SCF_CHARREPFROMLCID"></span><span id="scf_charrepfromlcid"></span><dl> <dt>**SCF \_ CHARREPFROMLCID**</dt> </dl> | Obtiene el repertorio de caracteres del LCID.<br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <dt>**\_valor predeterminado de SCF**</dt> </dl>                         | **RichEdit 4,1:** Establece la fuente predeterminada para el control. <br/>                                                                                                                                                                                                                                      |
| <span id="SPF_DONTSETDEFAULT"></span><span id="spf_dontsetdefault"></span><dl> <dt>**DONTSETDEFAULT de SPF \_**</dt> </dl>    | Impide establecer el formato de párrafo predeterminado cuando el control Rich Edit está vacío.<br/>                                                                                                                                                                                                             |
| <span id="SCF_NOKBUPDATE"></span><span id="scf_nokbupdate"></span><dl> <dt>**SCF \_ NOKBUPDATE**</dt> </dl>                | **RichEdit 4,1:** Impide que el cambio de teclado coincida con la fuente. Por ejemplo, si se establece una fuente árabe, normalmente la característica de teclado automático para los idiomas bidireccionales cambia el teclado a un teclado árabe.<br/>                                                                                 |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <dt>**selección de SCF \_**</dt> </dl>                   | Aplica el formato a la selección actual. Si la selección está vacía, el formato de caracteres se aplica al punto de inserción y el nuevo formato de carácter solo está en vigor hasta que el punto de inserción cambie.<br/>                                                                      |
| <span id="SPF_SETDEFAULT"></span><span id="spf_setdefault"></span><dl> <dt>**SETDEFAULT de SPF \_**</dt> </dl>                | Establece los atributos de formato de párrafo predeterminados.<br/>                                                                                                                                                                                                                                              |
| <span id="SCF_SMARTFONT"></span><span id="scf_smartfont"></span><dl> <dt>**SCF \_ SMARTFONT**</dt> </dl>                   | Aplique la fuente solo si puede controlar el script.<br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_USEUIRULES"></span><span id="scf_useuirules"></span><dl> <dt>**SCF \_ USEUIRULES**</dt> </dl>                | **RichEdit 4,1:** Se usa con la **\_ selección de SCF**. Indica que el formato proviene de una barra de herramientas u otra herramienta de interfaz de usuario, por lo que se deben usar reglas de formato de la interfaz de usuario en lugar del formato literal.<br/>                                                                                                               |
| <span id="SCF_WORD"></span><span id="scf_word"></span><dl> <dt>**\_palabra SCF**</dt> </dl>                                  | Aplica el formato a la palabra o palabras seleccionadas. Si la selección está vacía pero el punto de inserción está dentro de una palabra, el formato se aplica a la palabra. El valor de la **\_ palabra SCF** debe usarse junto con el valor de **\_ selección del SCF** .<br/>                                        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) que especifica el formato de caracteres que se va a utilizar. Solo se cambian los atributos de formato especificados por el miembro **dwMask** .

Microsoft Rich Edit 2,0 y versiones posteriores: este parámetro puede ser un puntero a una estructura [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) , que es una extensión de la estructura [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) . Antes de enviar el mensaje **\_ SETCHARFORMAT em** , establezca el miembro **cbSize** de la estructura en `sizeof(CHARFORMAT)` o `sizeof(CHARFORMAT2)` indique qué versión de la estructura se está usando.

Los miembros **szFaceName** y **bCharSet** pueden estar sobrereglados si no son válidos para los caracteres, por ejemplo: Arial en caracteres kanji.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si se produce un error en la operación, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Si este mensaje se envía más de una vez con los mismos parámetros, se alterna el efecto en el texto. Es decir, al enviar el mensaje una vez que se produce el efecto, el envío del mensaje se cancela dos veces, y así sucesivamente.

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

 

 





