---
description: La función DocumentEvent es un controlador de eventos para eventos asociados a la impresión de un documento.
ms.assetid: 1250116e-55c7-470f-97f6-36f27a31a841
title: Función DocumentEvent (Winspool.h)
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
ms.openlocfilehash: 0c38a95c4e0dc9820130e467c971c0adb5b9df0ede248506ed56f963c3246b3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971604"
---
# <a name="documentevent-function"></a>Función DocumentEvent

La **función DocumentEvent** es un controlador de eventos para eventos asociados a la impresión de un documento.

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

*hPrinter* \[ En\]
</dt> <dd>

Identificador de un objeto de impresora. Use la [**función OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*hdc* \[ En\]
</dt> <dd>

Identificador de contexto de dispositivo generado por una llamada de [**CreateDC.**](/windows/desktop/api/wingdi/nf-wingdi-createdca) Es cero si *iEsc* está establecido en DOCUMENTEVENT \_ CREATEDCPRE. Para ver las restricciones de impresión desde una aplicación de 32 bits en una versión de 64 bits de Windows, vea Comentarios.

</dd> <dt>

*iEsc* 
</dt> <dd>

Código de escape que identifica el evento que se va a controlar. Este parámetro puede ser una de las siguientes constantes de entero.



| Constante                                                                                                                                                                                                                                                                                                                                               | Evento                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_ABORTDOC"></span><span id="documentevent_abortdoc"></span><dl> <dt>**DOCUMENTEVENT \_ ABORTDOC**</dt> </dl>                                                                                                                                                               | GDI está a punto de procesar una llamada a su [**función AbortDoc.**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc)<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_CREATEDCPOST"></span><span id="documentevent_createdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPOST**</dt> </dl>                                                                                                                                                   | GDI acaba de procesar una llamada a su [**función CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) [**o CreateIC.**](/windows/desktop/api/wingdi/nf-wingdi-createica)<br/> Este código de escape no debe usarse a menos que haya habido una llamada anterior a **DocumentEvent** con *iEsc* establecido en DOCUMENTEVENT \_ CREATEDCPRE.<br/>                                 |
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl>                                                                                                                                                      | GDI está a punto de procesar una llamada a su [**función CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) [**o CreateIC.**](/windows/desktop/api/wingdi/nf-wingdi-createica)<br/>                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_DELETEDC"></span><span id="documentevent_deletedc"></span><dl> <dt>**DOCUMENTEVENT \_ DELETEDC**</dt> </dl>                                                                                                                                                               | GDI está a punto de procesar una llamada a su [**función DeleteDC.**](/windows/desktop/api/wingdi/nf-wingdi-deletedc)<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_ENDDOCPOST"></span><span id="documentevent_enddocpost"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPOST**</dt> </dl>                                                                                                                                                         | GDI acaba de procesar una llamada a su [**función EndDoc.**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)<br/>                                                                                                                                                                                                                              |
| <span id="DOCUMENTEVENT_ENDDOCPRE_or_DOCUMENTEVENT_ENDDOC"></span><span id="documentevent_enddocpre_or_documentevent_enddoc"></span><span id="DOCUMENTEVENT_ENDDOCPRE_OR_DOCUMENTEVENT_ENDDOC"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPRE o DOCUMENTEVENT \_ ENDDOC**</dt> </dl>                 | GDI está a punto de procesar una llamada a su [**función EndDoc.**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)<br/>                                                                                                                                                                                                                             |
| <span id="DOCUMENTEVENT_ENDPAGE"></span><span id="documentevent_endpage"></span><dl> <dt>**DOCUMENTEVENT \_ ENDPAGE**</dt> </dl>                                                                                                                                                                  | GDI está a punto de procesar una llamada a su [**función EndPage.**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)<br/>                                                                                                                                                                                                                           |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**ESCAPE \_ DE DOCUMENTEVENT**</dt> </dl>                                                                                                                                                                     | GDI está a punto de procesar una llamada a su [**función ExtEscape.**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)<br/>                                                                                                                                                                                                                       |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl>                                                                                                                                                      | El evento DOCUMENTEVENT QUERYFILTER representa una oportunidad para que el administrador de trabajos en cola consulte al controlador para obtener una lista de los eventos DOCUMENTEVENT XXX a los que \_ \_  responderá el controlador. Este evento se emite justo antes de una llamada a **DocumentEvent** que pasa el evento \_ DOCUMENTEVENT CREATEDCPRE.<br/> |
| <span id="DOCUMENTEVENT_RESETDCPOST"></span><span id="documentevent_resetdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPOST**</dt> </dl>                                                                                                                                                      | GDI acaba de procesar una llamada a su [**función ResetDC.**](/windows/desktop/api/wingdi/nf-wingdi-resetdca)<br/> Este código de escape no debe usarse a menos que haya habido una llamada anterior a **DocumentEvent** con *iEsc* establecido en DOCUMENTEVENT \_ RESETDCPRE.<br/>                                                                    |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>                                                                                                                                                         | GDI está a punto de procesar una llamada a su [**función ResetDC.**](/windows/desktop/api/wingdi/nf-wingdi-resetdca)<br/>                                                                                                                                                                                                                           |
| <span id="DOCUMENTEVENT_STARTDOCPOST"></span><span id="documentevent_startdocpost"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPOST**</dt> </dl>                                                                                                                                                   | GDI acaba de procesar una llamada a su [**función StartDoc.**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_STARTDOCPRE_or_DOCUMENTEVENT_STARTDOC"></span><span id="documentevent_startdocpre_or_documentevent_startdoc"></span><span id="DOCUMENTEVENT_STARTDOCPRE_OR_DOCUMENTEVENT_STARTDOC"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPRE o DOCUMENTEVENT \_ STARTDOC**</dt> </dl> | GDI está a punto de procesar una llamada a su [**función StartDoc.**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_STARTPAGE"></span><span id="documentevent_startpage"></span><dl> <dt>**DOCUMENTEVENT \_ STARTPAGE**</dt> </dl>                                                                                                                                                            | GDI está a punto de procesar una llamada a su [**función StartPage.**](/windows/desktop/api/Wingdi/nf-wingdi-startpage)<br/>                                                                                                                                                                                                                       |



 

</dd> <dt>

*cbIn* 
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *pvIn*.

</dd> <dt>

*pvIn* \[ En\]
</dt> <dd>

Puntero a un búfer. Lo que contiene el búfer depende del valor de *iEsc*, como se muestra en la tabla siguiente.



| Constante                                                                                                                                                                                                                                                                                                                                               | Contenido de pvin                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_ABORTDOC"></span><span id="documentevent_abortdoc"></span><dl> <dt>**DOCUMENTEVENT \_ ABORTDOC**</dt> </dl>                                                                                                                                                               | No se usa.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_CREATEDCPOST"></span><span id="documentevent_createdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPOST**</dt> </dl>                                                                                                                                                   | *pvIn* contiene la dirección de un puntero a la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) especificada en el parámetro *pvOut* en una llamada anterior a esta función, para la que el parámetro *iEsc* se estableció en DOCUMENTEVENT \_ CREATEDCPRE.<br/> |
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl>                                                                                                                                                      | *pvIn* apunta a una estructura CREATEDCPRE de DOCEVENT que se documenta en Windows \_ [Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428).<br/>                                                                   |
| <span id="DOCUMENTEVENT_DELETEDC"></span><span id="documentevent_deletedc"></span><dl> <dt>**DOCUMENTEVENT \_ DELETEDC**</dt> </dl>                                                                                                                                                               | No se usa.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDDOCPOST"></span><span id="documentevent_enddocpost"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPOST**</dt> </dl>                                                                                                                                                         | No se usa.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDDOCPRE_or_DOCUMENTEVENT_ENDDOC"></span><span id="documentevent_enddocpre_or_documentevent_enddoc"></span><span id="DOCUMENTEVENT_ENDDOCPRE_OR_DOCUMENTEVENT_ENDDOC"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPRE o DOCUMENTEVENT \_ ENDDOC**</dt> </dl>                 | No se usa.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDPAGE"></span><span id="documentevent_endpage"></span><dl> <dt>**DOCUMENTEVENT \_ ENDPAGE**</dt> </dl>                                                                                                                                                                  | No se usa.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**ESCAPE \_ DE DOCUMENTEVENT**</dt> </dl>                                                                                                                                                                     | *pvIn* apunta a una estructura ESCAPE DE DOCEVENT que se documenta en Windows \_ [Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428).<br/>                                                                        |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl>                                                                                                                                                      | Igual que para DOCUMENTEVENT \_ CREATEDCPRE.<br/>                                                                                                                                                                                            |
| <span id="DOCUMENTEVENT_RESETDCPOST"></span><span id="documentevent_resetdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPOST**</dt> </dl>                                                                                                                                                      | *pvIn* contiene la dirección de un puntero a la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) especificada en el parámetro *pvOut* en una llamada anterior a esta función, para la que el parámetro *iEsc* se estableció en DOCUMENTEVENT \_ RESETDCPRE.<br/>  |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>                                                                                                                                                         | *pvIn* contiene la dirección de un puntero a la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) proporcionada por el autor de la llamada de [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca).<br/>                                                                                         |
| <span id="DOCUMENTEVENT_STARTDOCPOST"></span><span id="documentevent_startdocpost"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPOST**</dt> </dl>                                                                                                                                                   | *pvIn* apunta a un valor LONG que especifica el identificador del trabajo de impresión devuelto por [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).<br/>                                                                                                                          |
| <span id="DOCUMENTEVENT_STARTDOCPRE_or_DOCUMENTEVENT_STARTDOC"></span><span id="documentevent_startdocpre_or_documentevent_startdoc"></span><span id="DOCUMENTEVENT_STARTDOCPRE_OR_DOCUMENTEVENT_STARTDOC"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPRE o DOCUMENTEVENT \_ STARTDOC**</dt> </dl> | *pvIn* contiene la dirección de un puntero a una [**estructura DOCINFO**](/windows/desktop/api/Wingdi/ns-wingdi-docinfoa) proporcionada por el autor de la llamada [**de StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).<br/>                                                                                         |
| <span id="DOCUMENTEVENT_STARTPAGE"></span><span id="documentevent_startpage"></span><dl> <dt>**DOCUMENTEVENT \_ STARTPAGE**</dt> </dl>                                                                                                                                                            | No se usa.<br/>                                                                                                                                                                                                                          |



 

</dd> <dt>*cbOut*</dt> <dd> 

| Valor                       | Significado                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------|
| IDOCUMENTEVENT \_ QUERYFILTER | Tamaño, en bytes, del puntero de búfer a por *pvOut*.                             |
| ESCAPE \_ DE DOCUMENTEVENT       | Valor que se usa como parámetro *cbOutput* para [**ExtEscape.**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) |
| Para todos los demás valores        | *No se usa iEsc.*                                                                  |



 

</dd> <dt>

*pvOut* \[ out\]
</dt> <dd>

Puntero a un búfer. El contenido del búfer depende del valor proporcionado para *iEsc*, como se muestra en la tabla siguiente.



| Constante                                                                                                                                                                                          | Contenido de pvOut                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl> | Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) proporcionada por el controlador, que GDI usa en lugar de la proporcionada por el autor de [**la llamada CreateDC.**](/windows/desktop/api/wingdi/nf-wingdi-createdca) (Si **es NULL,** GDI usa la estructura proporcionada por el autor de la llamada).<br/> |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**ESCAPE \_ DE DOCUMENTEVENT**</dt> </dl>                | Puntero a un búfer que se usa como parámetro *lpszOutData* para [**ExtEscape.**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)<br/>                                                                                                              |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl> | Puntero al búfer que contiene una estructura DOCEVENT FILTER que se documenta en Windows \_ [Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428).<br/>                                          |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>    | Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) proporcionada por el controlador, que GDI usa en lugar de la proporcionada por el autor de la llamada [**ResetDC.**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) (Si **es NULL,** GDI usa la estructura proporcionada por el autor de la llamada).<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto de la función depende del escape proporcionado para *iEsc*. Para algunos códigos de escape, no se usa el valor devuelto (consulte a continuación). Si la función proporciona un valor devuelto, debe ser uno de los siguientes.



| Valor devuelto               | Significado                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| ERROR DE \_ DOCUMENTEVENT     | El controlador admite el código de escape identificado por *iEsc*, pero se produjo un error. |
| DOCUMENTEVENT \_ SUCCESS     | El controlador controló correctamente el código de escape identificado por *iEsc*.             |
| DOCUMENTEVENT \_ NO COMPATIBLE | El controlador no admite el código de escape identificado por *iEsc*.                 |



 

En la lista siguiente se indica qué códigos de escape requieren un valor devuelto y cuáles no, y se explica el significado de los códigos de retorno DOCUMENTEVENT \_ SUCCESS, DOCUMENTEVENT FAILURE y \_ DOCUMENTEVENT \_ UNSUPPORTED.



| Valor devuelto                                          | Significado                                                                                                                                                                                    |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DOCUMENTEVENT \_ ABORTDOC                               | No se usa el valor devuelto y no se debe leer.                                                                                                                                       |
| DOCUMENTEVENT \_ CREATEDCPOST                           | No se usa el valor devuelto y no se debe leer.                                                                                                                                       |
| DOCUMENTEVENT \_ CREATEDCPRE                            | ERROR DE DOCUMENTEVENT: GDI no crea el contexto de dispositivo ni el contexto de información y proporciona un valor devuelto de 0 para \_ [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) [**o CreateIC.**](/windows/desktop/api/wingdi/nf-wingdi-createica) |
| DOCUMENTEVENT \_ DELETEDC                               | No se usa el valor devuelto y no se debe leer.                                                                                                                                       |
| DOCUMENTEVENT \_ ENDDOCPOST                             | No se usa el valor devuelto y no se debe leer.                                                                                                                                       |
| DOCUMENTEVENT \_ ENDDOCPRE o DOCUMENTEVENT \_ ENDDOC     | No se usa el valor devuelto y no se debe leer.                                                                                                                                       |
| DOCUMENTEVENT \_ ENDPAGE                                | No se usa el valor devuelto y no se debe leer.                                                                                                                                       |
| ESCAPE \_ DE DOCUMENTEVENT                                 | No se usa el valor devuelto y no se debe leer.                                                                                                                                       |
| DOCUMENTEVENT \_ QUERYFILTER                            | Vea la sección Comentarios.                                                                                                                                                                               |
| DOCUMENTEVENT \_ RESETDCPOST                            | No se usa el valor devuelto y no se debe leer.                                                                                                                                       |
| DOCUMENTEVENT \_ RESETDCPRE                             | ERROR DE DOCUMENTEVENT: GDI no restablece el contexto del dispositivo y proporciona un valor devuelto \_ de 0 para [**ResetDC.**](/windows/desktop/api/wingdi/nf-wingdi-resetdca)                                                           |
| DOCUMENTEVENT \_ STARTDOCPOST                           | ERROR DE \_ DOCUMENTEVENT: GDI llama a [**AbortDoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc) para detener el documento y, a continuación, proporciona un valor devuelto de \_ SP ERROR para [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).                      |
| DOCUMENTEVENT \_ STARTDOCPRE o DOCUMENTEVENT \_ STARTDOC | ERROR DE DOCUMENTEVENT: GDI no inicia el documento y proporciona un valor devuelto de \_ \_ SP ERROR para [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).                                                       |
| DOCUMENTEVENT \_ STARTPAGE                              | ERROR DE DOCUMENTEVENT: GDI no inicia la página y proporciona un valor devuelto de \_ SP \_ ERROR para [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage).                                                         |



 

## <a name="remarks"></a>Comentarios

Para un valor *iEsc* de DOCUMENTEVENT QUERYFILTER, el administrador de trabajos en cola puede interpretar un valor DE DOCUMENTEVENT SUCCESS devuelto por DocumentEvent de dos maneras, dependiendo de si el controlador modificó determinados miembros de la estructura \_ \_ DOCEVENT FILTER  \_ (que [](https://msdn.microsoft.com/windows/hardware/gg487428) se documenta en el Kit de desarrollo de controladores de Windows ). (El *parámetro pvOut* apunta a esta estructura). Cuando el colador asigna memoria para una estructura de este tipo, inicializa dos miembros de esta estructura, **cElementsReturned** y **cElementsNeeded,** en valores conocidos. Una **vez que se devuelve DocumentEvent,** el colador determina si los valores de estos miembros han cambiado y usa esa información para interpretar el valor devuelto de **DocumentEvent.** En la tabla siguiente se resume esta situación.



| Valor devuelto                          | Estado de cElementsReturned y cElementsNeeded    | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DOCUMENTEVENT \_ SUCCESS<br/>     | El controlador no ha realizado ningún cambio en ninguno de los miembros.<br/> | El administrador de trabajos de cola interpreta este valor devuelto como equivalente a DOCUMENTEVENT \_ UNSUPPORTED. El administrador de trabajos en cola no puede recuperar el filtro de eventos del controlador, por lo que se conserva al llamar a **DocumentEvent** para todos los eventos.<br/>                                                                                                                                                                                                                         |
| DOCUMENTEVENT \_ SUCCESS<br/>     | El controlador escribió en uno o ambos miembros.<br/>    | El colador acepta este valor devuelto sin interpretación. Si el controlador escribió solo en uno de **los cElementsNeeded** y **cElementsReturned,** el administrador de trabajos en cola considera que el miembro sin cambios tiene un valor de cero.<br/> El administrador de trabajos de cola filtra todos los eventos enumerados en el miembro **aDocEventCall** de DOCEVENT FILTER (que se documenta en Windows \_ Driver Development [Kit](https://msdn.microsoft.com/windows/hardware/gg487428) ).<br/> |
| DOCUMENTEVENT \_ NO COMPATIBLE<br/> | No aplicable<br/>                          | El controlador no admite DOCUMENTEVENT \_ QUERYFILTER.<br/> El administrador de trabajos en cola no puede recuperar el filtro de eventos del controlador, por lo que se conserva al llamar a **DocumentEvent** para todos los eventos.<br/>                                                                                                                                                                                                                                            |
| ERROR DE \_ DOCUMENTEVENT<br/>     | No aplicable<br/>                          | El controlador admite DOCUMENTEVENT \_ QUERYFILTER, pero encontró un error interno.<br/> El administrador de trabajos en cola no puede recuperar el filtro de eventos del controlador, por lo que se conserva al llamar a **DocumentEvent** para todos los eventos.<br/>                                                                                                                                                                                                                 |



 

Si el código de escape proporcionado en el *parámetro iEsc* es DOCUMENTEVENT \_ CREATEDCPRE, se aplican las reglas siguientes:

-   Si el trabajo se envía directamente a la impresora sin cola, pvIn->pszDevice apunta al nombre de la impresora. (Para más información, consulte la documentación de DOCEVENT. \_ Estructura CREATEDCPRE en el [kit de Windows Driver Development Kit).](https://msdn.microsoft.com/windows/hardware/gg487428)
-   Si el trabajo se está colando, pvIn->pszDevice apunta al nombre del puerto de impresora.

> [!Note]  
> Las restricciones siguientes se aplican al ejecutar una aplicación de 32 bits en una versión de 64 bits de Windows. La única función GDI a la **que DocumentEvent** debe llamar es [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)y solo se deben usar escapes privados. **Las llamadas de DocumentEvent** a otras funciones GDI pueden producir un comportamiento indefinido.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DocumentEventW** (Unicode) y **DocumentEventA** (ANSI)<br/>                                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[Windows Kit de desarrollo de controladores](https://msdn.microsoft.com/windows/hardware/gg487428)
</dt> </dl>

 

