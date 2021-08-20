---
description: En este tema se identifican las constantes que usa WinHTTP.
ms.assetid: 460f1463-57a8-47eb-9957-17976757bd7f
title: Constantes WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f25ba011fdc97d55bae57c38a937a08177a6cefe2ecaaef3f85e2486e90956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114195"
---
# <a name="winhttp-constants"></a>Constantes WinHTTP

WinHTTP usa las siguientes constantes:

<dl>

<dt>

[**mensajes de error**](error-messages.md)
</dt> <dd>

Mensajes de error específicos de las funciones WinHTTP. Estas funciones también devuelven Windows de error cuando corresponda. El valor que corresponde a cada constante es el valor de la constante para las funciones de la interfaz de programación de aplicaciones (API) y los 16 bits inferiores del número de error para el [**objeto WinHttpRequest.**](winhttprequest.md)

</dd> <dt>

[**Códigos de estado HTTP**](http-status-codes.md)
</dt> <dd>

Constantes y valores correspondientes que indican códigos de estado HTTP devueltos por servidores en Internet.

</dd> <dt>

[**Marcas de opción**](option-flags.md)
</dt> <dd>

Marcas de opción admitidas [**por WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) [**y WinHttpSetOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) Todas las marcas de opción válidas tienen un valor mayor o igual que WINHTTP FIRST OPTION y menor o \_ \_ igual que WINHTTP LAST \_ \_ OPTION.

</dd> <dt>

[**PUERTO DE \_ INTERNET**](internet-port.md)
</dt> <dd>

Valor DE WORD que indica el puerto.

</dd> <dt>

[**ESQUEMA \_ DE INTERNET**](internet-scheme.md)
</dt> <dd>

Esquemas de Internet compatibles con WinHTTP.

</dd>

<dt>

[**Marcas de información de consulta**](query-info-flags.md)
</dt>
<dd>

Atributos y modificadores usados [**por WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).
</dd>

<dt>

**WINHTTP_EXTENDED_HEADER_FLAG_UNICODE**
</dt>
<dd>

Tiene un valor de 0x00000001. Indica a [WinHttpAddRequestHeadersEx](/windows/win32/api/winhttp/nf-winhttp-winhttpaddrequestheadersex) que las cadenas pasadas son cadenas Unicode.
</dd>

<dt>

**WINHTTP_READ_DATA_EX_FLAG_FILL_BUFFER**
</dt>
<dd>

Tiene un valor de 0x0000000000000001ull. Indica a [WinHttpReadDataEx](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddataex) que no complete la llamada hasta que se haya rellenado el búfer de datos proporcionado o se complete la respuesta. Pasar esta marca hace que el comportamiento de **WinHttpReadDataEx** sea equivalente al de [WinHttpReadData.](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddata)
</dd>

</dl>
