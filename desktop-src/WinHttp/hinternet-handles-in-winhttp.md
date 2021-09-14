---
description: Microsoft Windows HTTP Services (WinHTTP) usa identificadores para realizar un seguimiento de la configuración y la información necesaria al usar el protocolo HTTP.
ms.assetid: 0bd82860-1347-40c8-ae77-c4d865c109be
title: Identificadores HINTERNET en WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf374675ad6f2114dd48e0a3ff1db50cd0dd7f9c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160544"
---
# <a name="hinternet-handles-in-winhttp"></a>Identificadores HINTERNET en WinHTTP

Microsoft Windows HTTP Services (WinHTTP) usa identificadores para realizar un seguimiento de la configuración y la información necesaria al usar el protocolo HTTP. Cada identificador mantiene la información pertinente para una sesión HTTP, una conexión con un servidor HTTP o un recurso específico. En este tema se describen los distintos tipos de identificadores, las convenciones de nomenclatura para estos identificadores y su estructura jerárquica.

-   [Acerca de los identificadores HINTERNET](#about-hinternet-handles)
-   [Identificadores de nomenclatura](#naming-handles)
-   [Jerarquía de identificadores](#handle-hierarchy)
-   [Explicación de la jerarquía de identificadores](#explanation-of-the-handle-hierarchy)

## <a name="about-hinternet-handles"></a>Acerca de los identificadores HINTERNET

Los identificadores creados y usados por WinHTTP se denominan **identificadores HINTERNET.** Las funciones WinHTTP devuelven identificadores **HINTERNET** que no son intercambiables con otros identificadores, por lo que no se pueden usar con funciones como [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) o [**CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) De forma similar, no se pueden usar otros identificadores con funciones WinHTTP. Por ejemplo, un identificador devuelto por [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) no se puede pasar [**a WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata). Estos **identificadores HINTERNET** no se pueden cerrar mientras una llamada API que usa el identificador está en curso. Para evitar una condición de carrera, las aplicaciones deben proteger el identificador y evitar que se cierre mientras la llamada API esté en curso.

Las funciones de Microsoft Win32 Internet (WinInet) también usan **identificadores HINTERNET.** Sin embargo, los identificadores usados en las funciones de WinInet no se pueden intercambiar con los identificadores usados en las funciones WinHTTP. Para obtener más información sobre WinInet, consulta [Acerca de WinINet.](/windows/desktop/WinInet/about-wininet)

La [**función WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle) cierra los identificadores de WinHTTP **HINTERNET.**

## <a name="naming-handles"></a>Identificadores de nomenclatura

En la documentación de WinHTTP, las descripciones de las funciones de la interfaz de programación de aplicaciones (API) y el código de ejemplo muestran la creación y el uso de varios tipos de **identificadores HINTERNET.** Para realizar un seguimiento de los distintos tipos de identificadores disponibles, la nomenclatura de estos identificadores es coherente. En la tabla siguiente se muestran los identificadores utilizados por convención en la documentación.



| Tipo de identificador       | Identificador de creación de funciones                                                                                                          | Identificador |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------|------------|
| Identificador genérico    | [**WinHttpOpen,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)o [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) | hInternet  |
| Identificador de sesión    | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)                                                                                                | hSession   |
| Identificador de conexión | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)                                                                                          | hConnect   |
| Identificador de solicitud    | [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                  | hRequest   |



 

## <a name="handle-hierarchy"></a>Jerarquía de identificadores

Los **identificadores HINTERNET** se mantienen en una jerarquía. El identificador devuelto por [**WinHttpOpen es**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) el identificador **HINTERNET de** sesión. Al **llamar a WinHttpOpen** se inicializan las funciones WinHTTP y se inicia un contexto de sesión que mantiene la información y la configuración del usuario a lo largo de la vida del identificador de sesión. [**WinHttpConnect especifica**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) un servidor HTTP o HTTPS de destino y crea un identificador **HINTERNET de** conexión. De forma predeterminada, el identificador de conexión hereda la configuración del identificador de sesión. A cada recurso especificado con una llamada a [**WinHttpOpenRequest se**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) le asigna un identificador **HINTERNET de** solicitud.

En el diagrama siguiente se muestra la jerarquía de **identificadores HINTERNET.** Cada cuadro del diagrama representa una función WinHTTP que devuelve un **identificador HINTERNET.**

![funciones que crean identificadores](images/art-winhttp2.png)

Después de cerrar un identificador, la aplicación debe estar preparada para recibir notificaciones de devolución de llamada en el identificador hasta que se devuelva el valor final de **WINHTTP \_ CALLBACK \_ STATUS HANDLE \_ \_ CLOSED** para indicar que el identificador está completamente cerrado.

Un identificador de sesión se denomina elemento primario de cualquier identificador de conexión que se usa para crear; Del mismo modo, tanto el identificador de conexión como su identificador de sesión principal se denominan elementos primarios de cualquier identificador de solicitud que se usa para crear el identificador de conexión.

Cuando se cierra un identificador primario, todos los elementos secundarios que tiene se invalidan indirectamente aunque no se cierren ellos mismos y las solicitudes posteriores que los usan producirán el **error ERROR \_ INVALID \_ HANDLE**. No se puede confiar en las solicitudes asincrónicas pendientes para completarse correctamente.

En el diagrama siguiente se muestran las funciones que usan el identificador **HINTERNET** creado [**por WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). Los cuadros sombreados representan funciones WinHTTP que crean identificadores y los cuadros sin formato muestran las funciones que usan esos **identificadores HINTERNET.** El diagrama también se organiza para mostrar el orden en el que normalmente se llama a las funciones WinHTTP.

![funciones que crean identificadores](images/art-winhttp2.png)

## <a name="explanation-of-the-handle-hierarchy"></a>Explicación de la jerarquía de identificadores

En primer lugar, se crea un identificador de sesión [**con WinHttpOpen.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) [**WinHttpConnect requiere**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) el identificador de sesión como primer parámetro y devuelve un identificador de conexión para un servidor especificado. [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)crea un identificador de solicitud, que usa el identificador de conexión creado [**por WinHttpConnect.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) Si la aplicación decide agregar encabezados adicionales a la solicitud o si es necesario que la aplicación establezca las credenciales para la autenticación, se puede llamar a [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) y [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) mediante este identificador de solicitud. [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)envía la solicitud, que usa el identificador de solicitud. Después de enviar la solicitud, se pueden enviar datos adicionales al servidor mediante [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)o la aplicación puede ir directamente a [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) para especificar que no se envíe más información al servidor. En este momento, según el propósito de la aplicación, el identificador de solicitud se puede usar para llamar a [**WinHttpQueryHeaders,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)o recuperar un recurso con [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) y [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).

 

 
