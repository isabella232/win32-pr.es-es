---
title: Internet de Windows
description: La interfaz de programación de aplicaciones (API) de Microsoft Windows Internet (WinINet) permite a las aplicaciones tener acceso a los protocolos estándar de Internet, como FTP y HTTP. Para facilitar su uso, WinINet abstrae estos protocolos en una interfaz de alto nivel.
ms.assetid: 9d1856ac-f281-4582-bb70-83a8ec674914
keywords:
- Windows Internet WinINet
- WinINet WinINet, portal
- Windows Internet WinINet, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b5b76fefea900d3f187deb89929d3a09fe3c78
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488087"
---
# <a name="windows-internet"></a>Internet de Windows

## <a name="purpose"></a>Propósito

La interfaz de programación de aplicaciones (API) de Microsoft Windows Internet (WinINet) permite a las aplicaciones tener acceso a los protocolos estándar de Internet, como FTP y HTTP. Para facilitar su uso, WinINet abstrae estos protocolos en una interfaz de alto nivel.

## <a name="where-applicable"></a>Donde sea aplicable

WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

## <a name="developer-audience"></a>Audiencia de desarrolladores

WinINet está diseñado para que lo usen los programadores de C/C++. Requiere un conocimiento básico de los protocolos FTP y HTTP.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Las aplicaciones que utilizan la API WinINet requieren Windows NT 4,0 o posterior, o Windows Me/98/95. Para obtener más información sobre qué sistemas operativos o componentes son necesarios para usar un elemento de programación determinado, consulte la sección de requisitos de la documentación.

## <a name="in-this-section"></a>En esta sección



| Tema                                                          | Descripción                                                      |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [Acerca de Windows Internet](about-wininet.md)<br/>         | Información general sobre la API de Internet de Windows.<br/>   |
| [Usar Internet de Windows](using-wininet.md)<br/>         | Guía de programación de la API de Internet de Windows.<br/>       |
| [Referencia de Internet de Windows](wininet-reference.md)<br/> | Documentación de referencia de la API de Internet de Windows.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios HTTP de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

