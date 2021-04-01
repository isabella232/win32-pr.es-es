---
title: Mensaje EM_STREAMOUT (RichEdit. h)
description: Hace que un control Rich Edit pase su contenido a una función de devolución de llamada EditStreamCallback definida por la aplicación \ 8211;. La función de devolución de llamada puede escribir el flujo de datos en un archivo o en cualquier otra ubicación que elija.
ms.assetid: 3f14aaac-4b17-47af-8f2b-503390631a88
keywords:
- EM_STREAMOUT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_STREAMOUT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbdef51348593f8dbcfdb1ef579aca7dba6f96e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996433"
---
# <a name="em_streamout-message"></a>\_Mensaje STREAMOUT em

Hace que un control Rich Edit pase su contenido a una función de devolución de llamada [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definida por la aplicación. La función de devolución de llamada puede escribir el flujo de datos en un archivo o en cualquier otra ubicación que elija.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el formato de datos y las opciones de reemplazo.

Este valor debe ser uno de los valores siguientes.



| Value                                                                                                                                                      | Significado                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <dt>**RTF de SF \_**</dt> </dl>                   | RTF.<br/>                                            |
| <span id="SF_RTFNOOBJS"></span><span id="sf_rtfnoobjs"></span><dl> <dt>**\_RTFNOOBJS SF**</dt> </dl> | RTF con espacios en lugar de objetos COM.<br/>        |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <dt>**\_texto SF**</dt> </dl>                | Texto con espacios en lugar de objetos COM.<br/>       |
| <span id="SF_TEXTIZED"></span><span id="sf_textized"></span><dl> <dt>**SF con \_ texto**</dt> </dl>    | Texto con una representación de texto de los objetos COM.<br/> |



 

La **opción \_ RTFNOOBJS de SF** es útil si una aplicación almacena objetos com en sí, ya que la representación RTF de objetos com no es muy compacta. La palabra de control, \\ objattph, seguida de un espacio denota la posición del objeto.

Además, puede especificar las marcas siguientes.



| Value                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <dt>**SFF \_ PLAINRTF**</dt> </dl>       | Si se especifica, el control Rich Edit transmite solo las palabras clave comunes a todos los lenguajes, omitiendo las palabras clave específicas del idioma. Si no se especifica, el control Rich Edit transmite todas las palabras clave. Puede combinar esta marca con la marca **RTFNOOBJS \_ SF** o **SF \_** .<br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <dt>**selección de SFF \_**</dt> </dl>    | Si se especifica, el control Rich Edit transmite únicamente el contenido de la selección actual. Si no se especifica, el control transmite todo el contenido. Puede combinar esta marca con cualquiera de los valores de formato de datos.<br/>                                                        |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <dt>**SF \_ UNIcode**</dt> </dl>             | **Microsoft Rich Edit 2,0 y versiones posteriores:** Indica texto Unicode. Puede combinar esta marca con la marca **de \_ texto SF** .<br/>                                                                                                                                                        |
| <span id="SF_USECODEPAGE"></span><span id="sf_usecodepage"></span><dl> <dt>**el \_ USECODEPAGE de SF**</dt> </dl> | **Edición enriquecida 3,0 y versiones posteriores:** Genera RTF UTF-8 así como texto mediante otras páginas de códigos. La página de códigos se establece en la palabra alta de *wParam*. Por ejemplo, en el caso de RTF UTF-8, establezca *wParam* en (CP \_ UTF8 << 16) \| CF \_ USECODEPAGE \| SF \_ RTF.<br/>                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) . En la entrada, el miembro **pfnCallback** de esta estructura debe apuntar a una función [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definida por la aplicación. En la salida, el miembro **dwError** puede contener un código de error distinto de cero si se produce un error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve el número de caracteres escritos en el flujo de datos.

## <a name="remarks"></a>Observaciones

Cuando se envía un **mensaje \_ STREAMOUT em** , el control Rich Edit realiza llamadas repetidas a la función [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) especificada por el miembro **pfnCallback** de la estructura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) . Cada vez que llama a la función de devolución de llamada, el control pasa un búfer que contiene una parte del contenido del control. Este proceso continúa hasta que el control ha pasado todo su contenido a la función de devolución de llamada o hasta que se produce un error.

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

[**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[**\_secuencia em**](em-streamin.md)
</dt> </dl>

 

 





