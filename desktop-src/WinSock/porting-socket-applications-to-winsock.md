---
description: En esta sección se describen las consideraciones de portabilidad de Winsock.
ms.assetid: 41c0c98e-3990-4600-ab9f-fa87edbea402
title: Trasladar aplicaciones de socket a Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2b3480d5572405d33b3a3532892a48633caa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715115"
---
# <a name="porting-socket-applications-to-winsock"></a>Trasladar aplicaciones de socket a Winsock

En esta sección se describen las consideraciones de portabilidad de Winsock.

Hay un número limitado de instancias en las que Windows Sockets se desvía del cumplimiento estricto de las convenciones de Berkeley, normalmente debido a las dificultades de implementación en el entorno de Microsoft Windows.

Cuando se produce una desviación de las convenciones de Berkeley en Windows Sockets, la desviación se indica específicamente y claramente. Por ejemplo, si una función es específica de Windows Sockets, esa desviación se especifica con una frase en la descripción de la función similar a la siguiente:

La función **\[ de nombre \] de función** es una extensión específica de Microsoft para la API de Windows Sockets 2.

En esta sección se proporciona información sobre cómo migrar aplicaciones de sockets de UNIX Berkeley (BSD) a Winsock:

-   [Tipo de datos socket](socket-data-type-2.md)
-   [Macros Select, FD \_ set y FD \_ XXX](select-and-fd---2.md)
-   [Códigos de error: errno, h \_ errno y WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
-   [Punteros](pointers-2.md)
-   [Funciones cuyo nombre ha cambiado](renamed-functions-2.md)
-   [Número máximo de sockets admitidos](maximum-number-of-sockets-supported-2.md)
-   [Archivos de inclusión](include-files-2.md)
-   [Valores devueltos en un error de función](return-values-on-function-failure-2.md)
-   [Sockets sin formato](service-provided-raw-sockets-2.md)
-   [Ordenación de bytes](byte-ordering-2.md)
-   [Rutinas de conversión extendida Byte-Order](extended-byte-order-conversion-routines-2.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de errores de Winsock](handling-winsock-errors.md)
</dt> <dt>

[Trasladar aplicaciones de socket a Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Códigos de error de Windows Sockets](windows-sockets-error-codes-2.md)
</dt> <dt>

[Consideraciones sobre la programación de Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



