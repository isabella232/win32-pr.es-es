---
description: La función DocumentEvent es un controlador de eventos para los eventos asociados a la impresión de un documento.
ms.assetid: 1250116e-55c7-470f-97f6-36f27a31a841
title: Función DocumentEvent (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DocumentEvent
- DocumentEventA
- DocumentEventW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: aa80e5fe17047eceacdc30e2a40a4a629088d89f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545371"
---
# <a name="documentevent-function"></a>DocumentEvent función)

La función **DocumentEvent** es un controlador de eventos para los eventos asociados a la impresión de un documento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DocumentEvent(
  _In_  HANDLE hPrinter,
  _In_  HDC    hdc,
        INT    iEsc,
        ULONG  cbIn,
  _In_  PVOID  pvIn,
        ULONG  cbOut,
  _Out_ PVOID  pvOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ de\]
</dt> <dd>

Identificador de un objeto de impresora. Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*HDC* \[ de\]
</dt> <dd>

Identificador de contexto de dispositivo que se genera mediante una llamada de [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca). Es cero si *iEsc* está establecido en DOCUMENTEVENT \_ CREATEDCPRE. Para obtener restricciones en la impresión desde una aplicación de 32 bits en una versión de Windows de 64 bits, consulte la sección Comentarios.

</dd> <dt>

*iEsc* 
</dt> <dd>

Código de escape que identifica el evento que se va a controlar. Este parámetro puede ser una de las constantes de tipo entero siguientes.



| Constante                                                                                                                                                                                                                                                                                                                                               | Evento                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_ABORTDOC"></span><span id="documentevent_abortdoc"></span><dl> <dt>**DOCUMENTEVENT \_ ABORTDOC**</dt> </dl>                                                                                                                                                               | GDI está a punto de procesar una llamada a su función [**AbortDoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc) .<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_CREATEDCPOST"></span><span id="documentevent_createdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPOST**</dt> </dl>                                                                                                                                                   | GDI acaba de procesar una llamada a su función [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) o [**CreateIC**](/windows/desktop/api/wingdi/nf-wingdi-createica) .<br/> Este código de escape no debe usarse a menos que haya una llamada anterior a **DocumentEvent** con *IESC* establecido en DocumentEvent \_ CREATEDCPRE.<br/>                                 |
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl>                                                                                                                                                      | GDI está a punto de procesar una llamada a su función [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) o [**CreateIC**](/windows/desktop/api/wingdi/nf-wingdi-createica) .<br/>                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_DELETEDC"></span><span id="documentevent_deletedc"></span><dl> <dt>**DOCUMENTEVENT \_ DELETEDC**</dt> </dl>                                                                                                                                                               | GDI está a punto de procesar una llamada a su función [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) .<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_ENDDOCPOST"></span><span id="documentevent_enddocpost"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPOST**</dt> </dl>                                                                                                                                                         | GDI acaba de procesar una llamada a su función [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) .<br/>                                                                                                                                                                                                                              |
| <span id="DOCUMENTEVENT_ENDDOCPRE_or_DOCUMENTEVENT_ENDDOC"></span><span id="documentevent_enddocpre_or_documentevent_enddoc"></span><span id="DOCUMENTEVENT_ENDDOCPRE_OR_DOCUMENTEVENT_ENDDOC"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPRE o DOCUMENTEVENT \_ ENDDOC**</dt> </dl>                 | GDI está a punto de procesar una llamada a su función [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) .<br/>                                                                                                                                                                                                                             |
| <span id="DOCUMENTEVENT_ENDPAGE"></span><span id="documentevent_endpage"></span><dl> <dt>**DOCUMENTEVENT \_ ENDPAGE**</dt> </dl>                                                                                                                                                                  | GDI está a punto de procesar una llamada a su función [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage) .<br/>                                                                                                                                                                                                                           |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**\_escape DOCUMENTEVENT**</dt> </dl>                                                                                                                                                                     | GDI está a punto de procesar una llamada a su función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .<br/>                                                                                                                                                                                                                       |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl>                                                                                                                                                      | El \_ evento DOCUMENTEVENT QUERYFILTER representa una oportunidad para que el administrador de trabajos de impresión consulte el controlador para obtener una lista de los eventos DOCUMENTEVENT \_ *XXX* a los que responderá el controlador. Este evento se emite justo antes de una llamada a **DocumentEvent** que pasa el \_ evento CREATEDCPRE de DocumentEvent.<br/> |
| <span id="DOCUMENTEVENT_RESETDCPOST"></span><span id="documentevent_resetdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPOST**</dt> </dl>                                                                                                                                                      | GDI acaba de procesar una llamada a su función [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) .<br/> Este código de escape no debe usarse a menos que haya una llamada anterior a **DocumentEvent** con *IESC* establecido en DocumentEvent \_ RESETDCPRE.<br/>                                                                    |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>                                                                                                                                                         | GDI está a punto de procesar una llamada a su función [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) .<br/>                                                                                                                                                                                                                           |
| <span id="DOCUMENTEVENT_STARTDOCPOST"></span><span id="documentevent_startdocpost"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPOST**</dt> </dl>                                                                                                                                                   | GDI acaba de procesar una llamada a su función [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_STARTDOCPRE_or_DOCUMENTEVENT_STARTDOC"></span><span id="documentevent_startdocpre_or_documentevent_startdoc"></span><span id="DOCUMENTEVENT_STARTDOCPRE_OR_DOCUMENTEVENT_STARTDOC"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPRE o DOCUMENTEVENT \_ STARTDOC**</dt> </dl> | GDI está a punto de procesar una llamada a su función [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_STARTPAGE"></span><span id="documentevent_startpage"></span><dl> <dt>**DOCUMENTEVENT \_ STARTPAGE**</dt> </dl>                                                                                                                                                            | GDI está a punto de procesar una llamada a su función [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) .<br/>                                                                                                                                                                                                                       |



 

</dd> <dt>

*cbIn* 
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *pvIn*.

</dd> <dt>

*pvIn* \[ de\]
</dt> <dd>

Puntero a un búfer. El búfer que contiene depende del valor de *iEsc*, como se muestra en la tabla siguiente.



| Constante                                                                                                                                                                                                                                                                                                                                               | Contenido de pvin                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_ABORTDOC"></span><span id="documentevent_abortdoc"></span><dl> <dt>**DOCUMENTEVENT \_ ABORTDOC**</dt> </dl>                                                                                                                                                               | No se utiliza.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_CREATEDCPOST"></span><span id="documentevent_createdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPOST**</dt> </dl>                                                                                                                                                   | *pvIn* contiene la dirección de un puntero a la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) especificada en el parámetro *pvOut* en una llamada anterior a esta función, para la que el parámetro *iEsc* se estableció en DOCUMENTEVENT \_ CREATEDCPRE.<br/> |
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl>                                                                                                                                                      | *pvIn* apunta a una \_ estructura DOCEVENT CREATEDCPRE que se documenta en el [Kit de desarrollo de controladores de Windows](https://msdn.microsoft.com/windows/hardware/gg487428).<br/>                                                                   |
| <span id="DOCUMENTEVENT_DELETEDC"></span><span id="documentevent_deletedc"></span><dl> <dt>**DOCUMENTEVENT \_ DELETEDC**</dt> </dl>                                                                                                                                                               | No se utiliza.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDDOCPOST"></span><span id="documentevent_enddocpost"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPOST**</dt> </dl>                                                                                                                                                         | No se utiliza.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDDOCPRE_or_DOCUMENTEVENT_ENDDOC"></span><span id="documentevent_enddocpre_or_documentevent_enddoc"></span><span id="DOCUMENTEVENT_ENDDOCPRE_OR_DOCUMENTEVENT_ENDDOC"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPRE o DOCUMENTEVENT \_ ENDDOC**</dt> </dl>                 | No se utiliza.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDPAGE"></span><span id="documentevent_endpage"></span><dl> <dt>**DOCUMENTEVENT \_ ENDPAGE**</dt> </dl>                                                                                                                                                                  | No se utiliza.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**\_escape DOCUMENTEVENT**</dt> </dl>                                                                                                                                                                     | *pvIn* apunta a una \_ estructura de escape DOCEVENT que está documentada en el [Kit de desarrollo de controladores de Windows](https://msdn.microsoft.com/windows/hardware/gg487428).<br/>                                                                        |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl>                                                                                                                                                      | Igual que para DOCUMENTEVENT \_ CREATEDCPRE.<br/>                                                                                                                                                                                            |
| <span id="DOCUMENTEVENT_RESETDCPOST"></span><span id="documentevent_resetdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPOST**</dt> </dl>                                                                                                                                                      | *pvIn* contiene la dirección de un puntero a la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) especificada en el parámetro *pvOut* en una llamada anterior a esta función, para la que el parámetro *iEsc* se estableció en DOCUMENTEVENT \_ RESETDCPRE.<br/>  |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>                                                                                                                                                         | *pvIn* contiene la dirección de un puntero a la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) proporcionada por el autor de la llamada de [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca).<br/>                                                                                         |
| <span id="DOCUMENTEVENT_STARTDOCPOST"></span><span id="documentevent_startdocpost"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPOST**</dt> </dl>                                                                                                                                                   | *pvIn* apunta a un valor de tipo Long que especifica el identificador del trabajo de impresión devuelto por [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).<br/>                                                                                                                          |
| <span id="DOCUMENTEVENT_STARTDOCPRE_or_DOCUMENTEVENT_STARTDOC"></span><span id="documentevent_startdocpre_or_documentevent_startdoc"></span><span id="DOCUMENTEVENT_STARTDOCPRE_OR_DOCUMENTEVENT_STARTDOC"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPRE o DOCUMENTEVENT \_ STARTDOC**</dt> </dl> | *pvIn* contiene la dirección de un puntero a una estructura [**DOCINFO**](/windows/desktop/api/Wingdi/ns-wingdi-docinfoa) proporcionada por el autor de la llamada de [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).<br/>                                                                                         |
| <span id="DOCUMENTEVENT_STARTPAGE"></span><span id="documentevent_startpage"></span><dl> <dt>**DOCUMENTEVENT \_ STARTPAGE**</dt> </dl>                                                                                                                                                            | No se utiliza.<br/>                                                                                                                                                                                                                          |



 

</dd> <dt>*cbOut*</dt> <dd> 

| Value                       | Significado                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------|
| IDOCUMENTEVENT \_ QUERYFILTER | Tamaño, en bytes, del puntero de búfer a por *pvOut*.                             |
| \_escape DOCUMENTEVENT       | Un valor que se usa como el parámetro *cbOutput* para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape). |
| Para todos los demás valores        | no se usa *iEsc* .                                                                  |



 

</dd> <dt>

*pvOut* \[ enuncia\]
</dt> <dd>

Puntero a un búfer. El contenido del búfer depende del valor proporcionado para *iEsc*, como se muestra en la tabla siguiente.



| Constante                                                                                                                                                                                          | Contenido de pvOut                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl> | Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) proporcionada por el controlador, que GDI utiliza en lugar de la proporcionada por el autor de la llamada [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) . (Si **es null**, GDI usa la estructura proporcionada por el autor de la llamada).<br/> |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**\_escape DOCUMENTEVENT**</dt> </dl>                | Un puntero a un búfer que se usa como el parámetro *lpszOutData* para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).<br/>                                                                                                              |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl> | Un puntero al búfer que contiene una \_ estructura de filtro DOCEVENT que se documenta en el [Kit de desarrollo de controladores de Windows](https://msdn.microsoft.com/windows/hardware/gg487428).<br/>                                          |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>    | Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) proporcionada por el controlador, que GDI utiliza en lugar de la proporcionada por el autor de la llamada [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) . (Si **es null**, GDI usa la estructura proporcionada por el autor de la llamada).<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto de la función depende del escape proporcionado para *iEsc*. En algunos códigos de escape, no se utiliza el valor devuelto (consulte a continuación). Si la función proporciona un valor devuelto, debe ser uno de los siguientes.



| Valor devuelto               | Significado                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| error de DOCUMENTEVENT \_     | El controlador admite el código de escape identificado por *iEsc*, pero se produjo un error. |
| DOCUMENTEVENT \_ correcto     | El controlador controló correctamente el código de escape identificado por *iEsc*.             |
| DOCUMENTEVENT \_ no compatible | El controlador no admite el código de escape identificado por *iEsc*.                 |



 

En la lista siguiente se indica qué códigos de escape requieren un valor devuelto y cuáles no, y se explica el significado de DOCUMENTEVENT \_ Success, DOCUMENTEVENT \_ Failure y DOCUMENTEVENT \_ devuelven códigos de retorno no compatibles.



| Valor devuelto                                          | Significado                                                                                                                                                                                    |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DOCUMENTEVENT \_ ABORTDOC                               | El valor devuelto no se utiliza y no se debe leer.                                                                                                                                       |
| DOCUMENTEVENT \_ CREATEDCPOST                           | El valor devuelto no se utiliza y no se debe leer.                                                                                                                                       |
| DOCUMENTEVENT \_ CREATEDCPRE                            | Error de DOCUMENTEVENT \_ : GDI no crea el contexto de información o el contexto de dispositivo, y proporciona un valor devuelto de 0 para [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) o [**CreateIC**](/windows/desktop/api/wingdi/nf-wingdi-createica). |
| DOCUMENTEVENT \_ DELETEDC                               | El valor devuelto no se utiliza y no se debe leer.                                                                                                                                       |
| DOCUMENTEVENT \_ ENDDOCPOST                             | El valor devuelto no se utiliza y no se debe leer.                                                                                                                                       |
| DOCUMENTEVENT \_ ENDDOCPRE o DOCUMENTEVENT \_ ENDDOC     | El valor devuelto no se utiliza y no se debe leer.                                                                                                                                       |
| DOCUMENTEVENT \_ ENDPAGE                                | El valor devuelto no se utiliza y no se debe leer.                                                                                                                                       |
| \_escape DOCUMENTEVENT                                 | El valor devuelto no se utiliza y no se debe leer.                                                                                                                                       |
| DOCUMENTEVENT \_ QUERYFILTER                            | Vea la sección Comentarios.                                                                                                                                                                               |
| DOCUMENTEVENT \_ RESETDCPOST                            | El valor devuelto no se utiliza y no se debe leer.                                                                                                                                       |
| DOCUMENTEVENT \_ RESETDCPRE                             | Error de DOCUMENTEVENT \_ : GDI no restablece el contexto de dispositivo y proporciona un valor devuelto de 0 para [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca).                                                           |
| DOCUMENTEVENT \_ STARTDOCPOST                           | \_Error de DOCUMENTEVENT: GDI llama a [**AbortDoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc) para detener el documento y, a continuación, proporciona un valor devuelto de error de SP \_ para [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).                      |
| DOCUMENTEVENT \_ STARTDOCPRE o DOCUMENTEVENT \_ STARTDOC | Error de DOCUMENTEVENT \_ : GDI no inicia el documento y proporciona un valor devuelto de error de SP \_ para [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).                                                       |
| DOCUMENTEVENT \_ STARTPAGE                              | Error de DOCUMENTEVENT \_ : GDI no inicia la página y proporciona un valor devuelto de error de SP \_ para [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage).                                                         |



 

## <a name="remarks"></a>Observaciones

En el caso de un valor *iEsc* de DOCUMENTEVENT \_ QUERYFILTER, el administrador de trabajos de impresión puede interpretar un \_ valor correcto de DOCUMENTEVENT que devuelve **DOCUMENTEVENT** de dos maneras, en función de si el controlador modificó determinados miembros de la estructura del \_ filtro DOCEVENT (que está documentado en el [Kit de desarrollo de controladores de Windows](https://msdn.microsoft.com/windows/hardware/gg487428) ). (El parámetro *pvOut* apunta a esta estructura). Cuando el administrador de trabajos de impresión asigna memoria para una estructura de este tipo, inicializa dos miembros de esta estructura, **cElementsReturned** y **cElementsNeeded**, en valores conocidos. Una vez que **DocumentEvent** devuelve, el administrador de trabajos de impresión determina si los valores de estos miembros han cambiado y utiliza esa información para interpretar el valor devuelto de **DocumentEvent** . En la tabla siguiente se resume esta situación.



| Valor devuelto                          | Estado de cElementsReturned y cElementsNeeded    | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DOCUMENTEVENT \_ correcto<br/>     | El controlador no ha realizado ningún cambio en ninguno de los miembros.<br/> | El administrador de trabajos de impresión interpreta este valor devuelto como equivalente a DOCUMENTEVENT \_ no compatible. El administrador de trabajos de impresión no puede recuperar el filtro de eventos del controlador, por lo que se mantiene en una llamada a **DocumentEvent** para todos los eventos.<br/>                                                                                                                                                                                                                         |
| DOCUMENTEVENT \_ correcto<br/>     | El controlador escribió en uno o ambos miembros.<br/>    | El administrador de trabajos de impresión acepta este valor devuelto sin interpretación. Si el controlador escribió solo en uno de **cElementsNeeded** y **cElementsReturned**, el administrador de trabajos de impresión considera que el miembro sin cambios tiene un valor de cero.<br/> El administrador de trabajos de impresión filtra todos los eventos enumerados en el miembro **aDocEventCall** del \_ filtro DOCEVENT (que está documentado en el [Kit de desarrollo de controladores de Windows](https://msdn.microsoft.com/windows/hardware/gg487428) ).<br/> |
| DOCUMENTEVENT \_ no compatible<br/> | No aplicable<br/>                          | El controlador no es compatible con DOCUMENTEVENT \_ QUERYFILTER.<br/> El administrador de trabajos de impresión no puede recuperar el filtro de eventos del controlador, por lo que se mantiene en una llamada a **DocumentEvent** para todos los eventos.<br/>                                                                                                                                                                                                                                            |
| error de DOCUMENTEVENT \_<br/>     | No aplicable<br/>                          | El controlador es compatible con DOCUMENTEVENT \_ QUERYFILTER, pero encontró un error interno.<br/> El administrador de trabajos de impresión no puede recuperar el filtro de eventos del controlador, por lo que se mantiene en una llamada a **DocumentEvent** para todos los eventos.<br/>                                                                                                                                                                                                                 |



 

Si el código de escape proporcionado en el parámetro *iEsc* es DOCUMENTEVENT \_ CREATEDCPRE, se aplican las siguientes reglas:

-   Si el trabajo se envía directamente a la impresora sin poner en cola, pvIn->pszDevice apunta al nombre de la impresora. (Para obtener más información, vea la documentación de DOCEVENT \_ . Estructura CREATEDCPRE en el [Kit de desarrollo de controladores de Windows](https://msdn.microsoft.com/windows/hardware/gg487428)).
-   Si el trabajo se está poniendo en cola, pvIn->pszDevice apunta al nombre del puerto de la impresora.

> [!Note]  
> Al ejecutar una aplicación de 32 bits en una versión de Windows de 64 bits, se aplican las siguientes restricciones. La única función GDI a la que debe llamar **DocumentEvent** es [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape), y solo se deben usar los escapes privados. Las llamadas a **DocumentEvent** a otras funciones GDI pueden producir un comportamiento indefinido.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DocumentEventW** (Unicode) y **DocumentEventA** (ANSI)<br/>                                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[Kit de desarrollo de controladores de Windows](https://msdn.microsoft.com/windows/hardware/gg487428)
</dt> </dl>

 

