---
description: Cómo crear una aplicación Windows Sockets básicos (Winsock).
ms.assetid: 56af2e95-ea82-49e4-b335-86dcf4c38780
title: Creación de una aplicación Winsock básica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67b13acc0ae80242fb747415d457e6809895c38cd81878224cad2ffe130b2536
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860955"
---
# <a name="creating-a-basic-winsock-application"></a>Creación de una aplicación Winsock básica

**Para crear una aplicación Winsock básica**

1.  Cree un nuevo proyecto vacío.
2.  Agregue un archivo de código fuente de C++ vacío al proyecto.
3.  Asegúrese de que el entorno de compilación hace referencia a los directorios Include, Lib y Src del Kit de desarrollo de software (SDK) de Microsoft Windows o del Kit de desarrollo de software (SDK) de plataforma anterior.
4.  Asegúrese de que el entorno de compilación se vincula al archivo Ws2 32.lib de la biblioteca \_ Winsock. Las aplicaciones que usan Winsock deben vincularse con el archivo de biblioteca \_ Ws2 32.lib. El comentario pragma indica al vinculador que se necesita el archivo \# *\_ Ws2 32.lib.*
5.  Comience a programar la aplicación Winsock. Use la API de Winsock mediante la inclusión de los archivos de encabezado de Winsock 2. El *archivo de encabezado Winsock2.h* contiene la mayoría de las funciones, estructuras y definiciones de Winsock. El archivo de encabezado *Ws2tcpip.h* contiene definiciones introducidas en el documento anexo Protocol-Specific de WinSock 2 para TCP/IP que incluye funciones y estructuras más recientes que se usan para recuperar direcciones IP.
    > [!Note]  
    > Stdio.h se usa para la entrada y salida estándar, específicamente la **función printf().**

     


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



> [!Note]
>
> El *archivo de encabezado Iphlpapi.h* es necesario si una aplicación usa las API del asistente de IP. Cuando se requiere el archivo de encabezado *Iphlpapi.h,* la línea de include del archivo de encabezado Winsock2.h debe colocarse antes de la línea include del archivo de encabezado \#  \# *Iphlpapi.h.*
>
> El archivo de encabezado *Winsock2.h* incluye internamente elementos principales del archivo de encabezado *Windows.h,* por lo que normalmente no hay una línea de include para el archivo de encabezado Windows.h en las aplicaciones \# Winsock.  Si se necesita una línea de include para el archivo de encabezado Windows.h, debe ir precedida de la \# macro DEFINE  \# WIN32 LEAN AND \_ \_ \_ MEAN. Por motivos históricos, *el encabezado Windows.h* incluye de forma predeterminada el archivo de encabezado *Winsock.h* para Windows Sockets 1.1. Las declaraciones del archivo de encabezado *Winsock.h* entra en conflicto con las declaraciones del archivo de encabezado *Winsock2.h* que requiere Windows Sockets 2.0. La macro WIN32 LEAN AND MEAN impide que \_ \_ \_ *winsock.h* se incluya en *el encabezado Windows.h.* A continuación se muestra un ejemplo que ilustra esto.

 


```C++
#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <iphlpapi.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



Paso siguiente: [Inicialización de Winsock](initializing-winsock.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Acerca de servidores y clientes](about-clients-and-servers.md)
</dt> </dl>

 

 



