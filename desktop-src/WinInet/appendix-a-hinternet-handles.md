---
title: Identificadores HINTERNET
description: Esta sección contiene información sobre los identificadores que usan las funciones de WinINet y la jerarquía en la que funcionan.
ms.assetid: 8a9788ed-eb25-42cb-b912-8dffa3df1850
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477558887ac484ec0c3645d568bc3d91d29926af887ebadc51cf7e9523da787
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051936"
---
# <a name="hinternet-handles"></a>Identificadores HINTERNET

Esta sección contiene información sobre los identificadores que usan las funciones de WinINet y la jerarquía en la que funcionan.

-   [Acerca de los identificadores HINTERNET](#about-hinternet-handles)
-   [Jerarquía de identificadores](#handle-hierarchy)
-   [Jerarquía de FTP](#ftp-hierarchy)
-   [Jerarquía HTTP](#http-hierarchy)

## <a name="about-hinternet-handles"></a>Acerca de los identificadores HINTERNET

Los identificadores creados y usados por las funciones de WinINet son de tipo **HINTERNET.** Las funciones de WinINet devuelven **identificadores HINTERNET** que no son intercambiables con otros tipos de identificador. Por lo tanto, no se pueden usar con funciones como [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) o [**CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) De forma similar, otros tipos de identificador no se pueden usar con las funciones de WinINet. Por ejemplo, un identificador devuelto por [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) no se puede pasar a [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).

La [**función InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) cierra los identificadores de tipo **HINTERNET**. Tenga en cuenta que los valores de identificador se reciclan rápidamente; Por lo tanto, si se cierra un identificador y se genera un nuevo identificador inmediatamente, es muy posible que el nuevo identificador tenga el mismo valor que el identificador que se acaba de cerrar.

## <a name="handle-hierarchy"></a>Jerarquía de identificadores

Los **identificadores HINTERNET** se mantienen en una jerarquía de árbol. El identificador devuelto por la [**función InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) es el nodo raíz. Los identificadores devueltos [**por la función InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) ocupan el siguiente nivel. Los identificadores devueltos [**por las funciones FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)y [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) son los nodos hoja.

**Windows XP y Windows Server 2003 R2 y versiones anteriores:** Los identificadores devueltos por , [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)y [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) también son nodos hoja.

En el diagrama siguiente se muestra la jerarquía de los **identificadores HINTERNET.** Cada cuadro del diagrama representa una función que devuelve un **identificador HINTERNET.**

![funciones que crean identificadores](images/ax-wnt01.png)

En el nivel superior se encuentra [**la función InternetOpen,**](/windows/desktop/api/Wininet/nf-wininet-internetopena) que crea el identificador raíz. El siguiente nivel contiene las [**funciones InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) [**e InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) Las funciones que usan el identificador devuelto [**por InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) son el último nivel.

En el diagrama siguiente se muestran las funciones que dependen del identificador creado [**por InternetOpenUrl.**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) Los cuadros sombreados representan funciones que devuelven identificadores **HINTERNET,** mientras que los cuadros sin formato representan funciones que usan el identificador **HINTERNET** creado por la función asociada.

![funciones que usan el identificador internetopenurl](images/ax-wnt02.png)

Las [**funciones InternetQueryDataAvailable,**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) usan el identificador **HINTERNET** creado [**por InternetOpenUrl.**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)

## <a name="ftp-hierarchy"></a>Jerarquía de FTP

En el diagrama siguiente se muestran las funciones FTP que dependen del identificador de sesión FTP devuelto [**por InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) Los cuadros sombreados representan funciones que devuelven identificadores **HINTERNET,** mientras que los cuadros sin formato representan funciones que usan el identificador **HINTERNET** creado por la función de la que dependen.

![funciones que usan el identificador de sesión ftp](images/ax-wnt06.png)

Las [**funciones FtpCreateDirectory,**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) [**FtpDeleteFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) [**FtpGetCurrentDirectory,**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) [**FtpGetFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) [**FtpPutFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) [**FtpRemoveDirectory,**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)y [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) usan el identificador **HINTERNET** creado por [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)

En el diagrama siguiente se muestran las dos funciones FTP que devuelven identificadores y las funciones que dependen de ellas. Los cuadros sombreados representan funciones que devuelven identificadores **HINTERNET,** mientras que los cuadros sin formato representan funciones que usan el identificador **HINTERNET** creado por la función de la que dependen.

![funciones que usan el identificador de ftpopen y ftpfindfirstfile](images/ax-wnt03.png)

La [**función InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) depende del identificador creado por [**FtpFindFirstFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)mientras que [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) e [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) usan el identificador creado por [**FtpOpenFile.**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)

## <a name="http-hierarchy"></a>Jerarquía HTTP

En el diagrama siguiente se muestran las relaciones de las funciones que se usan para el protocolo HTTP. Los cuadros sombreados representan funciones que devuelven identificadores **HINTERNET,** mientras que los cuadros sin formato representan funciones que usan el identificador **HINTERNET** creado por la función de la que dependen.

![funciones que usan el identificador de httpopenrequest](images/ax-wnt05.png)

Las [**funciones HttpAddRequestHeaders,**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) [**HttpQueryInfo,**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) [**HttpSendRequest,**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa)e [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) dependen del identificador creado por [**HttpOpenRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)

En el diagrama siguiente se muestran las funciones que usan el identificador **HINTERNET** creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) después de que [**httpSendRequest lo**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)envíe. Los cuadros sombreados representan funciones que devuelven identificadores **HINTERNET,** mientras que los cuadros sin formato representan funciones que usan el identificador **HINTERNET** creado por la función de la que dependen.

![funciones que usan el identificador después de httpsendrequest](images/ax-wnt07.png)

Después [**de que HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) haya usado el identificador devuelto por [**HttpOpenRequest,**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) [**internetQueryDataAvailable,**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)e [**InternetSetFilePointer pueden usarlo.**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)

![funciones que usan el identificador después de httpsendrequestex](images/ax-wnt08.png)

Después [**de que HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa) haya usado el identificador devuelto por [**HttpOpenRequest,**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) [**HttpEndRequest,**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta) [**InternetReadFileEx**](/windows/desktop/api/Wininet/nf-wininet-internetreadfileexa)e [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)pueden usar el identificador . Una vez que se ha llamado a [**HttpEndRequest,**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta) [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)e [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)pueden usar el identificador .

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para implementaciones de servidor o servicios, use [Microsoft Windows SERVICIOS HTTP (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 