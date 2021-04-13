---
title: Mensaje EM_STREAMIN (RichEdit. h)
description: Reemplaza el contenido de un control Rich Edit por un flujo de datos proporcionado por una aplicación definida \ 8211; Función de devolución de llamada EditStreamCallback.
ms.assetid: b8d3a108-b415-4f5e-99e7-0e0e7a82a778
keywords:
- EM_STREAMIN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_STREAMIN
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40fdcf844cce09cf5c49085a9fcf08a38ad988ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492167"
---
# <a name="em_streamin-message"></a>\_Mensaje de secuencia em

Reemplaza el contenido de un control Rich Edit por un flujo de datos proporcionado por una función de devolución de llamada [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definida por la aplicación.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el formato de datos y las opciones de reemplazo. Este valor debe ser uno de los valores siguientes.



| Value                                                                                                                                       | Significado         |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <dt>**RTF de SF \_**</dt> </dl>    | RTF<br/>  |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <dt>**\_texto SF**</dt> </dl> | Texto<br/> |



 

Además, puede especificar las marcas siguientes.



| Value                                                                                                                                                         | Significado                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <dt>**SFF \_ PLAINRTF**</dt> </dl>    | Si se especifica, solo se transmiten en secuencias las palabras clave comunes a todos los lenguajes. Se omiten las palabras clave RTF específicas del lenguaje en la secuencia. Si no se especifica, todas las palabras clave se transmiten en. Puede combinar esta marca con la marca **de \_ RTF de SF** .<br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <dt>**selección de SFF \_**</dt> </dl> | Si se especifica, el flujo de datos reemplaza el contenido de la selección actual. Si no se especifica, el flujo de datos reemplaza todo el contenido del control. Puede combinar esta marca con el **\_ texto SF** o las marcas de **\_ RTF de SF** .<br/>  |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <dt>**SF \_ UNIcode**</dt> </dl>          | **Microsoft Rich Edit 2,0 y versiones posteriores:** Indica texto Unicode. Puede combinar esta marca con la marca **de \_ texto SF** . <br/>                                                                                                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) . En la entrada, el miembro **pfnCallback** de esta estructura debe apuntar a una función [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definida por la aplicación. En la salida, el miembro **dwError** puede contener un código de error distinto de cero si se produce un error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve el número de caracteres leídos.

## <a name="remarks"></a>Observaciones

Cuando se envía un mensaje de **\_ secuencia em** , el control Rich Edit realiza llamadas repetidas a la función [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) especificada por el miembro **pfnCallback** de la estructura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) . Cada vez que se llama a la función de devolución de llamada, rellena un búfer con los datos que se van a leer en el control. Esto continúa hasta que la función de devolución de llamada indica que se ha completado la operación de transmisión por secuencias o se ha producido un error.

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

[**\_STREAMOUT em**](em-streamout.md)
</dt> </dl>

 

 





