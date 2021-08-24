---
description: Proporciona vínculos a códigos de error del sistema definidos en el archivo de encabezado WinError.h y está destinado a desarrolladores.
ms.assetid: 4a3a8feb-a05f-4614-8f04-1f507da7e5b7
title: Códigos de error del sistema
ms.topic: article
ms.date: 10/31/2019
ms.openlocfilehash: 4c762b2098531ecb19ad84522f8c9c8272c004397bbc4b32f15a6f6e157c4332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691735"
---
# <a name="system-error-codes"></a>Códigos de error del sistema

Esta sección está pensada para desarrolladores que están depurando errores del sistema. Si llegó a esta página al buscar otros errores, estos son algunos vínculos que pueden ayudar:

* [Windows errores de actualización:](https://support.microsoft.com/help/10164/fix-windows-update-errors) para obtener ayuda para resolver problemas con Windows update.
* [Windows errores de activación:](https://support.microsoft.com/help/10738/windows-10-get-help-with-activation-errors) para obtener ayuda para comprobar la copia de Windows.
* [Solución de errores de pantalla azul:](https://support.microsoft.com/help/14238/windows-10-troubleshoot-blue-screen-errors) para obtener ayuda para detectar lo que produjo un error de detección.
* [Soporte técnico de Microsoft:](https://support.microsoft.com) para obtener soporte técnico con un producto de Microsoft.

## <a name="more-ways-to-find-an-error-code"></a>Más formas de encontrar un código de error

Hemos enumerado los códigos de error del sistema en esta sección, organizados por número. Si necesita más ayuda para realizar el seguimiento de un error específico, estas son algunas recomendaciones más:

* Use la [herramienta de búsqueda de errores de Microsoft](system-error-code-lookup-tool.md).
*  Instale las herramientas de depuración para Windows, cargue un archivo de volcado de memoria y, a continuación, ejecute el **\! comando err. \<code>**
* Busque en el sitio protocolos de Microsoft el texto sin formato o el código de error. Para obtener más información, [vea [MS-ERREF]: Windows códigos de error .](/openspecs/windows_protocols/ms-erref/1bc92ddf-b79e-413c-bbaa-99a5281a6c90)

## <a name="third-party-error-codes"></a>Códigos de error de terceros

Otras aplicaciones o servicios de terceros pueden generar otros códigos de error (por ejemplo, Código de **error: -118** se puede mostrar en el servicio de juegos [de Steam)](https://support.steampowered.com/kb_cat.php?id=59)y, en esas situaciones, se pondrá en contacto con la línea de soporte técnico del tercero.

## <a name="system-error-codes"></a>Códigos de error del sistema

Los códigos de error del sistema son muy amplios: cada uno de ellos puede producirse en una de las muchas cientos de ubicaciones del sistema. Por lo tanto, las descripciones de estos códigos no pueden ser muy específicas. El uso de estos códigos requiere cierta cantidad de investigación y análisis. Debe tener en cuenta tanto el contexto de programación como el contexto de tiempo de ejecución en el que se producen estos errores. 

Dado que estos códigos se definen en WinError.h para que cualquiera los use, a veces los códigos los devuelve software que no es del sistema. Y, a veces, el código lo devuelve una función profunda en la pila y se quita lejos del código que está controlando el error.

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
