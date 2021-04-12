---
title: Controladores de HINTERNET
description: Esta sección contiene información sobre los identificadores que usan las funciones WinINet y la jerarquía en la que funcionan.
ms.assetid: 8a9788ed-eb25-42cb-b912-8dffa3df1850
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba70d2fadbd0d8393685fec2075ebf0dc4aa11c2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488135"
---
# <a name="hinternet-handles"></a>Controladores de HINTERNET

Esta sección contiene información sobre los identificadores que usan las funciones WinINet y la jerarquía en la que funcionan.

-   [Acerca de los identificadores de HINTERNET](#about-hinternet-handles)
-   [Jerarquía de identificadores](#handle-hierarchy)
-   [Jerarquía de FTP](#ftp-hierarchy)
-   [Jerarquía HTTP](#http-hierarchy)

## <a name="about-hinternet-handles"></a>Acerca de los identificadores de HINTERNET

Los identificadores creados y utilizados por las funciones WinINet son de tipo **HINTERNET**. Las funciones WinINet devuelven identificadores **HINTERNET** que no son intercambiables con otros tipos de identificador. Por lo tanto, no se pueden usar con funciones como [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) o [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle). Del mismo modo, no se pueden usar otros tipos de identificadores con las funciones de WinINet. Por ejemplo, un identificador devuelto por [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) no se puede pasar a [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).

La función [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) cierra los identificadores de tipo **HINTERNET**. Tenga en cuenta que los valores de identificador se reciclan rápidamente. por lo tanto, si se cierra un identificador y se genera inmediatamente un nuevo identificador, existe la posibilidad de que el nuevo identificador tenga el mismo valor que el controlador que se acaba de cerrar.

## <a name="handle-hierarchy"></a>Jerarquía de identificadores

Los identificadores de **HINTERNET** se mantienen en una jerarquía de árbol. El identificador devuelto por la función [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) es el nodo raíz. Los identificadores devueltos por la función [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) ocupan el siguiente nivel. Los identificadores devueltos por las funciones [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)y [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) son los nodos hoja.

**Windows XP y Windows Server 2003 R2 y versiones anteriores:** Los identificadores devueltos por, [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)y [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) también son nodos hoja.

En el diagrama siguiente se ilustra la jerarquía de los identificadores de **HINTERNET** . Cada cuadro del diagrama representa una función que devuelve un identificador **HINTERNET** .

![funciones que crean identificadores](images/ax-wnt01.png)

En el nivel superior se encuentra la función [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) , que crea el identificador raíz. El siguiente nivel contiene las funciones [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) y [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) . Las funciones que usan el identificador devuelto por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) forman el último nivel.

En el diagrama siguiente se muestran las funciones que dependen del identificador creado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla). Los cuadros sombreados representan funciones que devuelven los identificadores de **HINTERNET** , mientras que los cuadros simples representan funciones que utilizan el identificador **HINTERNET** creado por la función asociada.

![funciones que utilizan el identificador internetopenurl](images/ax-wnt02.png)

Las funciones [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)y [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) usan el identificador de **HINTERNET** creado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

## <a name="ftp-hierarchy"></a>Jerarquía de FTP

En el diagrama siguiente se muestran las funciones de FTP que dependen del identificador de sesión FTP devuelto por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). Los cuadros sombreados representan funciones que devuelven los identificadores de **HINTERNET** , mientras que los cuadros simples representan funciones que utilizan el identificador **HINTERNET** creado por la función de la que dependen.

![funciones que utilizan el identificador de sesión FTP](images/ax-wnt06.png)

Todas las funciones [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya), [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea), [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya), [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)y [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) usan el identificador de **HINTERNET** creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).

En el diagrama siguiente se muestran las dos funciones de FTP que devuelven los identificadores y las funciones que dependen de ellos. Los cuadros sombreados representan funciones que devuelven los identificadores de **HINTERNET** , mientras que los cuadros simples representan funciones que utilizan el identificador **HINTERNET** creado por la función de la que dependen.

![funciones que usan el identificador de ftpopen y ftpfindfirstfile](images/ax-wnt03.png)

La función [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) depende del identificador creado por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), mientras que [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) y [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) usan el identificador creado por [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).

## <a name="http-hierarchy"></a>Jerarquía HTTP

En el diagrama siguiente se muestran las relaciones de las funciones que se usan para el protocolo HTTP. Los cuadros sombreados representan funciones que devuelven los identificadores de **HINTERNET** , mientras que los cuadros simples representan funciones que utilizan el identificador **HINTERNET** creado por la función de la que dependen.

![funciones que usan el identificador de httpopenrequest](images/ax-wnt05.png)

Las funciones [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa), [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa), [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa)y [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) dependen del identificador creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).

En el diagrama siguiente se muestran las funciones que utilizan el identificador **HINTERNET** creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) después de que lo envíe [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). Los cuadros sombreados representan funciones que devuelven los identificadores de **HINTERNET** , mientras que los cuadros simples representan funciones que utilizan el identificador **HINTERNET** creado por la función de la que dependen.

![funciones que usan el identificador después de httpsendrequest](images/ax-wnt07.png)

Después de que [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) haya usado el identificador devuelto por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), se puede usar en [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)y [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer).

![funciones que usan el identificador después de HttpSendRequestEx](images/ax-wnt08.png)

Después de que [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa) haya usado el identificador devuelto por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), [**HttpEndRequest**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta), [**InternetReadFileEx**](/windows/desktop/api/Wininet/nf-wininet-internetreadfileexa)y [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)pueden usar el identificador. Después de llamar a [**HttpEndRequest**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta) , [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)y [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)pueden usar el identificador.

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 