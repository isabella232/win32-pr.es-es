---
description: Los archivos dll de TAPI, junto con el servidor TAPI (Tapisvr.exe), son abstracciones cruciales que separan las aplicaciones de usuario final o de servidor de los proveedores de servicios. Una DLL de TAPI junto con el servidor TAPI proporciona una interfaz coherente entre estas dos capas.
ms.assetid: 17937bf1-e0bd-4845-9484-d23190807642
title: DLL DE TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8482045ec16a999957121aff669e93b34b605069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104560217"
---
# <a name="tapi-dll"></a><span data-ttu-id="9fa6a-104">DLL DE TAPI</span><span class="sxs-lookup"><span data-stu-id="9fa6a-104">TAPI DLL</span></span>

<span data-ttu-id="9fa6a-105">Los archivos dll de TAPI, junto con el servidor TAPI (Tapisvr.exe), son abstracciones cruciales que separan las aplicaciones de usuario final o de servidor de los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-105">The TAPI DLLs, along with the TAPI Server (Tapisvr.exe), are crucial abstractions separating end-user or server applications from service providers.</span></span> <span data-ttu-id="9fa6a-106">Una DLL de TAPI junto con el servidor TAPI proporciona una interfaz coherente entre estas dos capas.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-106">A TAPI DLL in conjunction with the TAPI Server provides a consistent interface between these two layers.</span></span>

<span data-ttu-id="9fa6a-107">Una aplicación TAPI carga el archivo DLL adecuado en su espacio de proceso.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-107">A TAPI application loads the appropriate DLL into its process space.</span></span> <span data-ttu-id="9fa6a-108">Durante la inicialización, TAPI establece un vínculo RPC con Tapisvr.exe.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-108">During initialization, TAPI establishes an RPC link with Tapisvr.exe.</span></span> <span data-ttu-id="9fa6a-109">El servidor TAPI se ejecuta en el contexto de SVCHOST.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-109">The TAPI Server runs in the context of SVCHOST.</span></span>

<span data-ttu-id="9fa6a-110">Hay tres dll asociadas a TAPI: Tapi.dll, Tapi32.dll y Tapi3.dll.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-110">There are three DLLs associated with TAPI: Tapi.dll, Tapi32.dll, and Tapi3.dll.</span></span> <span data-ttu-id="9fa6a-111">Estos archivos DLL se encuentran en% SystemRoot% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-111">These DLLs are located in %SystemRoot%\\system32.</span></span> <span data-ttu-id="9fa6a-112">En la ilustración siguiente se muestran los roles de sus respectivos roles en telefonía de Microsoft:</span><span class="sxs-lookup"><span data-stu-id="9fa6a-112">The following figure illustrates the roles of their respective roles in Microsoft Telephony:</span></span>

![roles de los tres archivos dll de TAPI](images/dllserv.png)

<span data-ttu-id="9fa6a-114">Las aplicaciones de 16 bits existentes se vinculan a Tapi.dll.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-114">Existing 16-bit applications link to Tapi.dll.</span></span> <span data-ttu-id="9fa6a-115">Tapi.dll es simplemente una capa de código thunk que asigna direcciones de 16 bits a direcciones de 32 bits y solicitudes de paso a Tapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-115">Tapi.dll is simply a thunk layer that maps 16-bit addresses to 32-bit addresses and pass requests to Tapi32.dll.</span></span>

<span data-ttu-id="9fa6a-116">Las aplicaciones TAPI 2. x de 32 bits existentes se vinculan a Tapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-116">Existing 32-bit TAPI 2.x applications link to Tapi32.dll.</span></span> <span data-ttu-id="9fa6a-117">Tapi32.dll es una capa de serialización fina que transfiere las solicitudes de función al servidor TAPI (TAPISRV) y, cuando sea necesario, carga e invoca los archivos DLL del proveedor de servicios multimedia en el proceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-117">Tapi32.dll is a thin marshalling layer that transfers function requests to the TAPI Server (TAPISRV) and, when needed, loads and invokes media service provider DLLs in the application's process.</span></span>

<span data-ttu-id="9fa6a-118">Las aplicaciones TAPI 3. x se vinculan a Tapi3.dll.</span><span class="sxs-lookup"><span data-stu-id="9fa6a-118">TAPI 3.x applications link to Tapi3.dll.</span></span>

 

 



