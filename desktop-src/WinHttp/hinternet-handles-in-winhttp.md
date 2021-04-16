---
description: Los servicios HTTP de Microsoft Windows (WinHTTP) usan identificadores para realizar un seguimiento de la configuración y la información necesaria cuando se usa el protocolo HTTP.
ms.assetid: 0bd82860-1347-40c8-ae77-c4d865c109be
title: Controladores HINTERNET en WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf374675ad6f2114dd48e0a3ff1db50cd0dd7f9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563559"
---
# <a name="hinternet-handles-in-winhttp"></a>Controladores HINTERNET en WinHTTP

Los servicios HTTP de Microsoft Windows (WinHTTP) usan identificadores para realizar un seguimiento de la configuración y la información necesaria cuando se usa el protocolo HTTP. Cada identificador mantiene la información pertinente a una sesión HTTP, una conexión con un servidor HTTP o un recurso específico. En este tema se describen los distintos tipos de identificadores, las convenciones de nomenclatura de estos identificadores y su estructura jerárquica.

-   [Acerca de los identificadores de HINTERNET](#about-hinternet-handles)
-   [Controladores de nomenclatura](#naming-handles)
-   [Jerarquía de identificadores](#handle-hierarchy)
-   [Explicación de la jerarquía de identificadores](#explanation-of-the-handle-hierarchy)

## <a name="about-hinternet-handles"></a>Acerca de los identificadores de HINTERNET

Los identificadores que se crean y usan en WinHTTP se denominan identificadores de **HINTERNET** . Las funciones WinHTTP devuelven identificadores **HINTERNET** que no son intercambiables con otros identificadores, por lo que no se pueden usar con funciones como [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) o [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle). Del mismo modo, no se pueden usar otros identificadores con funciones WinHTTP. Por ejemplo, un identificador devuelto por [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) no se puede pasar a [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata). Estos identificadores de **HINTERNET** no se pueden cerrar mientras haya una llamada API que use el identificador en curso. Para evitar una condición de carrera, las aplicaciones deben proteger el identificador e impedir que se cierre mientras la llamada a la API esté en curso.

Las funciones de Microsoft Win32 Internet (WinInet) también usan identificadores de **HINTERNET** . Sin embargo, los identificadores que se usan en las funciones WinInet no se pueden intercambiar con los identificadores utilizados en las funciones WinHTTP. Para obtener más información sobre WinInet, vea [About WinInet](/windows/desktop/WinInet/about-wininet).

La función [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle) cierra los identificadores de WinHTTP **HINTERNET** .

## <a name="naming-handles"></a>Controladores de nomenclatura

En la documentación de WinHTTP, las descripciones de las funciones de la interfaz de programación de aplicaciones (API) y el código de ejemplo muestran la creación y el uso de diversos tipos de identificadores de **HINTERNET** . Para realizar un seguimiento de los distintos tipos de identificadores disponibles, la nomenclatura de estos identificadores es coherente. En la tabla siguiente se muestran los identificadores usados por la Convención en la documentación de.



| Tipo de identificador       | Función que crea el controlador                                                                                                          | Identificador |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------|------------|
| Identificador genérico    | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen), [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)o [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) | hInternet  |
| Identificador de sesión    | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)                                                                                                | hSession   |
| Identificador de conexión | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)                                                                                          | hConnect   |
| Identificador de solicitud    | [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                  | hRequest   |



 

## <a name="handle-hierarchy"></a>Jerarquía de identificadores

Los identificadores de **HINTERNET** se mantienen en una jerarquía. El identificador devuelto por [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) es el identificador de **HINTERNET** de la sesión. La llamada a **WinHttpOpen** inicializa las funciones WinHTTP e inicia un contexto de sesión que mantiene la información y la configuración de usuario a lo largo de la vida del identificador de sesión. [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) especifica un servidor http o https de destino y crea un identificador de **HINTERNET** de conexión. De forma predeterminada, el identificador de conexión hereda la configuración del identificador de sesión. A cada recurso especificado con una llamada a [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) se le asigna un identificador de **HINTERNET** de solicitud.

En el diagrama siguiente se ilustra la jerarquía de los identificadores de **HINTERNET** . Cada cuadro del diagrama representa una función WinHTTP que devuelve un identificador **HINTERNET** .

![funciones que crean identificadores](images/art-winhttp2.png)

Después de cerrar un identificador, la aplicación debe estar preparada para recibir notificaciones de devolución de llamada en el identificador hasta que se devuelva el valor **Closed del identificador de estado de devolución de llamada de WinHTTP \_ \_ \_ \_** final para indicar que el identificador está completamente cerrado.

Un identificador de sesión se denomina elemento primario de cualquier identificador de conexión que se use para crear; del mismo modo, tanto el identificador de conexión como su identificador de sesión principal se denominan elementos primarios de cualquier identificador de solicitud que se utiliza para crear el identificador de conexión.

Cuando se cierra un identificador primario, los elementos secundarios que tiene se invalidan indirectamente incluso si no se cierran, y las solicitudes posteriores que los usan se producen con el error de **\_ \_ identificador no válido**. No se puede confiar en las solicitudes asincrónicas pendientes para que se completen correctamente.

En el diagrama siguiente se muestran las funciones que utilizan el identificador **HINTERNET** creado por [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). Los cuadros sombreados representan funciones de WinHTTP que crean identificadores y los cuadros de texto simple muestran las funciones que usan esos manipuladores de **HINTERNET** . El diagrama también se organiza para mostrar el orden en el que normalmente se llama a las funciones WinHTTP.

![funciones que crean identificadores](images/art-winhttp2.png)

## <a name="explanation-of-the-handle-hierarchy"></a>Explicación de la jerarquía de identificadores

En primer lugar, se crea un identificador de sesión con [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen). [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) requiere el identificador de sesión como primer parámetro y devuelve un identificador de conexión para un servidor especificado. [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)crea un identificador de solicitud que usa el identificador de conexión creado por [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect). Si la aplicación elige agregar encabezados adicionales a la solicitud, o si es necesario para que la aplicación establezca credenciales para la autenticación, se puede llamar a [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) y [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) mediante este identificador de solicitud. La solicitud se envía mediante [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), que usa el identificador de solicitud. Después de enviar la solicitud, se pueden enviar datos adicionales al servidor mediante [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata), o bien la aplicación puede omitir directamente [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) para especificar que no se envía más información al servidor. En este punto, dependiendo del propósito de la aplicación, el identificador de solicitud se puede usar para llamar a [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders), [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)o recuperar un recurso con [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) y [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).

 

 
