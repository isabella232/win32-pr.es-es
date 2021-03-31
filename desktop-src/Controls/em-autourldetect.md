---
title: Mensaje EM_AUTOURLDETECT (RichEdit. h)
description: Habilita o deshabilita la detección automática de hipervínculos mediante un control Rich Edit.
ms.assetid: 6970ff36-ff3f-4413-a471-9389a76c8f38
keywords:
- EM_AUTOURLDETECT controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996654"
---
# <a name="em_autourldetect-message"></a>\_Mensaje AUTOURLDETECT em

Habilita o deshabilita la detección automática de hipervínculos mediante un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifique 0 para deshabilitar la detección automática de vínculos o uno de los valores siguientes para habilitar distintos tipos de detección.



| Value                                                                                                                                                                                       | Significado                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AURL_DISABLEMIXEDLGC"></span><span id="aurl_disablemixedlgc"></span><dl> <dt>**AURL \_ DISABLEMIXEDLGC**</dt> </dl>          | **Windows 8**: deshabilite el reconocimiento de nombres de dominio que contengan etiquetas con caracteres que pertenezcan a más de uno de los siguientes scripts: Latín, griego y cirílico. <br/> |
| <span id="AURL_ENABLEDRIVELETTERS"></span><span id="aurl_enabledriveletters"></span><dl> <dt>**AURL \_ ENABLEDRIVELETTERS**</dt> </dl> | **Windows 8**: reconoce los nombres de archivo que tienen una especificación de unidad inicial, como c: \\ temp.<br/>                                                                           |
| <span id="AURL_ENABLEEA"></span><span id="aurl_enableea"></span><dl> <dt>**AURL \_ ENABLEEA**</dt> </dl>                               | Este valor está en desuso; Use **AURL \_ ENABLEEAURLS** en su lugar.<br/>                                                                                                            |
| <span id="AURL_ENABLEEAURLS"></span><span id="aurl_enableeaurls"></span><dl> <dt>**AURL \_ ENABLEEAURLS**</dt> </dl>                   | Reconoce las direcciones URL que contienen caracteres de Asia oriental. <br/>                                                                                                                      |
| <span id="AURL_ENABLEEMAILADDR"></span><span id="aurl_enableemailaddr"></span><dl> <dt>**AURL \_ ENABLEEMAILADDR**</dt> </dl>          | **Windows 8**: reconocer direcciones de correo electrónico.<br/>                                                                                                                                |
| <span id="AURL_ENABLETELNO"></span><span id="aurl_enabletelno"></span><dl> <dt>**AURL \_ ENABLETELNO**</dt> </dl>                      | **Windows 8**: reconocer números de teléfono.<br/>                                                                                                                              |
| <span id="AURL_ENABLEURL"></span><span id="aurl_enableurl"></span><dl> <dt>**AURL \_ ENABLEURL**</dt> </dl>                            | **Windows 8**: reconozca las direcciones URL que incluyen la ruta de acceso.<br/>                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro determina los esquemas de dirección URL reconocidos si **AURL \_ ENABLEURL** está activo. Si *lParam* es null, se utiliza la lista de nombres de esquema predeterminados (vea la sección comentarios). Como alternativa, *lParam* puede apuntar a una cadena terminada en null que consta de hasta 50 nombres de esquema terminados con dos puntos que sustituyen a la lista de nombres de esquemas predeterminados. Por ejemplo, la cadena puede ser "News: http: ftp: Telnet:". La sintaxis de nombre de esquema se define en el sitio web de los [identificadores uniformes de recursos (URI): Sintaxis genérica]( https://www.ietf.org/rfc/rfc2396.txt) en el sitio web del equipo de ingeniería de Internet (IETF). En concreto, un nombre de esquema puede contener hasta 13 caracteres (incluidos los dos puntos), debe empezar por un carácter alfabético ASCII y puede ir seguido de una combinación de alphabetics ASCII, dígitos y los tres caracteres de puntuación: ".", "+" y "-". El tipo de cadena puede ser **Char \** _ o _*WCHAR \**_; el control Rich Edit detecta automáticamente el tipo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es cero.

Si se produce un error en el mensaje, el valor devuelto es un valor distinto de cero. Por ejemplo, puede producirse un error en el mensaje debido a que no hay memoria suficiente, una opción de detección no válida o una cadena de nombre de esquema no válida.

Si _lParam * contiene más de 50 nombres de esquema, se produce un error en el mensaje con un valor devuelto de **E \_ INVALIDARG**.

## <a name="remarks"></a>Observaciones

Si la detección automática de direcciones URL está habilitada (es decir, *wParam* incluye **AURL \_ ENABLEURL**), el control Rich Edit examina cualquier texto modificado para determinar si el texto coincide con el formato de una dirección URL (o más general en Windows 8 o posterior, un identificador de recursos de IRI International). Si *lParam* es null, el control detecta las direcciones URL que comienzan con los siguientes nombres de esquema:

-   callto
-   archivo
-   ftp
-   gopher
-   http
-   https
-   mailto
-   news
-   HDInsight
-   NNTP
-   onenote
-   Outlook
-   prospero
-   tel
-   telnet
-   wais
-   webcal

Cuando se habilita la detección automática de vínculos, el control Rich Edit quita el efecto de **\_ vínculo CFE** del texto modificado que no tiene un formato reconocido por el control. Si la aplicación usa el efecto de **\_ vínculo CFE** para marcar otros tipos de texto, no habilite la detección automática de vínculos. El control Rich Edit no comprueba si existe un vínculo detectado; esa responsabilidad pertenece al cliente.

Un control Rich Edit envía la notificación de [ \_ vínculo en](en-link.md) cuando recibe varios mensajes mientras el puntero del mouse se encuentra sobre el texto que tiene el efecto de **\_ vínculo CFE** . Para obtener más información, vea [hipervínculos de RichEdit automático](/archive/blogs/murrays/automatic-richedit-hyperlinks) y [hipervínculos de nombre descriptivo de RichEdit](/archive/blogs/murrays/richedit-friendly-name-hyperlinks).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

[EN \_ vínculo](en-link.md)
</dt> </dl>

 

