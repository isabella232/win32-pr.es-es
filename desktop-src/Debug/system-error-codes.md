---
description: Proporciona vínculos a códigos de error del sistema definidos en el archivo de encabezado WinError.h y está pensado para desarrolladores.
ms.assetid: 4a3a8feb-a05f-4614-8f04-1f507da7e5b7
title: Códigos de error del sistema
ms.topic: article
ms.date: 10/31/2019
ms.openlocfilehash: 072e1eb4a43c787055bc2793b3f58d69cdf6dd12
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164566"
---
# <a name="system-error-codes"></a>Códigos de error del sistema

Esta sección está pensada para desarrolladores que depuran errores del sistema. Si ha llegado a esta página al buscar otros errores, estos son algunos vínculos que pueden ayudar:

* [Windows errores de actualización:](https://support.microsoft.com/help/10164/fix-windows-update-errors) para obtener ayuda para resolver problemas con Windows Update.
* [Windows errores de activación:](https://support.microsoft.com/help/10738/windows-10-get-help-with-activation-errors) para obtener ayuda para comprobar la copia de Windows.
* [Solución de problemas de errores de pantalla azul:](https://support.microsoft.com/help/14238/windows-10-troubleshoot-blue-screen-errors) para obtener ayuda para detectar lo que produjo un error de detenerse.
* [Soporte técnico de Microsoft:](https://support.microsoft.com) para obtener soporte técnico con un producto de Microsoft.

## <a name="more-ways-to-find-an-error-code"></a>Más maneras de encontrar un código de error

Hemos enumerado los códigos de error del sistema en esta sección, organizados por número. Si necesita más ayuda para realizar el seguimiento de un error específico, estas son algunas recomendaciones más:

* Use la [Herramienta de búsqueda de errores de Microsoft](system-error-code-lookup-tool.md).
*  Instale las herramientas de depuración para Windows, cargue un archivo de volcado de memoria y, a continuación, ejecute el **\! comando err. \<code>**
* Busque el texto sin formato o el código de error en el sitio protocolos de Microsoft. Para obtener más información, [vea [MS-ERREF]: Windows códigos de error .](/openspecs/windows_protocols/ms-erref/1bc92ddf-b79e-413c-bbaa-99a5281a6c90)

## <a name="third-party-error-codes"></a>Códigos de error de terceros

Otros códigos de error pueden generarse mediante servicios o aplicaciones de terceros (por ejemplo, Código de **error: -118** puede mostrarse por el servicio de juegos [de Steam)](https://support.steampowered.com/kb_cat.php?id=59)y, en esas situaciones, se pondrá en contacto con la línea de soporte técnico de terceros.

## <a name="system-error-codes"></a>Códigos de error del sistema

Los códigos de error del sistema son muy amplios: cada uno puede producirse en uno de los cientos de ubicaciones del sistema. Por lo tanto, las descripciones de estos códigos no pueden ser muy específicas. El uso de estos códigos requiere cierta cantidad de investigación y análisis. Debe tener en cuenta tanto el contexto de programación como el contexto en tiempo de ejecución en el que se producen estos errores. 

Dado que estos códigos se definen en WinError.h para que cualquiera los use, a veces los devuelve software que no es del sistema. Y, a veces, el código lo devuelve una función profunda en la pila y lejos del código que está controlando el error.

En los temas siguientes se proporcionan listas de códigos de error del sistema. Estos valores se definen en el archivo de encabezado WinError.h.

-   [Códigos de error del sistema (0-499) (0x0-0x1f3)](system-error-codes--0-499-.md)
-   [Códigos de error del sistema (500-999) (0x1f4-0x3e7)](system-error-codes--500-999-.md)
-   [Códigos de error del sistema (1000-1299) (0x3e8-0x513)](system-error-codes--1000-1299-.md)
-   [Códigos de error del sistema (1300-1699) (0x514-0x6a3)](system-error-codes--1300-1699-.md)
-   [Códigos de error del sistema (1700-3999) (0x6a4-0xf9f)](system-error-codes--1700-3999-.md)
-   [Códigos de error del sistema (4000-5999) (0xfa0-0x176f)](system-error-codes--4000-5999-.md)
-   [Códigos de error del sistema (6000-8199) (0x1770-0x2007)](system-error-codes--6000-8199-.md)
-   [Códigos de error del sistema (8200-8999) (0x2008-0x2327)](system-error-codes--8200-8999-.md)
-   [Códigos de error del sistema (9000-11999) (0x2328-0x2edf)](system-error-codes--9000-11999-.md)
-   [Códigos de error del sistema (12000-15999) (0x2ee0-0x3e7f)](system-error-codes--12000-15999-.md)
