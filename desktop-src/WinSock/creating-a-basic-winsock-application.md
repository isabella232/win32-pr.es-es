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
# <a name="creating-a-basic-winsock-application"></a><span data-ttu-id="9f063-103">Crear una aplicación de Winsock básica</span><span class="sxs-lookup"><span data-stu-id="9f063-103">Creating a Basic Winsock Application</span></span>

<span data-ttu-id="9f063-104">**Para crear una aplicación de Winsock básica**</span><span class="sxs-lookup"><span data-stu-id="9f063-104">**To create a basic Winsock application**</span></span>

1.  <span data-ttu-id="9f063-105">Cree un nuevo proyecto vacío.</span><span class="sxs-lookup"><span data-stu-id="9f063-105">Create a new empty project.</span></span>
2.  <span data-ttu-id="9f063-106">Agregue un archivo de código fuente de C++ vacío al proyecto.</span><span class="sxs-lookup"><span data-stu-id="9f063-106">Add an empty C++ source file to the project.</span></span>
3.  <span data-ttu-id="9f063-107">Asegúrese de que el entorno de compilación hace referencia a los directorios include, lib y src del kit de desarrollo de software (SDK) de Microsoft Windows o del kit de desarrollo de software (SDK) de plataforma anterior.</span><span class="sxs-lookup"><span data-stu-id="9f063-107">Ensure that the build environment refers to the Include, Lib, and Src directories of the Microsoft Windows Software Development Kit (SDK) or the earlier Platform Software Development Kit (SDK).</span></span>
4.  <span data-ttu-id="9f063-108">Asegúrese de que el entorno de compilación se vincula al archivo de biblioteca Winsock Ws2 \_ 32. lib.</span><span class="sxs-lookup"><span data-stu-id="9f063-108">Ensure that the build environment links to the Winsock Library file Ws2\_32.lib.</span></span> <span data-ttu-id="9f063-109">Las aplicaciones que usan Winsock deben estar vinculadas al \_ archivo de biblioteca Ws2 32. lib.</span><span class="sxs-lookup"><span data-stu-id="9f063-109">Applications that use Winsock must be linked with the Ws2\_32.lib library file.</span></span> <span data-ttu-id="9f063-110">El \# Comentario de pragma indica al vinculador que el archivo *Ws2 \_ 32. lib* es necesario.</span><span class="sxs-lookup"><span data-stu-id="9f063-110">The \#pragma comment indicates to the linker that the *Ws2\_32.lib* file is needed.</span></span>
5.  <span data-ttu-id="9f063-111">Empiece a programar la aplicación Winsock.</span><span class="sxs-lookup"><span data-stu-id="9f063-111">Begin programming the Winsock application.</span></span> <span data-ttu-id="9f063-112">Use la API de Winsock incluyendo los archivos de encabezado Winsock 2.</span><span class="sxs-lookup"><span data-stu-id="9f063-112">Use the Winsock API by including the Winsock 2 header files.</span></span> <span data-ttu-id="9f063-113">El archivo de encabezado *WinSock2. h* contiene la mayoría de las funciones, estructuras y definiciones de Winsock.</span><span class="sxs-lookup"><span data-stu-id="9f063-113">The *Winsock2.h* header file contains most of the Winsock functions, structures, and definitions.</span></span> <span data-ttu-id="9f063-114">El archivo de encabezado *Ws2tcpip. h* contiene las definiciones introducidas en el documento WinSock 2 Protocol-Specific anexo para TCP/IP que incluye las funciones y estructuras más recientes que se usan para recuperar direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="9f063-114">The *Ws2tcpip.h* header file contains definitions introduced in the WinSock 2 Protocol-Specific Annex document for TCP/IP that includes newer functions and structures used to retrieve IP addresses.</span></span>
    > [!Note]  
    > <span data-ttu-id="9f063-115">Stdio. h se utiliza para la entrada y salida estándar, específicamente la función **printf ()** .</span><span class="sxs-lookup"><span data-stu-id="9f063-115">Stdio.h is used for standard input and output, specifically the **printf()** function.</span></span>

     


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
> <span data-ttu-id="9f063-116">El archivo de encabezado *iphlpapi. h* es necesario si una aplicación usa las API auxiliares de IP.</span><span class="sxs-lookup"><span data-stu-id="9f063-116">The *Iphlpapi.h* header file is required if an application is using the IP Helper APIs.</span></span> <span data-ttu-id="9f063-117">Cuando se requiere el archivo de encabezado *iphlpapi. h* , la \# línea de inclusión del archivo de encabezado *WinSock2. h* debe colocarse antes de la \# línea de inclusión del archivo de encabezado *iphlpapi. h* .</span><span class="sxs-lookup"><span data-stu-id="9f063-117">When the *Iphlpapi.h* header file is required, the \#include line for the *Winsock2.h* header file should be placed before the \#include line for the *Iphlpapi.h* header file.</span></span>
>
> <span data-ttu-id="9f063-118">El archivo de encabezado *WinSock2. h* incluye internamente los elementos básicos del archivo de encabezado *Windows. h* , por lo que no suele haber una \# línea de inclusión para el archivo de encabezado *Windows. h* en aplicaciones Winsock.</span><span class="sxs-lookup"><span data-stu-id="9f063-118">The *Winsock2.h* header file internally includes core elements from the *Windows.h* header file, so there is not usually an \#include line for the *Windows.h* header file in Winsock applications.</span></span> <span data-ttu-id="9f063-119">Si \# se necesita una línea de inclusión para el archivo de encabezado de *Windows. h* , debe ir precedida de la \# macro definir Win32 \_ lean \_ y \_ Mean.</span><span class="sxs-lookup"><span data-stu-id="9f063-119">If an \#include line is needed for the *Windows.h* header file, this should be preceded with the \#define WIN32\_LEAN\_AND\_MEAN macro.</span></span> <span data-ttu-id="9f063-120">Por motivos históricos, el encabezado *Windows. h* tiene como valor predeterminado el archivo de encabezado *Winsock. h* para Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="9f063-120">For historical reasons, the *Windows.h* header defaults to including the *Winsock.h* header file for Windows Sockets 1.1.</span></span> <span data-ttu-id="9f063-121">Las declaraciones del archivo de encabezado *Winsock. h* entrarán en conflicto con las declaraciones del archivo de encabezado *WinSock2. h* requerido por Windows Sockets 2,0.</span><span class="sxs-lookup"><span data-stu-id="9f063-121">The declarations in the *Winsock.h* header file will conflict with the declarations in the *Winsock2.h* header file required by Windows Sockets 2.0.</span></span> <span data-ttu-id="9f063-122">La \_ macro lean \_ y \_ Mean de Win32 evita que se incluya *Winsock. h* en el encabezado de *Windows. h* .</span><span class="sxs-lookup"><span data-stu-id="9f063-122">The WIN32\_LEAN\_AND\_MEAN macro prevents the *Winsock.h* from being included by the *Windows.h* header.</span></span> <span data-ttu-id="9f063-123">A continuación se muestra un ejemplo que ilustra esto.</span><span class="sxs-lookup"><span data-stu-id="9f063-123">An example illustrating this is shown below.</span></span>

 


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



<span data-ttu-id="9f063-124">Paso siguiente: [inicializando Winsock](initializing-winsock.md)</span><span class="sxs-lookup"><span data-stu-id="9f063-124">Next Step: [Initializing Winsock](initializing-winsock.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f063-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9f063-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f063-126">Introducción con Winsock</span><span class="sxs-lookup"><span data-stu-id="9f063-126">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="9f063-127">Acerca de los servidores y clientes</span><span class="sxs-lookup"><span data-stu-id="9f063-127">About Servers and Clients</span></span>](about-clients-and-servers.md)
</dt> </dl>

 

 



