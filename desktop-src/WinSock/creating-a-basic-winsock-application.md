---
description: Cómo crear una aplicación básica de Windows Sockets (Winsock).
ms.assetid: 56af2e95-ea82-49e4-b335-86dcf4c38780
title: Crear una aplicación de Winsock básica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d5b5695ddb3b329bb4f81da6149fcf740a4240
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154291"
---
# <a name="creating-a-basic-winsock-application"></a>Crear una aplicación de Winsock básica

**Para crear una aplicación de Winsock básica**

1.  Cree un nuevo proyecto vacío.
2.  Agregue un archivo de código fuente de C++ vacío al proyecto.
3.  Asegúrese de que el entorno de compilación hace referencia a los directorios include, lib y src del kit de desarrollo de software (SDK) de Microsoft Windows o del kit de desarrollo de software (SDK) de plataforma anterior.
4.  Asegúrese de que el entorno de compilación se vincula al archivo de biblioteca Winsock Ws2 \_ 32. lib. Las aplicaciones que usan Winsock deben estar vinculadas al \_ archivo de biblioteca Ws2 32. lib. El \# Comentario de pragma indica al vinculador que el archivo *Ws2 \_ 32. lib* es necesario.
5.  Empiece a programar la aplicación Winsock. Use la API de Winsock incluyendo los archivos de encabezado Winsock 2. El archivo de encabezado *WinSock2. h* contiene la mayoría de las funciones, estructuras y definiciones de Winsock. El archivo de encabezado *Ws2tcpip. h* contiene las definiciones introducidas en el documento WinSock 2 Protocol-Specific anexo para TCP/IP que incluye las funciones y estructuras más recientes que se usan para recuperar direcciones IP.
    > [!Note]  
    > Stdio. h se utiliza para la entrada y salida estándar, específicamente la función **printf ()** .

     


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
> El archivo de encabezado *iphlpapi. h* es necesario si una aplicación usa las API auxiliares de IP. Cuando se requiere el archivo de encabezado *iphlpapi. h* , la \# línea de inclusión del archivo de encabezado *WinSock2. h* debe colocarse antes de la \# línea de inclusión del archivo de encabezado *iphlpapi. h* .
>
> El archivo de encabezado *WinSock2. h* incluye internamente los elementos básicos del archivo de encabezado *Windows. h* , por lo que no suele haber una \# línea de inclusión para el archivo de encabezado *Windows. h* en aplicaciones Winsock. Si \# se necesita una línea de inclusión para el archivo de encabezado de *Windows. h* , debe ir precedida de la \# macro definir Win32 \_ lean \_ y \_ Mean. Por motivos históricos, el encabezado *Windows. h* tiene como valor predeterminado el archivo de encabezado *Winsock. h* para Windows Sockets 1,1. Las declaraciones del archivo de encabezado *Winsock. h* entrarán en conflicto con las declaraciones del archivo de encabezado *WinSock2. h* requerido por Windows Sockets 2,0. La \_ macro lean \_ y \_ Mean de Win32 evita que se incluya *Winsock. h* en el encabezado de *Windows. h* . A continuación se muestra un ejemplo que ilustra esto.

 


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



Paso siguiente: [inicializando Winsock](initializing-winsock.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Acerca de los servidores y clientes](about-clients-and-servers.md)
</dt> </dl>

 

 



