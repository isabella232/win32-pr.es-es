---
description: Todos los procesos (aplicaciones o archivos dll) que llaman a funciones Winsock deben inicializar el uso de la DLL de Windows Sockets antes de realizar otras llamadas a funciones Winsock. Esto también garantiza que Winsock sea compatible con el sistema.
ms.assetid: 300858d8-bed3-4a3c-abb5-2cecd100e5d7
title: Inicializando Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d3d02805c684c677c4358cf79c421d6a577f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541571"
---
# <a name="initializing-winsock"></a><span data-ttu-id="2d05b-104">Inicializando Winsock</span><span class="sxs-lookup"><span data-stu-id="2d05b-104">Initializing Winsock</span></span>

<span data-ttu-id="2d05b-105">Todos los procesos (aplicaciones o archivos dll) que llaman a funciones Winsock deben inicializar el uso de la DLL de Windows Sockets antes de realizar otras llamadas a funciones Winsock.</span><span class="sxs-lookup"><span data-stu-id="2d05b-105">All processes (applications or DLLs) that call Winsock functions must initialize the use of the Windows Sockets DLL before making other Winsock functions calls.</span></span> <span data-ttu-id="2d05b-106">Esto también garantiza que Winsock sea compatible con el sistema.</span><span class="sxs-lookup"><span data-stu-id="2d05b-106">This also makes certain that Winsock is supported on the system.</span></span>

<span data-ttu-id="2d05b-107">**Para inicializar Winsock**</span><span class="sxs-lookup"><span data-stu-id="2d05b-107">**To initialize Winsock**</span></span>

1.  <span data-ttu-id="2d05b-108">Cree un objeto [**wsadata (**](/windows/desktop/api/winsock/ns-winsock-wsadata) denominado wsadata (.</span><span class="sxs-lookup"><span data-stu-id="2d05b-108">Create a [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) object called wsaData.</span></span>
    ```C++
    WSADATA wsaData;
    ```

    

2.  <span data-ttu-id="2d05b-109">Llame a [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) y devuelva su valor como un entero y compruebe si hay errores.</span><span class="sxs-lookup"><span data-stu-id="2d05b-109">Call [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) and return its value as an integer and check for errors.</span></span>
    ```C++
    int iResult;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2,2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }
    ```

    

<span data-ttu-id="2d05b-110">Se llama a la función [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para iniciar el uso de WS2 \_32.dll.</span><span class="sxs-lookup"><span data-stu-id="2d05b-110">The [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) function is called to initiate use of WS2\_32.dll.</span></span>

<span data-ttu-id="2d05b-111">La estructura [**wsadata (**](/windows/desktop/api/winsock/ns-winsock-wsadata) contiene información sobre la implementación de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="2d05b-111">The [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) structure contains information about the Windows Sockets implementation.</span></span> <span data-ttu-id="2d05b-112">El parámetro MAKEWORD (2, 2) de [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) realiza una solicitud de la versión 2,2 de Winsock en el sistema y establece la versión pasada como la versión más alta de compatibilidad de Windows Sockets que puede usar el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="2d05b-112">The MAKEWORD(2,2) parameter of [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) makes a request for version 2.2 of Winsock on the system, and sets the passed version as the highest version of Windows Sockets support that the caller can use.</span></span>

<span data-ttu-id="2d05b-113">Siguiente paso para un cliente: [crear un socket para el cliente](creating-a-socket-for-the-client.md)</span><span class="sxs-lookup"><span data-stu-id="2d05b-113">Next Step for a Client: [Creating a Socket for the Client](creating-a-socket-for-the-client.md)</span></span>

<span data-ttu-id="2d05b-114">Siguiente paso para un servidor: [crear un socket para el servidor](creating-a-socket-for-the-server.md)</span><span class="sxs-lookup"><span data-stu-id="2d05b-114">Next Step for a Server: [Creating a Socket for the Server](creating-a-socket-for-the-server.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d05b-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2d05b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d05b-116">Introducción con Winsock</span><span class="sxs-lookup"><span data-stu-id="2d05b-116">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="2d05b-117">Crear una aplicación de Winsock básica</span><span class="sxs-lookup"><span data-stu-id="2d05b-117">Creating a Basic Winsock Application</span></span>](creating-a-basic-winsock-application.md)
</dt> </dl>

 

 



