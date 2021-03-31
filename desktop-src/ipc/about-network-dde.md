---
description: DDE de red se usa para iniciar y mantener las conexiones de red necesarias para las conversaciones DDE entre aplicaciones que se ejecutan en equipos diferentes en una red.
ms.assetid: f9eee391-2b4a-4c17-bea5-72cda5124e1c
title: Acerca de DDE de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412971f6bef8d2782dce38b5aef413e4d073f6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360616"
---
# <a name="about-network-dde"></a><span data-ttu-id="ac639-103">Acerca de DDE de red</span><span class="sxs-lookup"><span data-stu-id="ac639-103">About Network DDE</span></span>

<span data-ttu-id="ac639-104">\[Ya no se admite DDE de red.</span><span class="sxs-lookup"><span data-stu-id="ac639-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="ac639-105">Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="ac639-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="ac639-106">DDE de red se usa para iniciar y mantener las conexiones de red necesarias para las conversaciones DDE entre aplicaciones que se ejecutan en equipos diferentes en una red.</span><span class="sxs-lookup"><span data-stu-id="ac639-106">Network DDE is used to initiate and maintain the network connections needed for DDE conversations between applications running on different computers in a network.</span></span> <span data-ttu-id="ac639-107">Una *conversación* DDE es la interacción entre las aplicaciones cliente y servidor.</span><span class="sxs-lookup"><span data-stu-id="ac639-107">A DDE *conversation* is the interaction between client and server applications.</span></span> <span data-ttu-id="ac639-108">El DDE de red se utiliza junto con DDE y la biblioteca de administración de DDE (DDEML) en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac639-108">You use network DDE along with DDE and the DDE management library (DDEML) in your application.</span></span>

<span data-ttu-id="ac639-109">DDE es una forma de comunicación entre procesos que usa la memoria compartida para intercambiar datos entre aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ac639-109">DDE is a form of interprocess communication that uses shared memory to exchange data between applications.</span></span> <span data-ttu-id="ac639-110">Las aplicaciones pueden utilizar DDE para transferencias de datos de una vez o para intercambios en curso y actualizar datos.</span><span class="sxs-lookup"><span data-stu-id="ac639-110">Applications can use DDE for one time data transfers or for ongoing exchanges and updating data.</span></span> <span data-ttu-id="ac639-111">Para obtener más información sobre DDE, consulte [intercambio dinámico de datos](../dataxchg/dynamic-data-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="ac639-111">For more information on DDE, see [Dynamic Data Exchange](../dataxchg/dynamic-data-exchange.md).</span></span>

<span data-ttu-id="ac639-112">DDEML simplifica la tarea de agregar funcionalidad DDE a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac639-112">DDEML simplifies the task of adding DDE capability to an application.</span></span> <span data-ttu-id="ac639-113">En lugar de enviar, publicar y procesar directamente los mensajes DDE, una aplicación usa las funciones proporcionadas por DDEML para administrar las conversaciones DDE.</span><span class="sxs-lookup"><span data-stu-id="ac639-113">Instead of sending, posting, and processing DDE messages directly, an application uses the functions provided by the DDEML to manage DDE conversations.</span></span> <span data-ttu-id="ac639-114">Para obtener más información sobre DDEML, vea [biblioteca de administración de intercambio dinámico de datos](../dataxchg/dynamic-data-exchange-management-library.md).</span><span class="sxs-lookup"><span data-stu-id="ac639-114">For more information on DDEML, see [Dynamic Data Exchange Management Library](../dataxchg/dynamic-data-exchange-management-library.md).</span></span>

## <a name="network-dde-files"></a><span data-ttu-id="ac639-115">Archivos DDE de red</span><span class="sxs-lookup"><span data-stu-id="ac639-115">Network DDE Files</span></span>

<span data-ttu-id="ac639-116">Para usar los elementos de la API de DDE de red, debe incluir el archivo de encabezado NDDEApi. h en los archivos de código fuente e incluir el archivo NDDEApi. lib en la línea de vínculo.</span><span class="sxs-lookup"><span data-stu-id="ac639-116">To use the API elements of network DDE, you must include the NDDEApi.h header file in your source files and include NDDEApi.lib file on your link line.</span></span> <span data-ttu-id="ac639-117">También debe asegurarse de que se carga el archivo de NDDEApi.dll.</span><span class="sxs-lookup"><span data-stu-id="ac639-117">You must also make sure that the NDDEApi.dll file is loaded.</span></span>

<span data-ttu-id="ac639-118">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="ac639-118">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="ac639-119">Agente DDE de red</span><span class="sxs-lookup"><span data-stu-id="ac639-119">Network DDE Agent</span></span>](network-dde-agent.md)
-   [<span data-ttu-id="ac639-120">Recursos compartidos DDE</span><span class="sxs-lookup"><span data-stu-id="ac639-120">DDE Shares</span></span>](dde-shares.md)
-   [<span data-ttu-id="ac639-121">Seguridad y recursos compartidos de confianza</span><span class="sxs-lookup"><span data-stu-id="ac639-121">Trusted Shares and Security</span></span>](trusted-shares-and-security.md)
-   [<span data-ttu-id="ac639-122">Administrar recursos compartidos DDE</span><span class="sxs-lookup"><span data-stu-id="ac639-122">Managing DDE Shares</span></span>](managing-dde-shares.md)

 

 
