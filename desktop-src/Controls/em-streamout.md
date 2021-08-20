---
title: EM_STREAMOUT mensaje (Richedit.h)
description: Hace que un control de edición enriquecido pase su contenido a una aplicación \ 8211; función de devolución de llamada EditStreamCallback definida. A continuación, la función de devolución de llamada puede escribir el flujo de datos en un archivo o en cualquier otra ubicación que elija.
ms.assetid: 3f14aaac-4b17-47af-8f2b-503390631a88
keywords:
- EM_STREAMOUT controles de Windows mensaje
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
ms.openlocfilehash: 63236083c1964d29cb915e4bfc51303b30b730e01f76f2b186cc200d1dcfce6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019473"
---
# <a name="em_streamout-message"></a>Mensaje \_ DE EM STREAMOUT

Hace que un control de edición enriquecido pase su contenido a una función de devolución de llamada [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definida por la aplicación. A continuación, la función de devolución de llamada puede escribir el flujo de datos en un archivo o en cualquier otra ubicación que elija.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el formato de datos y las opciones de reemplazo.

Este valor debe ser uno de los siguientes valores.



| Value                                                                                                                                                      | Significado                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <dt>**SF \_ RTF**</dt> </dl>                   | Rtf.<br/>                                            |
| <span id="SF_RTFNOOBJS"></span><span id="sf_rtfnoobjs"></span><dl> <dt>**SF \_ RTFNOOBJS**</dt> </dl> | RTF con espacios en lugar de objetos COM.<br/>        |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <dt>**SF \_ TEXT**</dt> </dl>                | Texto con espacios en lugar de objetos COM.<br/>       |
| <span id="SF_TEXTIZED"></span><span id="sf_textized"></span><dl> <dt>**SF \_ TEXTIZED**</dt> </dl>    | Texto con una representación de texto de objetos COM.<br/> |



 

La **opción SF \_ RTFNOOBJS** es útil si una aplicación almacena los propios objetos COM, ya que la representación RTF de los objetos COM no es muy compacta. La palabra de \\ control, objattph, seguida de un espacio denota la posición del objeto.

Además, puede especificar las marcas siguientes.



| Value                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <dt>**SFF \_ PLAINRTF**</dt> </dl>       | Si se especifica, el control rich edit solo transmite las palabras clave comunes a todos los lenguajes, omitiendo las palabras clave específicas del lenguaje. Si no se especifica, el control rich edit transmite todas las palabras clave. Puede combinar esta marca con la marca **SF \_ RTF** o **SF \_ RTFNOOBJS.**<br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <dt>**SELECCIÓN DE \_ SFF**</dt> </dl>    | Si se especifica, el control rich edit solo transmite el contenido de la selección actual. Si no se especifica, el control transmite todo el contenido. Puede combinar esta marca con cualquiera de los valores de formato de datos.<br/>                                                        |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <dt>**SF \_ UNICODE**</dt> </dl>             | **Microsoft Rich Edit 2.0 y versiones posteriores:** Indica texto Unicode. Puede combinar esta marca con la **marca SF \_ TEXT.**<br/>                                                                                                                                                        |
| <span id="SF_USECODEPAGE"></span><span id="sf_usecodepage"></span><dl> <dt>**SF \_ USECODEPAGE**</dt> </dl> | **Rich Edit 3.0 y versiones posteriores:** Genera UTF-8 RTF, así como texto mediante otras páginas de códigos. La página de códigos se establece en la palabra alta *de wParam*. Por ejemplo, para UTF-8 RTF, establezca *wParam* en (CP \_ UTF8 << 16) \| SF \_ USECODEPAGE \| SF \_ RTF.<br/>                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura EDITSTREAM.**](/windows/desktop/api/Richedit/ns-richedit-editstream) En la entrada, el **miembro pfnCallback** de esta estructura debe apuntar a una [*función EditStreamCallback definida por la*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) aplicación. En la salida, el **miembro dwError** puede contener un código de error distinto de cero si se produjo un error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve el número de caracteres escritos en el flujo de datos.

## <a name="remarks"></a>Comentarios

Cuando se envía un mensaje **EM \_ STREAMOUT,** el control de edición enriquecido realiza llamadas repetidas a la [*función EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) especificada por el **miembro pfnCallback** de la [**estructura EDITSTREAM.**](/windows/desktop/api/Richedit/ns-richedit-editstream) Cada vez que llama a la función de devolución de llamada, el control pasa un búfer que contiene una parte del contenido del control. Este proceso continúa hasta que el control ha pasado todo su contenido a la función de devolución de llamada o hasta que se produce un error.

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

[**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[**EM \_ STREAMIN**](em-streamin.md)
</dt> </dl>

 

 





