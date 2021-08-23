---
title: EM_GETIMEPROPERTY mensaje (Richedit.h)
description: Recupera la propiedad y las funciones del Editor de métodos de entrada (IME) asociado a la configuración regional de entrada actual.
ms.assetid: 0cbe52d4-c3e7-40bd-a6f6-da0a11056976
keywords:
- EM_GETIMEPROPERTY controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETIMEPROPERTY
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b96ad255d9d68cc76869b6f9163aedf549da19ff0c3ddba756f8da42267135c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541115"
---
# <a name="em_getimeproperty-message"></a>Mensaje \_ GETIMEPROPERTY EM

Recupera la propiedad y las funciones del Editor de métodos de entrada (IME) asociado a la configuración regional de entrada actual.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el tipo de información de propiedad que se debe recuperar. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                     | Significado                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="IGP_PROPERTY"></span><span id="igp_property"></span><dl> <dt>**IGP \_ (PROPIEDAD)**</dt> </dl>                | Información de propiedad.<br/>                                                         |
| <span id="IGP_CONVERSION"></span><span id="igp_conversion"></span><dl> <dt>**CONVERSIÓN \_ DE IGP**</dt> </dl>          | Capacidades de conversión. <br/>                                                     |
| <span id="IGP_SENTENCE"></span><span id="igp_sentence"></span><dl> <dt>**ORACIÓN IGP \_**</dt> </dl>                | Funcionalidades del modo de oración. <br/>                                                  |
| <span id="IGP_UI"></span><span id="igp_ui"></span><dl> <dt>**IGP \_ UI**</dt> </dl>                                  | Funcionalidades de la interfaz de usuario. <br/>                                                 |
| <span id="IGP_SETCOMPSTR"></span><span id="igp_setcompstr"></span><dl> <dt>**IGP \_ SETCOMPSTR**</dt> </dl>          | Funcionalidades de cadena de composición. <br/>                                             |
| <span id="IGP_SELECT"></span><span id="igp_select"></span><dl> <dt>**IGP \_ SELECT**</dt> </dl>                      | Funcionalidades de herencia de selección. <br/>                                          |
| <span id="IGP_GETIMEVERSION"></span><span id="igp_getimeversion"></span><dl> <dt>**IGP \_ GETIMEVERSION**</dt> </dl> | Recupera el número de versión del sistema para el que se creó el IME especificado. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la propiedad o el valor de funcionalidad, en función del valor del *parámetro lParam.* Para obtener más información, vea la sección Notas.

## <a name="remarks"></a>Comentarios

Si *wParam es* IGP \_ PROPERTY, devuelve uno o varios de los valores siguientes.



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IME \_ PROP \_ AT \_ CARET                | Si se establece, la ventana de conversión se encuentra en la posición del cursor de cursor. Si está despejado, la ventana está cerca de la posición del cursor de cursor.                                                                                                                                                                  |
| IME \_ PROP \_ SPECIAL \_ UI              | Si se establece, IME tiene una interfaz de usuario no estándar. La aplicación no debe dibujarse en la ventana de IME.                                                                                                                                                                  |
| IME \_ PROP \_ CANDLIST \_ START FROM \_ \_ 1 | Si se establece, las cadenas de la lista de candidatos se numeran a partir de 1. Si está claro, las cadenas comienzan en cero.                                                                                                                                                                |
| IME \_ PROP \_ UNICODE                  | Si se establece, el IME se ve como UnicodeIME. El sistema y el IME se comunicarán a través de la interfaz UnicodeIME. Si está claro, IME usará la interfaz ANSI para comunicarse con el sistema.                                                                    |
| IME \_ PROP \_ COMPLETE \_ ON \_ UNSELECT   | Si se establece, la ventana de conversión se encuentra en la posición del cursor de cursor. Si está despejado, la ventana está cerca de la posición del cursor de cursor.                                                                                                                                                                  |
| IME \_ PROP \_ ACCEPT \_ WIDE \_ VKEY       | Si se establece, el IME procesa el Unicode insertado que provenía de la [**función SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) mediante VK \_ PACKET. Si está claro, es posible que el IME no procese el Unicode que se ha inyectado y que el Unicode que se ha inyectado se envíe directamente a la aplicación. |



 

Si *wParam es* IGP \_ UI, devuelve uno o varios de los valores siguientes.



| Requisito | Valor |
|-----------------|-------------------------------------------------------------------------------------------------------|
| UI \_ CAP \_ 2700   | Admite valores de escape de texto de 0 o 2700. Para obtener más información, vea **lfEscapement**.             |
| UI \_ CAP \_ ROT90  | Admite valores de escape de texto de 0, 900, 1800 o 2700. Para obtener más información, vea **lfEscapement**. |
| ROTACIÓN \_ DE \_ MAYÚSCULAS DE LA INTERFAZ DE USUARIO | Admite cualquier valor de escape de texto. Para obtener más información, vea **lfEscapement**.                       |



 

Si *wParam es* SETCOMPSTR de IGP, \_ devuelve uno o varios de los valores siguientes.



| Requisito | Value |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SCS \_ CAP \_ COMPSTR            | Puede crear la cadena de composición llamando a la [**función ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) con el valor \_ SETSTR de SCS.                                                      |
| SCS \_ CAP \_ MAKEREAD           | Puede crear la cadena de lectura a partir de la cadena de composición correspondiente cuando se usa la función [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) con SCS SETSTR y sin \_ establecer *lpRead*. |
| SCS \_ CAP \_ SETRECONVERTSTRING | Este IME puede admitir la reconversión. Use [**ImmSetCompositionString para**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) realizar la reconversión.                                                                             |



 

Si *wParam* es IGP \_ SELECT, devuelve uno o varios de los valores siguientes.



| Requisito | Value |
|-----------------------|------------------------------------------------------|
| SELECCIÓN \_ DE CAP \_ CONVMODE | Hereda el modo de conversión cuando se selecciona un nuevo IME. |
| SELECCIÓN DE \_ LA FRASE \_ DE LÍMITE | Hereda el modo de oración cuando se selecciona un nuevo IME.   |



 

Si *wParam es* IGP \_ GETIMEVERSION, devuelve uno o varios de los valores siguientes.



| Requisito | Value |
|--------------|---------------------------------------------|
| IMEVER \_ 0310 | El IME se creó para Windows 3.1.        |
| IMEVER \_ 0400 | El IME se creó para Windows 95 o posterior |



 

Este mensaje es similar a [**ImmGetProperty,**](/windows/desktop/api/imm/nf-imm-immgetproperty)salvo que usa la configuración regional de entrada actual. La aplicación debe llamar a [**EM \_ ISIME antes**](em-isime.md) de llamar a esta función.

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

[**EM \_ ISIME**](em-isime.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty)
</dt> </dl>

 

