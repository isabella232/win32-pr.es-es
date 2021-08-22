---
title: Codificación de contenido
description: A partir de Windows Server 2008 y Windows Vista, la aplicación puede dirigir a WinINet para que realice la codificación de contenido para los esquemas de codificación de contenido gzip y deflate.
ms.assetid: 136f22a6-e5ca-41c5-8651-6e132655d268
keywords:
- Codificación de contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1a91120e4ea01c4636c8d9942e968a0d69aeed50b6a037b31aa0241f3e933c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132888"
---
# <a name="content-encoding"></a>Codificación de contenido

Como se especifica en el protocolo HTTP (RFC 2616), las aplicaciones pueden solicitar que el servidor devuelva respuestas HTTP en formato codificado. Antes de Windows Server 2008 y Windows Vista, las solicitudes con codificación de contenido se enviaban a la aplicación para su procesamiento en su nivel. A partir de Windows Server 2008 y Windows Vista, la aplicación puede dirigir a WinINet para que realice la codificación de contenido para los esquemas de codificación de contenido gzip y deflate.

Para habilitar lacoding de contenido, la aplicación establece la opción de descoding que solicita que WinINet realice la decodificación en su nombre. Sin embargo, la habilitación de lacoding no garantiza que WinINet realice lacoding de contenido y la aplicación debe estar preparada para controlar la decodificación. WinINet quita el encabezado de codificación de contenido de la respuesta cuando la codificación de contenido se realiza correctamente. Se espera que las aplicaciones controle la codificación de contenido independientemente de si la opción de codificación está habilitada o deshabilitada cuando el encabezado de codificación de contenido está presente en la respuesta.

Cuando la codificación está habilitada, la aplicación debe especificar la lista de codificaciones admitidas en el Accept-Encoding encabezado de la solicitud. El Accept-Encoding, sin embargo, no obliga al servidor a enviar una respuesta codificada. WinINet enviará a la aplicación respuestas que no coincidan con la lista de codificaciones aceptables.

En la lista siguiente se describen las condiciones en las que WinINet realizará la decodificación de contenido cuando la opción esté habilitada:

-   El Accept-Encoding debe estar presente en la solicitud y debe especificar los esquemas de codificación gzip, deflate o gzip y deflate.
-   El esquema de codificación especificado en el encabezado Content-Encoding debe coincidir con uno de los esquemas de codificación especificados en el Accept-Encoding encabezado.
-   El encabezado Content-Encoding de la respuesta especifica solo un esquema de codificación.
-   La respuesta solo debe contener un encabezado Content- Encoding. WinINet descodifica el contenido codificado con un solo esquema de codificación.
-   El Cache-Control encabezado no debe contener la directiva no-transform.
-   El encabezado Content-Range no debe estar presente en la respuesta.

## <a name="setting-the-decompression-option"></a>Establecer la opción Descompresión

La opción de decoding se puede establecer en el identificador de sesión, el identificador de solicitud o el identificador de conexión. El identificador en el que se establece la opción de decoding define el ámbito de la opción decoding. Por ejemplo, al establecer la decoding en la sesión se habilitará la decoding de todas las conexiones y solicitudes creadas en ese identificador.

Para establecer la opción de decoding, la aplicación llama a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) con el identificador devuelto [**de InternetOpen,**](/windows/desktop/api/Wininet/nf-wininet-internetopena) [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)o [**HttpOpenRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) La **opción INTERNET OPTION HTTP \_ \_ \_ DECODING** se especifica en el parámetro *dwOption* y el parámetro *lpBuffer* apunta a una variable booleana establecida en true. Para deshabilitar lacoding, la aplicación llama a **InternetSetOption** con la opción **\_ HTTP \_ \_ DECODING INTERNET OPTION** y la variable booleana establecida en false.

Cuando se establece la opción de decoding, WinINet realiza la decodificación en la solicitud cuando la aplicación llama a [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile). Si WinINet encuentra un error al realizar la decodificación de contenido, se produce un error en la llamada a **InternetReadFile** con **un ERROR INTERNET \_ \_ DECODING \_ FAILED**. Cuando se produce un error en lacodización, la aplicación tiene dos opciones: puede quitar el encabezado Accept-Encoding y volver a enviar la solicitud, o puede establecer la opción **\_ \_ \_ DECODING HTTP DE** INTERNET OPTION en la solicitud en false y, a continuación, volver a enviar la solicitud. Si la opción de codificación se establece en false, la aplicación debe comprobar el encabezado Content-Encoding y realizar cualquier codificación en el nivel de aplicación.

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para las implementaciones o servicios de servidor, use [Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 