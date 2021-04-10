---
description: Proporciona vínculos a los códigos de error del sistema definidos en el archivo de encabezado WinError. h y está destinado a los desarrolladores.
ms.assetid: 4a3a8feb-a05f-4614-8f04-1f507da7e5b7
title: Códigos de error del sistema
ms.topic: article
ms.date: 10/31/2019
ms.openlocfilehash: 072e1eb4a43c787055bc2793b3f58d69cdf6dd12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153105"
---
# <a name="system-error-codes"></a>Códigos de error del sistema

Esta sección está destinada a desarrolladores que depuran errores del sistema. Si llegó a esta página durante la búsqueda de otros errores, estos son algunos vínculos que podrían ayudar:

* [Windows Update errores](https://support.microsoft.com/help/10164/fix-windows-update-errors) : para ayudar a resolver problemas con Windows Update.
* [Errores de activación de Windows](https://support.microsoft.com/help/10738/windows-10-get-help-with-activation-errors) : para obtener ayuda para comprobar la copia de Windows.
* [Solución de problemas de errores de pantalla azul](https://support.microsoft.com/help/14238/windows-10-troubleshoot-blue-screen-errors) : para obtener ayuda para detectar la causa de un error de detención.
* [Soporte técnico de Microsoft](https://support.microsoft.com) : para obtener soporte técnico con un producto de Microsoft.

## <a name="more-ways-to-find-an-error-code"></a>Más formas de buscar un código de error

En esta sección se enumeran los códigos de error del sistema, organizados por número. Si necesita más ayuda para hacer un seguimiento de un error específico, estas son algunas recomendaciones:

* Use la [herramienta de búsqueda de errores de Microsoft](system-error-code-lookup-tool.md).
*  Instale las herramientas de depuración para Windows, cargue un archivo de volcado de memoria y, a continuación, ejecute el comando **\! Err \<code>** .
* Busque el código de error o el texto sin formato en el sitio protocolos de Microsoft. Para obtener más información, vea [[ms-ERREF]: códigos de error de Windows](/openspecs/windows_protocols/ms-erref/1bc92ddf-b79e-413c-bbaa-99a5281a6c90).

## <a name="third-party-error-codes"></a>Códigos de error de terceros

Otros servicios o aplicaciones de terceros pueden generar otros códigos de error (por ejemplo, el **código de error:-118** puede aparecer en el [servicio de juego de vapor](https://support.steampowered.com/kb_cat.php?id=59)) y en esas situaciones se podría poner en contacto con la línea de soporte técnico de terceros.

## <a name="system-error-codes"></a>Códigos de error del sistema

Los códigos de error del sistema son muy amplios: cada uno de ellos puede producirse en uno de los muchos cientos de ubicaciones del sistema. Por consiguiente, las descripciones de estos códigos no pueden ser muy específicas. El uso de estos códigos requiere cierta cantidad de investigación y análisis. Debe anotar el contexto de programación y el contexto en tiempo de ejecución en el que se producen estos errores. 

Dado que estos códigos se definen en WinError. h para que los usen los usuarios, a veces los códigos los devuelve el software que no es del sistema. En ocasiones, el código es devuelto por una función de profundidad en la pila y se ha quitado de forma lejana del código que controla el error.

En los temas siguientes se proporcionan listas de códigos de error del sistema. Estos valores se definen en el archivo de encabezado WinError. h.

-   [Códigos de error del sistema (0-499) (0X0-0x1f3)](system-error-codes--0-499-.md)
-   [Códigos de error del sistema (500-999) (0x1F4-0x3e7)](system-error-codes--500-999-.md)
-   [Códigos de error del sistema (1000-1299) (0x3e8-0x513)](system-error-codes--1000-1299-.md)
-   [Códigos de error del sistema (1300-1699) (0x514-0x6a3)](system-error-codes--1300-1699-.md)
-   [Códigos de error del sistema (1700-3999) (0x6a4-0xf9f)](system-error-codes--1700-3999-.md)
-   [Códigos de error del sistema (4000-5999) (0xfa0-0x176f)](system-error-codes--4000-5999-.md)
-   [Códigos de error del sistema (6000-8199) (0x1770-0x2007)](system-error-codes--6000-8199-.md)
-   [Códigos de error del sistema (8200-8999) (0x2008-0x2327)](system-error-codes--8200-8999-.md)
-   [Códigos de error del sistema (9000-11999) (0x2328-0x2edf)](system-error-codes--9000-11999-.md)
-   [Códigos de error del sistema (12000-15999) (0x2ee0-0x3e7f)](system-error-codes--12000-15999-.md)
