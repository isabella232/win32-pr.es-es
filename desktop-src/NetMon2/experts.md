---
description: Un experto es una biblioteca de vínculos dinámicos (DLL) de Microsoft Win32 que analiza el tráfico de red recopilado por un proveedor de paquetes de red (NPP) y colocado en un archivo de captura.
ms.assetid: 57d8164e-f587-4bb9-a0b1-6094037e584c
title: Experto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf5fc0096b15d590bf70859443667f2d9969f1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666295"
---
# <a name="expert"></a><span data-ttu-id="77c58-103">Experto</span><span class="sxs-lookup"><span data-stu-id="77c58-103">Expert</span></span>

<span data-ttu-id="77c58-104">Un experto es una biblioteca de vínculos dinámicos (DLL) de Microsoft Win32 que analiza el tráfico de red recopilado por un [*proveedor de paquetes de red*](n.md) (NPP) y colocado en un archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="77c58-104">An expert is a Microsoft Win32 dynamic-link library (DLL) that analyzes network traffic collected by a [*network packet provider*](n.md) (NPP), and placed in a capture file.</span></span> <span data-ttu-id="77c58-105">Una vez que los datos se capturan y almacenan en un archivo de captura, el experto trabaja con un analizador, también denominado analizador de protocolos, para analizar los datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="77c58-105">After the data is captured and stored in a capture file, the expert works with a parser, also referred to as a protocol parser, to analyze the data in the file.</span></span> <span data-ttu-id="77c58-106">Por ejemplo, puede examinar los fotogramas del archivo de captura y usar un [*analizador*](p.md) para reconocer protocolos como el bloque de mensajes del servidor (SMB) o el protocolo de control de transmisión/Protocolo de Internet (TCP/IP).</span><span class="sxs-lookup"><span data-stu-id="77c58-106">For example, you can examine the frames of the capture file and use a [*parser*](p.md) to recognize protocols such as server message block (SMB), or Transmission Control Protocol/Internet Protocol (TCP/IP).</span></span>

<span data-ttu-id="77c58-107">Puede diseñar un experto para que funcione con todos los analizadores de Monitor de red y los analizadores que cree usted mismo.</span><span class="sxs-lookup"><span data-stu-id="77c58-107">You can design an expert to work with all of the Network Monitor parsers, and any parsers that you create yourself.</span></span>

<span data-ttu-id="77c58-108">Después de que una coincidencia solicitada de protocolos identifique un marco específico, el experto extrae los datos del marco.</span><span class="sxs-lookup"><span data-stu-id="77c58-108">After a requested match of protocols identifies a specific frame, the expert extracts data from the frame.</span></span> <span data-ttu-id="77c58-109">Puede programar el experto para manipular la información en datos que se pueden usar que muestra el Monitor de red Visor de eventos.</span><span class="sxs-lookup"><span data-stu-id="77c58-109">You can program the expert to manipulate information into usable data that the Network Monitor Event Viewer displays.</span></span>

<span data-ttu-id="77c58-110">Puede configurar un experto en tiempo de ejecución y, a continuación, usar Monitor de red para guardar los datos de configuración de usuario para su reutilización con diferentes archivos de captura.</span><span class="sxs-lookup"><span data-stu-id="77c58-110">You can configure an expert at run time, and then use Network Monitor to save user configuration data for reuse with different capture files.</span></span> <span data-ttu-id="77c58-111">Puede usar un experto para proporcionar datos de correlación y resoluciones personalizadas para los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="77c58-111">You can use an expert to provide correlation data and custom resolutions for end users.</span></span> <span data-ttu-id="77c58-112">Para obtener más información sobre la creación de información de configuración basada en HTML, vea [Página referencia de eventos](event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="77c58-112">For more information about the creation of HTML-based configuration information, see [Event Reference Page](event-reference-page.md).</span></span>

<span data-ttu-id="77c58-113">Durante la instalación de Monitor de red, se instalan los siguientes archivos dll de expertos en el subdirectorio Experts:</span><span class="sxs-lookup"><span data-stu-id="77c58-113">During Network Monitor setup, the following expert DLLs are installed in the Experts sub-directory:</span></span>

-   <span data-ttu-id="77c58-114">Coalesce.dll</span><span class="sxs-lookup"><span data-stu-id="77c58-114">Coalesce.dll</span></span>
-   <span data-ttu-id="77c58-115">Propdist.dll</span><span class="sxs-lookup"><span data-stu-id="77c58-115">Propdist.dll</span></span>
-   <span data-ttu-id="77c58-116">Protdist.dll</span><span class="sxs-lookup"><span data-stu-id="77c58-116">Protdist.dll</span></span>
-   <span data-ttu-id="77c58-117">Resptime.dll</span><span class="sxs-lookup"><span data-stu-id="77c58-117">Resptime.dll</span></span>
-   <span data-ttu-id="77c58-118">Tcpipe.dll</span><span class="sxs-lookup"><span data-stu-id="77c58-118">Tcpipe.dll</span></span>
-   <span data-ttu-id="77c58-119">Topuser.dll</span><span class="sxs-lookup"><span data-stu-id="77c58-119">Topuser.dll</span></span>

<span data-ttu-id="77c58-120">Al iniciar Monitor de red, la función [**DllMain**](dllmain-expert.md) crea todos los expertos en el subdirectorio Experts.</span><span class="sxs-lookup"><span data-stu-id="77c58-120">When you start Network Monitor, the [**DllMain**](dllmain-expert.md) function builds all experts in the experts subdirectory.</span></span> <span data-ttu-id="77c58-121">Cuando el usuario selecciona **expertos** en el menú **herramientas** de la interfaz de usuario de monitor de red, monitor de red carga los archivos dll de expertos.</span><span class="sxs-lookup"><span data-stu-id="77c58-121">When the user selects **Experts** on the **Tools** menu of the Network Monitor UI, Network Monitor loads the expert DLLs.</span></span> <span data-ttu-id="77c58-122">Se llama al experto a través del punto de entrada del [experto de registro](register-expert.md) para proporcionar los detalles básicos sobre el experto.</span><span class="sxs-lookup"><span data-stu-id="77c58-122">The expert is called through the [Register Expert](register-expert.md) entry point to provide basic details about the expert.</span></span>

![cuadro de diálogo expertos de monitor de red](images/expick.png)

<span data-ttu-id="77c58-124">Monitor de red llama a las siguientes funciones para administrar el experto:</span><span class="sxs-lookup"><span data-stu-id="77c58-124">Network Monitor calls the following functions to manage the expert:</span></span>

-   [<span data-ttu-id="77c58-125">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="77c58-125">**DllMain**</span></span>](dllmain-expert.md)
-   [<span data-ttu-id="77c58-126">**Registrar experto**</span><span class="sxs-lookup"><span data-stu-id="77c58-126">**Register Expert**</span></span>](register-expert.md)
-   [<span data-ttu-id="77c58-127">**Ejecutar**</span><span class="sxs-lookup"><span data-stu-id="77c58-127">**Run**</span></span>](run.md)
-   [<span data-ttu-id="77c58-128">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="77c58-128">**Configure**</span></span>](configure.md)

<span data-ttu-id="77c58-129">El experto debe implementar cada una de las funciones anteriores.</span><span class="sxs-lookup"><span data-stu-id="77c58-129">The expert must implement each of the preceding functions.</span></span>

 

 



