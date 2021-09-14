---
description: Usar la Checkv4.exe para modificar la aplicación IPv4 para admitir IPv6.
ms.assetid: 36b72e4f-133d-4d96-a3c9-86a852d3a479
title: Uso de la utilidad Checkv4.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc9eca96b2138f9950b157a4b7690dc382f273e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242282"
---
# <a name="using-the-checkv4exe-utility"></a>Uso de la utilidad Checkv4.exe

> [!IMPORTANT]
> La *utilidadCheckv4.exe* no se incluye en el Kit de desarrollo de software (SDK) de Windows para Windows 8 ni en versiones posteriores del SDK Windows.

La *utilidadCheckv4.exe* está diseñada para proporcionarle un asociado de porte de código; una utilidad que realiza un paso a través de la base de código con usted, identifica posibles problemas o resalta el código que podría beneficiarse de las funciones o estructuras compatibles con IPv6, y hace recomendaciones. Con la Checkv4.exe, la tarea de modificar una aplicación IPv4 existente para admitir IPv6 es mucho más fácil.

La *utilidadCheckv4.exe* se instala como parte del Kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y sdk posteriores (hasta el Kit de desarrollo de software (SDK) de Windows para Windows 8.

Una versión anterior de la utilidad *Checkv4.exe* con características más limitadas también estaba disponible como parte de la versión preliminar de tecnología IPv6 de Microsoft anterior para Windows 2000.

En las secciones siguientes se describe cómo usar la utilidadCheckv4.exey, *a* continuación, se explica el enfoque recomendado para modificar una aplicación IPv4 existente para admitir IPv6.

## <a name="recommendations-for-running-checkv4exe"></a>Recomendaciones para ejecutar Checkv4.exe

-   La *Checkv4.exe* es sencilla. Simplemente ejecute *Checkv4.exe* en la línea de comandos con el nombre del archivo que desea comprobar como parámetro. *Checkv4.exe* analiza el archivo y proporciona comentarios sobre dónde existen problemas de porte de IPv6 en ese archivo. La *colocación deCheckv4.exe* en la ruta de acceso del equipo facilita mucho la ejecución de la utilidad *Checkv4.exe* desde cualquier lugar de la estructura de directorios del código fuente. Por ejemplo, colocar *Checkv4.exe* %windir% le permite  iniciarCheckv4.exedesde cualquier directorio del equipo sin incluir su ruta de acceso.

-   Emita el siguiente comando en el símbolo del sistema para analizar el archivo Simplec.c:

    **Checkv4 simplec.c**

    Tenga en cuenta que algunas de las recomendaciones realizadas por la utilidad *Checkv4.exe* requieren estructuras disponibles solo en versiones recientes del archivo de encabezado *Ws2tcpip.h,* como la estructura **SOCKADDR \_ IN6.** Estos archivos de encabezado se incluyen en el SDK de Windows publicado para Windows Vista y versiones posteriores. Estos archivos de encabezado también se incluyen en el kit de desarrollo de software (SDK) de plataforma anterior publicado para Windows Server 2003. Estos archivos de encabezado también se incluyen como parte de una suscripción a MSDN o mediante descarga.

    En la siguiente captura de pantalla se muestran los resultados del uso de *la utilidadCheckv4.exe* en el archivo Simplec.c incluido en el Apéndice A:

    ![checkv4.exe incompatibilidades de ipv6 en el archivo simplec.c](images/portingguide002.jpg)

    En la captura de pantalla siguiente se muestran los resultados del uso de la utilidad *Checkv4.exe* en el archivo Simples.c, que también se incluye en el Apéndice A:

    ![checkv4.exe informes de incompatibilidades de ipv6 en el archivo simples.c](images/portingguide003.jpg)

## <a name="the-application-modification-process-where-to-start"></a>Proceso de modificación de la aplicación: Dónde empezar

Hay un procedimiento recomendado asociado a la adición de la funcionalidad IPv6 a las aplicaciones. Seguir esta secuencia es beneficioso, ya que permite a los desarrolladores asegurarse de que se toman todos los pasos necesarios para modificar una aplicación IPv4 existente para admitir IPv6. Algunas aplicaciones pueden requerir una atención más exhaustiva a una de estas secuencias. Por ejemplo, un servicio del sistema probablemente tendría menos problemas de interfaz de usuario que un programa gráfico de transferencia de archivos (FTP).

**Para modificar aplicaciones IPv4 para admitir IPv6**

1.  Corrija las estructuras y declaraciones para habilitar la compatibilidad con IPv6 e IPv4.
2.  Modifique las llamadas de función para aprovechar las funciones habilitadas para IPv6, como las funciones [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) [**y getnameinfo.**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
3.  Revise el código fuente para el uso de direcciones IPv4 codificadas de forma hard-code, como la dirección de bucleback o el uso de otras cadenas literales.
4.  Realice una revisión exhaustiva de la interfaz de usuario, incluidos los cuadros de diálogo informativos. Reflexión sobre si es adecuado que las aplicaciones habilitadas para IPv6 especifiquen o proporcionen información basada en direcciones IP.
5.  Determine si la aplicación se basa en protocolos subyacentes, como RPC, y realice los cambios mediante programación adecuados para controlar las direcciones IPv6.
6.  Use la marca de tiempo de compilación IPV6STRICT al compilar aplicaciones en Windows XP y versiones posteriores. Esta marca provoca que el código incompatible no se compile, como se muestra a continuación:

    Windows Las aplicaciones sockets 1.x con código incompatible no se pueden compilar y devolver el mensaje de error "WINSOCK2 Required".

    Windows Las aplicaciones sockets 2.x con código incompatible provocan un error de tiempo de compilación para cada instancia de código incompatible. Se genera un mensaje de error en el formato siguiente:

    `[file name] ([line number]) : [error message] '[symbol]_IPV6INCOMPATIBLE'`

    Por ejemplo:

    `sample.c(8) : error C2065: 'gethostbyaddr_IPV6INCOMPATIBLE' : undeclared identifier`

 

 



