---
title: Mensaje EM_GETIMEPROPERTY (RichEdit. h)
description: Recupera la propiedad y las capacidades del editor de métodos de entrada (IME) asociado a la configuración regional de entrada actual.
ms.assetid: 0cbe52d4-c3e7-40bd-a6f6-da0a11056976
keywords:
- EM_GETIMEPROPERTY controles de mensajes de Windows
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
ms.openlocfilehash: 94c081aa99c99f4cd0995c0f9d2f5256e2958dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150767"
---
# <a name="em_getimeproperty-message"></a>\_Mensaje GETIMEPROPERTY em

Recupera la propiedad y las capacidades del editor de métodos de entrada (IME) asociado a la configuración regional de entrada actual.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el tipo de información de propiedad que se va a recuperar. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                     | Significado                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="IGP_PROPERTY"></span><span id="igp_property"></span><dl> <dt>**IGP \_ (propiedad)**</dt> </dl>                | Información de la propiedad.<br/>                                                         |
| <span id="IGP_CONVERSION"></span><span id="igp_conversion"></span><dl> <dt>**conversión de IGP \_**</dt> </dl>          | Capacidades de conversión. <br/>                                                     |
| <span id="IGP_SENTENCE"></span><span id="igp_sentence"></span><dl> <dt>**\_frase IGP**</dt> </dl>                | Capacidades del modo de oraciones. <br/>                                                  |
| <span id="IGP_UI"></span><span id="igp_ui"></span><dl> <dt>**interfaz de usuario de IGP \_**</dt> </dl>                                  | Capacidades de la interfaz de usuario. <br/>                                                 |
| <span id="IGP_SETCOMPSTR"></span><span id="igp_setcompstr"></span><dl> <dt>**IGP \_ SETCOMPSTR**</dt> </dl>          | Capacidades de la cadena de composición. <br/>                                             |
| <span id="IGP_SELECT"></span><span id="igp_select"></span><dl> <dt>**selección de IGP \_**</dt> </dl>                      | Funcionalidades de herencia de selección. <br/>                                          |
| <span id="IGP_GETIMEVERSION"></span><span id="igp_getimeversion"></span><dl> <dt>**IGP \_ GETIMEVERSION**</dt> </dl> | Recupera el número de versión del sistema para el que se creó el IME especificado. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de la propiedad o de la capacidad, dependiendo del valor del parámetro *lParam* . Para obtener más información, vea la sección Notas.

## <a name="remarks"></a>Observaciones

Si *wParam* es \_ la propiedad IGP, devuelve uno o varios de los valores siguientes.



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_prop IME \_ en el \_ símbolo de intercalación                | Si se establece, la ventana de conversión se encuentra en la posición del símbolo de intercalación. Si está desactivada, la ventana está cerca de la posición del símbolo de intercalación.                                                                                                                                                                  |
| \_interfaz de \_ usuario especial de prop de IME \_              | Si se establece, IME tiene una interfaz de usuario no estándar. La aplicación no debe dibujarse en la ventana del IME.                                                                                                                                                                  |
| \_CANDLIST prop \_ IME \_ Start \_ from \_ 1 | Si se establece, las cadenas de la lista de candidatos se numeran a partir de 1. Si está desactivada, las cadenas comienzan por cero.                                                                                                                                                                |
| PROP de IME \_ \_ Unicode                  | Si se establece, el IME se ve como UnicodeIME. El sistema y el IME se comunicarán a través de la interfaz UnicodeIME. Si está claro, IME usará la interfaz ANSI para comunicarse con el sistema.                                                                    |
| \_prop. \_ de IME completada \_ en \_ anulación de selección   | Si se establece, la ventana de conversión se encuentra en la posición del símbolo de intercalación. Si está desactivada, la ventana está cerca de la posición del símbolo de intercalación.                                                                                                                                                                  |
| PROP de IME \_ \_ Accept \_ \_ VKEY Wide       | Si se establece, el IME procesa el Unicode insertado que proviene de la función [**SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) mediante el \_ paquete VK. Si está desactivada, es posible que el IME no procese el Unicode insertado y que el Unicode insertado se envíe directamente a la aplicación. |



 

Si *wParam* es \_ la interfaz de usuario de IGP, devuelve uno o varios de los valores siguientes.



| Requisito | Value |
|-----------------|-------------------------------------------------------------------------------------------------------|
| Cap de UI \_ \_ 2700   | Admite valores de escape de texto de 0 o 2700. Para obtener más información, vea **lfEscapement**.             |
| \_ROT90 de Cap de IU \_  | Admite valores de escape de texto de 0, 900, 1800 o 2700. Para obtener más información, vea **lfEscapement**. |
| \_ROTANY de Cap de IU \_ | Admite cualquier valor de escape de texto. Para obtener más información, vea **lfEscapement**.                       |



 

Si *wParam* es IGP \_ SETCOMPSTR, devuelve uno o varios de los valores siguientes.



| Requisito | Value |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cap de SCS \_ \_ COMPSTR            | Puede crear la cadena de composición mediante una llamada a la función [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) con el \_ valor SETSTR de SCS.                                                      |
| Cap de SCS \_ \_ MAKEREAD           | Puede crear la cadena de lectura a partir de la cadena de composición correspondiente al usar la función [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) con SCS \_ SETSTR y sin establecer *lpRead*. |
| Cap de SCS \_ \_ SETRECONVERTSTRING | Este IME puede admitir la reconversión. Use [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) para realizar la conversión.                                                                             |



 

Si *wParam* es \_ la selección de IGP, devuelve uno o varios de los valores siguientes.



| Requisito | Value |
|-----------------------|------------------------------------------------------|
| SELECCIONAR \_ Cap \_ CONVMODE | Hereda el modo de conversión cuando se selecciona un nuevo IME. |
| SELECCIONAR \_ frase de extremo \_ | Hereda el modo de oración cuando se selecciona un nuevo IME.   |



 

Si *wParam* es IGP \_ GETIMEVERSION, devuelve uno o varios de los valores siguientes.



| Requisito | Value |
|--------------|---------------------------------------------|
| \_0310 | Se creó el IME para Windows 3,1.        |
| \_0400 | Se creó el IME para Windows 95 o posterior. |



 

Este mensaje es similar a [**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty), con la excepción de que usa la configuración regional de entrada actual. La aplicación debe llamar a [**em \_ ISIME**](em-isime.md) antes de llamar a esta función.

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

[**\_ISIME em**](em-isime.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty)
</dt> </dl>

 

