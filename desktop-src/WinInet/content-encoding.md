---
title: Codificación de contenido
description: A partir de Windows Server 2008 y Windows Vista, la aplicación puede indicar a WinINet que realice la descodificación de contenido para los esquemas de codificación de contenido gzip y DEFLATE.
ms.assetid: 136f22a6-e5ca-41c5-8651-6e132655d268
keywords:
- Codificación de contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b089ae2aa4cbacdfc9b6ebefe5cbdfc1bfc10e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078236"
---
# <a name="content-encoding"></a>Codificación de contenido

Tal y como se especifica en el protocolo HTTP (RFC 2616), las aplicaciones pueden solicitar que el servidor devuelva respuestas HTTP en formato codificado. Antes de Windows Server 2008 y Windows Vista, las solicitudes con codificación de contenido se enviaban a la aplicación para su procesamiento en su nivel. A partir de Windows Server 2008 y Windows Vista, la aplicación puede indicar a WinINet que realice la descodificación de contenido para los esquemas de codificación de contenido gzip y DEFLATE.

Para habilitar la descodificación de contenido, la aplicación establece la opción de descodificación solicitando que WinINet realice la descodificación en su nombre. Sin embargo, al habilitar la descodificación no se garantiza que WinINet realice la descodificación de contenido y la aplicación debe estar preparada para controlar la descodificación. WinINet quita el encabezado Content-Encoding de la respuesta cuando se realiza correctamente la descodificación de contenido. Se espera que las aplicaciones controlen la descodificación de contenido independientemente de si la opción de descodificación está habilitada o deshabilitada cuando el encabezado Content-Encoding está presente en la respuesta.

Cuando la descodificación está habilitada, la aplicación debe especificar la lista de codificaciones admitidas en el encabezado Accept-Encoding de la solicitud. Sin embargo, el encabezado Accept-Encoding no obliga al servidor a enviar una respuesta codificada. WinINet enviará las respuestas que no coincidan con la lista de codificaciones aceptables de vuelta a la aplicación.

En la lista siguiente se describen las condiciones en las que WinINet realizará la descodificación de contenido cuando se habilite la opción:

-   El encabezado Accept-Encoding debe estar presente en la solicitud y debe especificar los esquemas de codificación gzip, DEFLATE o gzip y DEFLATE.
-   El esquema de codificación especificado en el encabezado Content-Encoding debe coincidir con uno de los esquemas de codificación especificados en el encabezado Accept-Encoding.
-   El encabezado Content-Encoding de la respuesta especifica solo un esquema de codificación.
-   La respuesta debe contener solo un encabezado Content-Encoding. WinINet descodifica el contenido que está codificado con un solo esquema de codificación.
-   El encabezado Cache-Control no debe contener la Directiva no-transform.
-   El encabezado Content-Range no debe estar presente en la respuesta.

## <a name="setting-the-decompression-option"></a>Establecer la opción de descompresión

La opción de descodificación se puede establecer en el identificador de la sesión, el identificador de la solicitud o el identificador de conexión. Identificador en el que se establece la opción de descodificación, que define el ámbito de la opción de descodificación. Por ejemplo, si se establece la descodificación en la sesión, se habilitará la descodificación de todas las conexiones y solicitudes creadas bajo dicho identificador.

Para establecer la opción de descodificación, la aplicación llama a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) con el identificador devuelto por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta). La opción de **Internet \_ \_ \_ descodificación http** se especifica en el parámetro *dwOption* y el parámetro *lpBuffer* apunta a una variable booleana establecida en true. Para deshabilitar la descodificación, la aplicación llama a **InternetSetOption** con la opción de **Internet \_ \_ \_ descodificación http** y la variable booleana establecida en false.

Cuando se establece la opción de descodificación, WinINet realiza la descodificación en la solicitud cuando la aplicación llama a [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile). Si WinINet detecta un error mientras realiza la descodificación de contenido, se produce un error en la llamada a **InternetReadFile** con un error en la **\_ \_ descodificación \_ de Internet**. Cuando se produce un error en la descodificación, la aplicación tiene dos opciones: puede quitar el encabezado Accept-Encoding y volver a enviar la solicitud, o bien establecer la opción de configuración de **Internet \_ \_ \_ descodificación http** en la solicitud en false y volver a enviar la solicitud. Si la opción de descodificación está establecida en false, la aplicación debe comprobar el encabezado Content-Encoding y realizar cualquier descodificación en el nivel de la aplicación.

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 