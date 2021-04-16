---
description: Usar la utilidad de Checkv4.exe para modificar la aplicación IPv4 para que admita IPv6.
ms.assetid: 36b72e4f-133d-4d96-a3c9-86a852d3a479
title: Usar la utilidad Checkv4.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc9eca96b2138f9950b157a4b7690dc382f273e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557350"
---
# <a name="using-the-checkv4exe-utility"></a>Usar la utilidad Checkv4.exe

> [!IMPORTANT]
> La utilidad *Checkv4.exe* no se incluye en el kit de desarrollo de software (SDK) de Windows para Windows 8 ni en versiones posteriores de la Windows SDK.

La utilidad *Checkv4.exe* está diseñada para proporcionarle un asociado de portabilidad de código; una utilidad que recorre el código base con usted, identifica posibles problemas o resalta código que podría beneficiarse de estructuras o funciones compatibles con IPv6 y realiza recomendaciones. Con la utilidad Checkv4.exe, la tarea de modificar una aplicación IPv4 existente para admitir IPv6 es mucho más fácil.

La utilidad de *Checkv4.exe* se instala como parte del kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y SDK posteriores (hasta, pero sin incluir, el kit de desarrollo de software (SDK) de Windows para Windows 8).

Una versión anterior de la utilidad *Checkv4.exe* con características más limitadas también estaba disponible como parte de la versión anterior de Microsoft IPv6 Technology Preview para Windows 2000.

En las secciones siguientes se describe cómo usar la utilidad *Checkv4.exe* y, a continuación, se explica el enfoque recomendado para modificar una aplicación IPv4 existente para que admita IPv6.

## <a name="recommendations-for-running-checkv4exe"></a>Recomendaciones para ejecutar Checkv4.exe

-   La utilidad *Checkv4.exe* es sencilla. Simplemente ejecute *Checkv4.exe* en la línea de comandos con el nombre del archivo que desea comprobar como parámetro. *Checkv4.exe* analiza el archivo y proporciona comentarios sobre dónde se encuentran los problemas de portabilidad IPv6 en ese archivo. Colocar el *Checkv4.exe* en la ruta de acceso del equipo hace que la ejecución de la utilidad de *Checkv4.exe* desde cualquier lugar de la estructura de directorios del código fuente sea mucho más fácil. Por ejemplo, la colocación de *Checkv4.exe* en% WINDIR% le permite iniciar *Checkv4.exe* desde cualquier directorio del equipo sin incluir su ruta de acceso.

-   Emita el siguiente comando en el símbolo del sistema para analizar el archivo Simplec. c:

    **Checkv4 simplec. c**

    Tenga en cuenta que algunas de las recomendaciones realizadas por la utilidad *Checkv4.exe* requieren estructuras disponibles solo en las versiones recientes del archivo de encabezado *Ws2tcpip. h* , como la estructura **\_ IN6 de SOCKADDR** . Estos archivos de encabezado se incluyen en la Windows SDK publicada para Windows Vista y versiones posteriores. Estos archivos de encabezado también se incluyen en el kit de desarrollo de software (SDK) de plataforma anterior publicado para Windows Server 2003. Estos archivos de encabezado también se incluyen como parte de una suscripción a MSDN o mediante descarga.

    En la captura de pantalla siguiente se muestran los resultados del uso de la utilidad *Checkv4.exe* en el archivo Simplec. c incluido en el Apéndice A:

    ![checkv4.exe informa de las incompatibilidades de IPv6 en el archivo simplec. c](images/portingguide002.jpg)

    En la captura de pantalla siguiente se muestran los resultados del uso de la utilidad *Checkv4.exe* en el archivo simple. c, que también se incluye en el Apéndice A:

    ![checkv4.exe informa de las incompatibilidades de IPv6 en el archivo simple. c](images/portingguide003.jpg)

## <a name="the-application-modification-process-where-to-start"></a>Proceso de modificación de la aplicación: Dónde iniciar

Existe un procedimiento recomendado asociado a la adición de funcionalidad IPv6 a las aplicaciones. Esta secuencia es beneficiosa, ya que permite a los desarrolladores asegurarse de que se realizan todos los pasos necesarios para modificar una aplicación IPv4 existente para admitir IPv6. Ciertas aplicaciones pueden requerir una atención más exhaustiva a una de estas secuencias; por ejemplo, un servicio de sistema probablemente tendrá menos problemas de interfaz de usuario que un programa de transferencia de archivos gráfico (FTP).

**Para modificar las aplicaciones IPv4 para que admitan IPv6**

1.  Corrija las estructuras y declaraciones para habilitar la compatibilidad con IPv6 e IPv4.
2.  Modifique las llamadas de función para aprovechar las funciones habilitadas para IPv6, como las funciones [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) y [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .
3.  Revise el código fuente para el uso de direcciones IPv4 codificadas de forma rígida, como la dirección de bucle invertido o el uso de otras cadenas literales.
4.  Realice una revisión completa de la interfaz de usuario, incluidos los cuadros de diálogo informativos. Piense si es adecuado para las aplicaciones habilitadas para IPv6 especificar o proporcionar información basada en direcciones IP.
5.  Determine si la aplicación se basa en protocolos subyacentes, como RPC, y realice los cambios de programación adecuados para controlar las direcciones IPv6.
6.  Use la marca de tiempo de compilación IPV6STRICT al compilar aplicaciones en Windows XP y versiones posteriores. Esta marca produce un error en la compilación de código incompatible, como se indica a continuación:

    Las aplicaciones de Windows Sockets 1. x con código incompatible no se compilan y devuelven el mensaje de error "se requiere WINSOCK2".

    Las aplicaciones de Windows Sockets 2. x con código incompatible producen un error en tiempo de compilación para cada instancia de código incompatible. Se genera un mensaje de error con el siguiente formato:

    `[file name] ([line number]) : [error message] '[symbol]_IPV6INCOMPATIBLE'`

    Por ejemplo:

    `sample.c(8) : error C2065: 'gethostbyaddr_IPV6INCOMPATIBLE' : undeclared identifier`

 

 



