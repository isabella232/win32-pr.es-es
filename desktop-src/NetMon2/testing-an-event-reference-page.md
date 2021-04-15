---
description: El paso final de la creación de una página de referencia de eventos (ERP) es probarlo.
ms.assetid: 12690317-1cd2-496c-8a0d-ba6caca58b86
title: Probar una página de referencia de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6afaaec279403922abde578b9e73931e607680f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677421"
---
# <a name="testing-an-event-reference-page"></a><span data-ttu-id="4e010-103">Probar una página de referencia de eventos</span><span class="sxs-lookup"><span data-stu-id="4e010-103">Testing an Event Reference Page</span></span>

<span data-ttu-id="4e010-104">El paso final de la creación de una página de referencia de eventos (ERP) es probarlo.</span><span class="sxs-lookup"><span data-stu-id="4e010-104">The final step of creating an event reference page (ERP) is to test it.</span></span> <span data-ttu-id="4e010-105">Puede probar un ERP viendo el archivo en un explorador HTML, como Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="4e010-105">You can test an ERP by viewing the file in an HTML browser such as Microsoft Internet Explorer.</span></span> <span data-ttu-id="4e010-106">O bien, puede instalar el ERP y su archivo DLL de expertos para probarlo para la invocación de eventos y mostrarlo en el Visor de eventos de Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="4e010-106">Or, you can install the ERP and its expert DLL to test it for event invocation and display it in the Network Monitor Event Viewer.</span></span>

## <a name="viewing-erps-that-have-no-dll"></a><span data-ttu-id="4e010-107">Ver O ERP e que no tienen DLL</span><span class="sxs-lookup"><span data-stu-id="4e010-107">Viewing ERPs that Have No DLL</span></span>

<span data-ttu-id="4e010-108">Para ver el ERP completado sin un archivo DLL de experto instalado, abra el archivo con un visor HTML que admita los orígenes incrustados.</span><span class="sxs-lookup"><span data-stu-id="4e010-108">To view the completed ERP without an installed expert DLL, open the file with an HTML viewer that supports your embedded sources.</span></span> <span data-ttu-id="4e010-109">En la ilustración siguiente se muestra el archivo ERP de ejemplo que se describe en [Writing a ERP](writing-an-event-reference-page.md) , tal como se muestra con la versión 4,01 de Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="4e010-109">The following illustration shows the sample ERP file described in [Writing an ERP](writing-an-event-reference-page.md) as it is displayed using Microsoft Internet Explorer Version 4.01.</span></span>

![archivo ERP de ejemplo](images/ie-erp.png)

<span data-ttu-id="4e010-111">Prueba de O ERP e que tienen un archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4e010-111">Testing ERPs that Have a DLL</span></span>

<span data-ttu-id="4e010-112">Después de crear los archivos ERP y el archivo dll de [**expertos**](experts.md) , puede probar la funcionalidad completa de su o erp e con monitor de red.</span><span class="sxs-lookup"><span data-stu-id="4e010-112">After the ERP files and the [**expert**](experts.md) DLL is created, you can test the complete functionality of your ERPs with Network Monitor.</span></span> <span data-ttu-id="4e010-113">Se supone que el archivo DLL está depurado y puede generar eventos válidos.</span><span class="sxs-lookup"><span data-stu-id="4e010-113">It is assumed that the DLL is debugged and can generate valid events.</span></span>

<span data-ttu-id="4e010-114">**Para probar O ERP e que tienen un archivo DLL**</span><span class="sxs-lookup"><span data-stu-id="4e010-114">**To test ERPs that have a DLL**</span></span>

1.  <span data-ttu-id="4e010-115">Compruebe que el archivo DLL de experto correcto está instalado en el directorio adecuado.</span><span class="sxs-lookup"><span data-stu-id="4e010-115">Verify that the correct expert DLL is installed in the appropriate directory.</span></span> <span data-ttu-id="4e010-116">Para obtener más información, consulte [instalación de un experto en Monitor de red 2,1](installing-an-expert-to-network-monitor-2-1.md).</span><span class="sxs-lookup"><span data-stu-id="4e010-116">For more information, see [Installing an Expert to Network Monitor 2.1](installing-an-expert-to-network-monitor-2-1.md).</span></span>
2.  <span data-ttu-id="4e010-117">Compruebe el [nombre correcto](naming-an-event-reference-page.md) del archivo ERP.</span><span class="sxs-lookup"><span data-stu-id="4e010-117">Verify the [correct name](naming-an-event-reference-page.md) of the ERP file.</span></span>
3.  <span data-ttu-id="4e010-118">Compruebe la [ubicación correcta](installing-existing-erps-to-network-monitor-2-1.md) de o ERP e en el directorio de monitor de red.</span><span class="sxs-lookup"><span data-stu-id="4e010-118">Verify the [correct location](installing-existing-erps-to-network-monitor-2-1.md) of the ERPs in the Network Monitor directory.</span></span>
4.  <span data-ttu-id="4e010-119">Pruebe Expert O ERP e en la interfaz de usuario de Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="4e010-119">Test expert ERPs in the Network Monitor UI.</span></span>
5.  <span data-ttu-id="4e010-120">Genere un evento de prueba.</span><span class="sxs-lookup"><span data-stu-id="4e010-120">Generate a test event.</span></span>
6.  <span data-ttu-id="4e010-121">Compruebe que el ERP aparece en el Visor de eventos de Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="4e010-121">Verify that the ERP appears in the Network Monitor Event Viewer.</span></span>

<span data-ttu-id="4e010-122">Para obtener más información acerca de la creación de un ERP, consulte:</span><span class="sxs-lookup"><span data-stu-id="4e010-122">For more information about creating an ERP, see:</span></span>

-   [<span data-ttu-id="4e010-123">Creación de páginas de referencia de eventos Expert y monitor</span><span class="sxs-lookup"><span data-stu-id="4e010-123">Creating Expert and Monitor Event Reference Pages</span></span>](creating-expert-and-monitor-event-reference-pages.md)
-   [<span data-ttu-id="4e010-124">Escribir una página de referencia de eventos</span><span class="sxs-lookup"><span data-stu-id="4e010-124">Writing an Event Reference Page</span></span>](writing-an-event-reference-page.md)
-   [<span data-ttu-id="4e010-125">Asignar un nombre a una página de referencia de eventos</span><span class="sxs-lookup"><span data-stu-id="4e010-125">Naming an Event Reference Page</span></span>](naming-an-event-reference-page.md)

 

 



