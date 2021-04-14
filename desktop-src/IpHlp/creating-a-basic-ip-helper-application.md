---
description: Cómo crear una aplicación auxiliar de IP básica.
ms.assetid: b53f1cf5-3659-407e-8279-5c94333f3017
title: Creación de una aplicación auxiliar de IP básica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baae961f8ffb6aa899e96fd05f0cb9f0c41469ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361652"
---
# <a name="creating-a-basic-ip-helper-application"></a><span data-ttu-id="1ed40-103">Creación de una aplicación auxiliar de IP básica</span><span class="sxs-lookup"><span data-stu-id="1ed40-103">Creating a Basic IP Helper Application</span></span>

<span data-ttu-id="1ed40-104">**Para crear una aplicación auxiliar de IP básica**</span><span class="sxs-lookup"><span data-stu-id="1ed40-104">**To create a basic IP Helper application**</span></span>

1.  <span data-ttu-id="1ed40-105">Cree un nuevo proyecto vacío.</span><span class="sxs-lookup"><span data-stu-id="1ed40-105">Create a new empty project.</span></span>
2.  <span data-ttu-id="1ed40-106">Agregue un archivo de código fuente de C++ vacío al proyecto.</span><span class="sxs-lookup"><span data-stu-id="1ed40-106">Add an empty C++ source file to the project.</span></span>
3.  <span data-ttu-id="1ed40-107">Asegúrese de que el entorno de compilación hace referencia a los directorios include, lib y src del kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="1ed40-107">Ensure that the build environment refers to the Include, Lib, and Src directories of the Platform Software Development Kit (SDK).</span></span>
4.  <span data-ttu-id="1ed40-108">Asegúrese de que el entorno de compilación se vincula con el archivo de biblioteca auxiliar de IP iphlpapi. lib y el archivo de biblioteca Winsock WS2 \_ 32. lib.</span><span class="sxs-lookup"><span data-stu-id="1ed40-108">Ensure that the build environment links to the IP Helper Library file Iphlpapi.lib and the Winsock Library file WS2\_32.lib.</span></span>
    > [!Note]  
    > <span data-ttu-id="1ed40-109">Algunas funciones básicas de Winsock se utilizan para devolver valores de dirección IP y otra información.</span><span class="sxs-lookup"><span data-stu-id="1ed40-109">Some basic Winsock functions are used to return IP address values and other information.</span></span>

     

5.  <span data-ttu-id="1ed40-110">Empiece a programar la aplicación auxiliar de IP.</span><span class="sxs-lookup"><span data-stu-id="1ed40-110">Begin programming the IP Helper application.</span></span> <span data-ttu-id="1ed40-111">Use la API auxiliar de IP incluyendo el archivo de encabezado de la aplicación auxiliar de IP.</span><span class="sxs-lookup"><span data-stu-id="1ed40-111">Use the IP Helper API by including the IP Helper header file.</span></span>

    ```C++
    #include <winsock2.h>
    #include <iphlpapi.h>
    #include <stdio.h>

    int main() {
      return 0;
    }
    
    ```

    

    > [!Note]
    >
    > <span data-ttu-id="1ed40-112">El archivo de encabezado *iphlpapi. h* es necesario para las aplicaciones que usan las funciones auxiliares de IP.</span><span class="sxs-lookup"><span data-stu-id="1ed40-112">The *Iphlpapi.h* header file is required for applications that use the IP Helper functions.</span></span> <span data-ttu-id="1ed40-113">El archivo de encabezado *iphlpapi. h* incluye automáticamente otros archivos de encabezados con estructuras y enumeraciones usadas por las funciones auxiliares de IP.</span><span class="sxs-lookup"><span data-stu-id="1ed40-113">The *Iphlpapi.h* header file automatically includes other headers files with structures and enumerations used by the IP Helper functions.</span></span>
    >
    > <span data-ttu-id="1ed40-114">Las nuevas funciones auxiliares de IP introducidas en Windows Vista y versiones posteriores se definen en el archivo de encabezado *Netioapi. h* que se incluye automáticamente en el archivo de encabezado *iphlpapi. h* .</span><span class="sxs-lookup"><span data-stu-id="1ed40-114">The new IP Helper functions introduced in Windows Vista and later are defined in the *Netioapi.h* header file which is automatically included by the *Iphlpapi.h* header file.</span></span> <span data-ttu-id="1ed40-115">El archivo de encabezado *Netioapi. h* nunca debe usarse directamente.</span><span class="sxs-lookup"><span data-stu-id="1ed40-115">The *Netioapi.h* header file should never be used directly.</span></span>
    >
    > <span data-ttu-id="1ed40-116">Muchas de las estructuras y enumeraciones usadas por las funciones auxiliares de IP se definen en los archivos de encabezado *Iprtrmib. h*, *Ipexport. h* y *Iptypes. h* .</span><span class="sxs-lookup"><span data-stu-id="1ed40-116">Many of the structures and enumerations used by IP Helper functions are defined in the *Iprtrmib.h*, *Ipexport.h*, and *Iptypes.h* header files.</span></span> <span data-ttu-id="1ed40-117">Estos archivos de encabezado se incluyen automáticamente en el archivo de encabezado *iphlpapi. h* y nunca deben usarse directamente.</span><span class="sxs-lookup"><span data-stu-id="1ed40-117">These header files are automatically included in the *Iphlpapi.h* header file and should never be used directly.</span></span>
    >
    > <span data-ttu-id="1ed40-118">En el kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores, la organización de los archivos de encabezado ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="1ed40-118">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed.</span></span> <span data-ttu-id="1ed40-119">Algunas de las estructuras se definen ahora en los archivos de encabezado *Ipmib. h*, *Tcpmib. h* y *Udpmib. h* , no en el archivo de encabezado *Iprtrmib. h* .</span><span class="sxs-lookup"><span data-stu-id="1ed40-119">Some of the structures are now defined in the *Ipmib.h*, *Tcpmib.h*, and *Udpmib.h* header files, not in the *Iprtrmib.h* header file.</span></span> <span data-ttu-id="1ed40-120">El archivo de encabezado *Ipmib. h* incluye automáticamente el archivo de encabezado *Ifmib. h* .</span><span class="sxs-lookup"><span data-stu-id="1ed40-120">The *Ipmib.h* header file automatically includes the *Ifmib.h* header file.</span></span> <span data-ttu-id="1ed40-121">Tenga en cuenta que estos archivos de encabezado se incluyen automáticamente en *Iprtrmib. h*, que se incluye automáticamente en el archivo de encabezado *iphlpapi. h* .</span><span class="sxs-lookup"><span data-stu-id="1ed40-121">Note that these header files are automatically included in *Iprtrmib.h*, which is automatically included in the *Iphlpapi.h* header file.</span></span>
    >
    > <span data-ttu-id="1ed40-122">La mayoría de las aplicaciones que usan las API auxiliares de IP requieren el archivo de encabezado *WinSock2. h* para Windows sockets 2,0.</span><span class="sxs-lookup"><span data-stu-id="1ed40-122">The *Winsock2.h* header file for Windows Sockets 2.0 is required by most applications using the IP Helper APIs.</span></span> <span data-ttu-id="1ed40-123">Cuando se requiere el archivo de encabezado *WinSock2. h* , la \# línea de inclusión de este archivo debe colocarse antes que la \# línea de inclusión del archivo de encabezado *iphlpapi. h* .</span><span class="sxs-lookup"><span data-stu-id="1ed40-123">When the *Winsock2.h* header file is required, the \#include line for this file should be placed before the \#include line for the *Iphlpapi.h* header file.</span></span>
    >
    > <span data-ttu-id="1ed40-124">El archivo de encabezado *WinSock2. h* incluye internamente los elementos básicos del archivo de encabezado *Windows. h* , por lo que no suele haber una \# línea de inclusión para el archivo de encabezado *Windows. h* en aplicaciones auxiliares de IP.</span><span class="sxs-lookup"><span data-stu-id="1ed40-124">The *Winsock2.h* header file internally includes core elements from the *Windows.h* header file, so there is not usually an \#include line for *Windows.h* header file in IP Helper applications.</span></span> <span data-ttu-id="1ed40-125">Si \# se necesita una línea de inclusión para el archivo de encabezado de *Windows. h* , debe ir precedida de la \# macro definir Win32 \_ lean \_ y \_ Mean.</span><span class="sxs-lookup"><span data-stu-id="1ed40-125">If an \#include line is needed for the *Windows.h* header file, this should be preceded with the \#define WIN32\_LEAN\_AND\_MEAN macro.</span></span> <span data-ttu-id="1ed40-126">Por motivos históricos, el encabezado *Windows. h* tiene como valor predeterminado el archivo de encabezado *Winsock. h* para Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="1ed40-126">For historical reasons, the *Windows.h* header defaults to including the *Winsock.h* header file for Windows Sockets 1.1.</span></span> <span data-ttu-id="1ed40-127">Las declaraciones del archivo de encabezado *Winsock. h* para Windows sockets 1,1 entrarán en conflicto con las declaraciones del archivo de encabezado *WinSock2. h* requerido por Windows Sockets 2,0.</span><span class="sxs-lookup"><span data-stu-id="1ed40-127">The declarations in the *Winsock.h* header file for Windows Sockets 1.1 will conflict with the declarations in the *Winsock2.h* header file required by Windows Sockets 2.0.</span></span> <span data-ttu-id="1ed40-128">La \_ macro lean y Mean de Win32 impide que el archivo \_ de encabezado \_ de *Windows. h* incluya el archivo de encabezado *Winsock. h* .</span><span class="sxs-lookup"><span data-stu-id="1ed40-128">The WIN32\_LEAN\_AND\_MEAN macro prevents the *Winsock.h* header file from being included by the *Windows.h* header file.</span></span> <span data-ttu-id="1ed40-129">A continuación se muestra un ejemplo que ilustra esto.</span><span class="sxs-lookup"><span data-stu-id="1ed40-129">An example illustrating this is shown below.</span></span>

     

    ```C++
    #ifndef WIN32_LEAN_AND_MEAN
    #define WIN32_LEAN_AND_MEAN
    #endif

    #include <windows.h>

    #include <winsock2.h>
    #include <iphlpapi.h>
    #include <stdio.h>

    int main() {
      return 0;
    }
    
    ```

    

    > [!Note]
    >
    > <span data-ttu-id="1ed40-130">Esta aplicación auxiliar de IP básica solo usa algunas estructuras de datos de direcciones IP y direcciones IP para las funciones de conversión de cadenas de Windows Sockets 2,0.</span><span class="sxs-lookup"><span data-stu-id="1ed40-130">This basic IP Helper application only uses some IP address data structures and IP address to string conversion functions from Windows Sockets 2.0.</span></span> <span data-ttu-id="1ed40-131">Estas funciones de Windows Sockets se pueden usar sin llamar a [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para inicializar los recursos de Windows Sockets y [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) cuando se realizan con estos recursos.</span><span class="sxs-lookup"><span data-stu-id="1ed40-131">These Windows Sockets functions can be used without calling [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) to initialize Windows Sockets resources and [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) when done using these resources.</span></span>
    >
    > <span data-ttu-id="1ed40-132">En las aplicaciones auxiliares de IP que usan otras funciones de Winsock que no son de esta dirección IP a las funciones de cadena, se debe llamar a la función [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para inicializar los recursos de Windows Sockets antes de llamar a cualquier función de Windows Sockets y se debe llamar a [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) cuando la aplicación se realiza mediante recursos de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="1ed40-132">In IP Helper applications that use other Winsock functions other than these IP address to string functions, the [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) function must be called to initialize Windows Sockets resources before calling any Windows Sockets functions and [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) should be called when the application is done using Windows Sockets resources.</span></span>

     

    > [!Note]
    >
    > <span data-ttu-id="1ed40-133">El archivo de encabezado *stdio. h* es necesario para el uso de varias funciones estándar de C en esta aplicación auxiliar de IP básica.</span><span class="sxs-lookup"><span data-stu-id="1ed40-133">The *Stdio.h* header file is required for the use of various standard C functions in this basic IP Helper application.</span></span>

     

    <span data-ttu-id="1ed40-134">Siguiente paso: [recuperar información mediante GetNetworkParams](retrieving-information-using-getnetworkparams.md)</span><span class="sxs-lookup"><span data-stu-id="1ed40-134">Next Step: [Retrieving Information Using GetNetworkParams](retrieving-information-using-getnetworkparams.md)</span></span>

 

 
