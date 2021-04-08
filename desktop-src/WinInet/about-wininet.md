---
title: Acerca de WinINet
description: La interfaz de programación de aplicaciones (API) de Windows Internet (WinINet) permite que la aplicación interactúe con los protocolos FTP y HTTP para tener acceso a los recursos de Internet.
ms.assetid: 0a06f2af-957a-4dff-a8cc-187370181b5c
keywords:
- Acerca de WinINet WinINet
- WinINet WinINet, acerca de
- WinINet WinINet, página de inicio
- Windows Internet WinINet
- Internet, Windows Internet WinINet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4513e5c3912a483fd4dbef96f452c5712717c8a5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "103994984"
---
# <a name="about-wininet"></a>Acerca de WinINet

> [!NOTE]
> En el caso de los contenedores de aplicaciones desde la versión 1709 de Windows 10, HTTP/2 (consulte [RFC7540](https://tools.ietf.org/html/rfc7540)) está activada de forma predeterminada.

La interfaz de programación de aplicaciones (API) de Windows Internet (WinINet) permite que la aplicación interactúe con los protocolos FTP y HTTP para tener acceso a los recursos de Internet. A medida que evolucionan los estándares, estas funciones controlan los cambios en los protocolos subyacentes, lo que les permite mantener un comportamiento coherente.

**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También permite a las aplicaciones interactuar con Gopher.

Para más información, consulte:

-   [WinINet frente a WinHTTP](wininet-vs-winhttp.md)
-   [Controladores de HINTERNET](appendix-a-hinternet-handles.md)
-   [Compatibilidad con IP versión 6](ip-version-6-support.md)
-   [Codificación de contenido \_](content-encoding.md)
-   [Almacenamiento en caché](caching.md)
-   [Funciones comunes](common-functions.md)
-   [Sesiones FTP](ftp-sessions.md)
-   [Sesiones HTTP](http-sessions.md)
-   [Cookies HTTP](http-cookies.md)
-   [Operación asincrónica](asynchronous-operation.md)
-   [Controlar la autenticación](handling-authentication.md)
-   [Controlar localizadores uniformes de recursos](handling-uniform-resource-locators.md)
-   [Instrucciones de seguridad \_](security-guidelines.md)

## <a name="internet-protocols"></a>Protocolos de Internet

Los dos protocolos de Internet principales son FTP y HTTP. Para obtener más información acerca de estos protocolos, consulte los documentos RFC (solicitud de comentarios) para FTP y HTTP:

-   [RFC 959](https://www.ietf.org/rfc/rfc0959.txt), *Protocolo de transferencia de archivos (FTP)*.
-   [RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt), *Protocolo de transferencia de hipertexto: http/1.0*.
-   [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), *Protocolo de transferencia de hipertexto: http/1.1*.

> [!NOTE]  
> (Es posible que estos recursos no estén disponibles en algunos idiomas y países).

**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También se admitía el protocolo Gopher. Consulte [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt), *el protocolo Gopher de Internet*.
