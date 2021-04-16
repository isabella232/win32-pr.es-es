---
description: Futuras mejoras en el ejemplo de código de aplicación Winsock.
ms.assetid: 317baa53-6bc8-42bd-8f56-480cab29ae6b
title: Mejoras futuras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 938f38334a4bbe392e83efc0be12905fb7ae66a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705617"
---
# <a name="future-improvements"></a><span data-ttu-id="978eb-103">Mejoras futuras</span><span class="sxs-lookup"><span data-stu-id="978eb-103">Future Improvements</span></span>

<span data-ttu-id="978eb-104">Hay varias mejoras que se pueden realizar en esta aplicación, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="978eb-104">There are several improvements that can be made to this application, such as:</span></span>

-   <span data-ttu-id="978eb-105">La aplicación puede crear una única conexión persistente.</span><span class="sxs-lookup"><span data-stu-id="978eb-105">A single, persistent connection could be created by the application.</span></span> <span data-ttu-id="978eb-106">Tendría que agregarse el control de errores adecuado.</span><span class="sxs-lookup"><span data-stu-id="978eb-106">Appropriate error handling would have to be added.</span></span> <span data-ttu-id="978eb-107">Esto reduciría la sobrecarga asociada con el inicio y el desmontaje de la conexión.</span><span class="sxs-lookup"><span data-stu-id="978eb-107">This would reduce the overhead associated with connection startup and teardown.</span></span>
-   <span data-ttu-id="978eb-108">El código de respuesta del servidor se puede optimizar para consolidar las respuestas, lo que reduce el número de paquetes enviados desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="978eb-108">The reply code on the server could be optimized to consolidate replies, reducing the number of packets sent from the server.</span></span>
-   <span data-ttu-id="978eb-109">Se pueden realizar mejoras en el protocolo.</span><span class="sxs-lookup"><span data-stu-id="978eb-109">Improvements in the protocol could be made.</span></span> <span data-ttu-id="978eb-110">Por ejemplo, se puede usar una máscara de máscara de actualización para indicar las celdas que se van a actualizar y solo los datos de las celdas que se envían.</span><span class="sxs-lookup"><span data-stu-id="978eb-110">For example, an update bitmask could be used to signify which cells are to be updated, and only that cell data sent.</span></span>
-   <span data-ttu-id="978eb-111">Las actualizaciones pueden superponerse mediante diferentes subprocesos, de modo que la red no esté inactiva mientras la función **ComputeNext** se esté ejecutando.</span><span class="sxs-lookup"><span data-stu-id="978eb-111">Updates could be overlapped using different threads, so that the network is not idle while the **ComputeNext** function is running.</span></span>

## <a name="related-topics"></a><span data-ttu-id="978eb-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="978eb-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="978eb-113">Mejora de una aplicación lenta</span><span class="sxs-lookup"><span data-stu-id="978eb-113">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="978eb-114">La versión de línea base: una aplicación con un rendimiento muy deficiente</span><span class="sxs-lookup"><span data-stu-id="978eb-114">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="978eb-115">Revisión 1: limpieza del manifiesto</span><span class="sxs-lookup"><span data-stu-id="978eb-115">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="978eb-116">Revisión 2: rediseño para menos conexiones</span><span class="sxs-lookup"><span data-stu-id="978eb-116">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="978eb-117">Revisión 3: envío de bloque comprimido</span><span class="sxs-lookup"><span data-stu-id="978eb-117">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> </dl>

 

 



