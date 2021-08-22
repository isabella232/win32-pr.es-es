---
title: Acerca de WinINet
description: La Windows de programación de aplicaciones (API) de Internet (WinINet) permite que la aplicación interactúe con los protocolos FTP y HTTP para acceder a los recursos de Internet.
ms.assetid: 0a06f2af-957a-4dff-a8cc-187370181b5c
keywords:
- Acerca de WinINet WinINet
- WinINet WinINet , acerca de
- WinINet WinINet, página de inicio
- Windows Internet WinINet
- Internet, Windows Internet WinINet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be38840c33735a1e064e9bdc5e044651130d6e15a6fe22d004a2e8d7c29bf140
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051873"
---
# <a name="about-wininet"></a>Acerca de WinINet

> [!NOTE]
> Para los contenedores de aplicaciones Windows 10, la versión 1709, HTTP/2 (consulte [RFC7540](https://tools.ietf.org/html/rfc7540)) está en estado predeterminado.

La Windows de programación de aplicaciones (API) de Internet (WinINet) permite que la aplicación interactúe con los protocolos FTP y HTTP para acceder a los recursos de Internet. A medida que evolucionan los estándares, estas funciones controlan los cambios en los protocolos subyacentes, lo que les permite mantener un comportamiento coherente.

**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También ha habilitado aplicaciones para interactuar con Gopher.

Para más información, consulte:

-   [WinINet frente a WinHTTP](wininet-vs-winhttp.md)
-   [Identificadores HINTERNET](appendix-a-hinternet-handles.md)
-   [Compatibilidad con ip versión 6](ip-version-6-support.md)
-   [Codificación \_ de contenido](content-encoding.md)
-   [Almacenamiento en caché](caching.md)
-   [Funciones comunes](common-functions.md)
-   [Sesiones FTP](ftp-sessions.md)
-   [Sesiones HTTP](http-sessions.md)
-   [HTTP Cookies](http-cookies.md)
-   [Operación asincrónica](asynchronous-operation.md)
-   [Control de la autenticación](handling-authentication.md)
-   [Control de localizadores uniformes de recursos](handling-uniform-resource-locators.md)
-   [Guía \_ de seguridad](security-guidelines.md)

## <a name="internet-protocols"></a>Protocolos de Internet

Los dos protocolos principales de Internet son FTP y HTTP. Para obtener más información sobre estos protocolos, vea los documentos de solicitud de comentarios (RFC) para FTP y HTTP:

-   [RFC 959](https://www.ietf.org/rfc/rfc0959.txt), *protocolo de transferencia de archivos (FTP)*.
-   [RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt), *Protocolo de transferencia de hipertexto : HTTP/1.0*.
-   [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), *Protocolo de transferencia de hipertexto : HTTP/1.1*.

> [!NOTE]  
> (Es posible que estos recursos no estén disponibles en algunos idiomas y países).

**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También se admite el protocolo Gopher. Vea [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt), *Protocolo Gopher de Internet*.
