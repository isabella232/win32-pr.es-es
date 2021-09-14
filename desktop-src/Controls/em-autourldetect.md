---
title: EM_AUTOURLDETECT mensaje (Richedit.h)
description: Habilita o deshabilita la detección automática de hipervínculos mediante un control de edición enriquecido.
ms.assetid: 6970ff36-ff3f-4413-a471-9389a76c8f38
keywords:
- EM_AUTOURLDETECT controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_AUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc8f76b89e5e8aa529084b5c8c0898200e28ed2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246914"
---
# <a name="em_autourldetect-message"></a>Mensaje EM \_ AUTOURLDETECT

Habilita o deshabilita la detección automática de hipervínculos mediante un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifique 0 para deshabilitar la detección automática de vínculos o uno de los siguientes valores para habilitar varios tipos de detección.



| Value                                                                                                                                                                                       | Significado                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AURL_DISABLEMIXEDLGC"></span><span id="aurl_disablemixedlgc"></span><dl> <dt>**AURL \_ DISABLEMIXEDLGC**</dt> </dl>          | **Windows 8:** deshabilite el reconocimiento de nombres de dominio que contienen etiquetas con caracteres que pertenecen a más de uno de los scripts siguientes: latino, griego y cirílico. <br/> |
| <span id="AURL_ENABLEDRIVELETTERS"></span><span id="aurl_enabledriveletters"></span><dl> <dt>**AURL \_ ENABLEDRIVELETTERS**</dt> </dl> | **Windows 8:** reconocer los nombres de archivo que tienen una especificación de unidad inicial, como c: \\ temp.<br/>                                                                           |
| <span id="AURL_ENABLEEA"></span><span id="aurl_enableea"></span><dl> <dt>**AURL \_ ENABLEEA**</dt> </dl>                               | Este valor está en desuso; use **AURL \_ ENABLEEAURLS en** su lugar.<br/>                                                                                                            |
| <span id="AURL_ENABLEEAURLS"></span><span id="aurl_enableeaurls"></span><dl> <dt>**AURL \_ ENABLEEAURLS**</dt> </dl>                   | Reconocer direcciones URL que contienen caracteres de Este de Asia. <br/>                                                                                                                      |
| <span id="AURL_ENABLEEMAILADDR"></span><span id="aurl_enableemailaddr"></span><dl> <dt>**AURL \_ ENABLEEMAILADDR**</dt> </dl>          | **Windows 8:** reconocer direcciones de correo electrónico.<br/>                                                                                                                                |
| <span id="AURL_ENABLETELNO"></span><span id="aurl_enabletelno"></span><dl> <dt>**AURL \_ ENABLETELNO**</dt> </dl>                      | **Windows 8:** reconocer números de teléfono.<br/>                                                                                                                              |
| <span id="AURL_ENABLEURL"></span><span id="aurl_enableurl"></span><dl> <dt>**AURL \_ ENABLEURL**</dt> </dl>                            | **Windows 8:** reconocer direcciones URL que incluyen la ruta de acceso.<br/>                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro determina los esquemas de dirección URL reconocidos si **AURL \_ ENABLEURL** está activo. Si *lParam es* NULL, se usa la lista de nombres de esquema predeterminada (vea Comentarios). Como alternativa, *lParam* puede apuntar a una cadena terminada en NULL que consta de hasta 50 nombres de esquema terminados en dos puntos que reemplazan a la lista de nombres de esquema predeterminada. Por ejemplo, la cadena podría ser "news:http:ftp:telnet:". La sintaxis de nombre de esquema se define en el documento [Identificadores uniformes]( https://www.ietf.org/rfc/rfc2396.txt) de recursos (URI): Sintaxis genérica en el sitio web del Grupo de tareas de ingeniería de Internet (IETF). En concreto, un nombre de esquema puede contener hasta 13 caracteres (incluidos los dos puntos), debe comenzar con un alfabeto ASCII y puede ir seguido de una combinación de caracteres alfabéticos ASCII, dígitos y los tres caracteres de puntuación: ".", "+" y "-". El tipo de cadena puede ser **char _ o \* *_* WCHAR; \*** el control rich edit detecta automáticamente el tipo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es cero.

Si se produce un error en el mensaje, el valor devuelto es un valor distinto de cero. Por ejemplo, el mensaje podría producir un error debido a memoria insuficiente, una opción de detección no válida o una cadena de nombre de esquema no válida.

Si *lParam contiene* más de 50 nombres de esquema, se produce un error en el mensaje con un valor devuelto **de E \_ INVALIDARG**.

## <a name="remarks"></a>Observaciones

Si la detección automática de direcciones URL está habilitada (es decir, *wParam* incluye **AURL \_ ENABLEURL),** el control de edición enriquecte examina cualquier texto modificado para determinar si el texto coincide con el formato de una dirección URL (o más generalmente en Windows 8 o posterior un identificador de recursos internacional de IRI). Si *lParam* es NULL, el control detecta las direcciones URL que comienzan por los siguientes nombres de esquema:

-   callto
-   archivo
-   ftp
-   gopher
-   http
-   https
-   mailto
-   news
-   HDInsight
-   Nntp
-   onenote
-   Outlook
-   Prospero
-   tel
-   telnet
-   wais
-   webcal

Cuando se habilita la detección automática de vínculos, el control de edición enriquecía quita el efecto **CFE \_ LINK** del texto modificado que no tiene un formato reconocido por el control. Si la aplicación usa el **efecto CFE \_ LINK** para marcar otros tipos de texto, no habilite la detección automática de vínculos. El control rich edit no comprueba si existe un vínculo detectado. esa responsabilidad pertenece al cliente.

Un control de edición enriquecido envía la notificación [EN \_ LINK](en-link.md) cuando recibe varios mensajes mientras el puntero del mouse se encuentra sobre el texto que tiene el **efecto CFE \_ LINK.** Para obtener más información, [vea Hipervínculos RichEdit automáticos](/archive/blogs/murrays/automatic-richedit-hyperlinks) e [Hipervínculos de nombre descriptivo richedit](/archive/blogs/murrays/richedit-friendly-name-hyperlinks).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

[VÍNCULO DE \_ EN](en-link.md)
</dt> </dl>

 

