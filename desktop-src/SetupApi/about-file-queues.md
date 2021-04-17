---
description: Una cola de archivos es una lista de operaciones de archivo que se procesan al mismo tiempo. Las operaciones de archivo en la cola pueden ser operaciones de copiar, cambiar nombre o eliminar. La cola de archivos organiza las operaciones de archivo por tipo, creando subcolas de copia, cambio de nombre y eliminación.
ms.assetid: 9ad42c37-1d6b-4f1b-8173-629e2d3678f2
title: Acerca de las colas de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af441a1195bad5116306ca93cfbe658be5b3efc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666434"
---
# <a name="about-file-queues"></a><span data-ttu-id="95cca-105">Acerca de las colas de archivos</span><span class="sxs-lookup"><span data-stu-id="95cca-105">About File Queues</span></span>

<span data-ttu-id="95cca-106">Una cola de archivos es una lista de operaciones de archivo que se procesan al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="95cca-106">A file queue is a list of file operations that are processed at one time.</span></span> <span data-ttu-id="95cca-107">Las operaciones de archivo en la cola pueden ser operaciones de copiar, cambiar nombre o eliminar.</span><span class="sxs-lookup"><span data-stu-id="95cca-107">The file operations in the queue may be copy, rename, or delete operations.</span></span> <span data-ttu-id="95cca-108">La cola de archivos organiza las operaciones de archivo por tipo, creando subcolas de copia, cambio de nombre y eliminación.</span><span class="sxs-lookup"><span data-stu-id="95cca-108">The file queue organizes file operations by type, creating copy, rename, and delete subqueues.</span></span>

<span data-ttu-id="95cca-109">Estas operaciones se pueden enviar a la cola en cualquier orden y el proceso de puesta en cola no debe ser contiguo.</span><span class="sxs-lookup"><span data-stu-id="95cca-109">These operations may be sent to the queue in any order, and the enqueuing process need not be contiguous.</span></span> <span data-ttu-id="95cca-110">Cuando se confirma la cola, la función [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) realiza operaciones de archivo en orden del tipo de operación.</span><span class="sxs-lookup"><span data-stu-id="95cca-110">When the queue is committed, the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function performs file operations in order of the operation type.</span></span>

<span data-ttu-id="95cca-111">Normalmente, todas las operaciones de archivo necesarias para una instalación completa se ponen en cola en la cola de archivos y, a continuación, se procesan en un lote único cuando se confirma la cola.</span><span class="sxs-lookup"><span data-stu-id="95cca-111">Typically, all of the file operations necessary for an entire installation are queued to the file queue, and then processed in a single batch when the queue is committed.</span></span>

<span data-ttu-id="95cca-112">Una ventaja de poner en cola las operaciones de archivo sobre la instalación de archivos sección por sección desde un archivo INF es que puede simplificar el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="95cca-112">One advantage of queuing file operations over installing files section-by-section from an INF file is that you can streamline the installation process.</span></span> <span data-ttu-id="95cca-113">En lugar de tener que obtener información del usuario para que se instale cada sección, puede obtener información de instalación del usuario para todos los archivos que se van a instalar al compilar la cola.</span><span class="sxs-lookup"><span data-stu-id="95cca-113">Instead of having to obtain information from the user for each section to be installed, you can obtain installation information from the user for all the files to be installed while building the queue.</span></span> <span data-ttu-id="95cca-114">Esto permite al usuario realizar otras actividades mientras se procesan las operaciones de copia con un uso intensivo de tiempo mediante la función [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) .</span><span class="sxs-lookup"><span data-stu-id="95cca-114">This frees the user to pursue other activities while the time-intensive copy operations are processed by the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function.</span></span>

<span data-ttu-id="95cca-115">Otra ventaja de las colas de archivos es que puede realizar un seguimiento del progreso de la instalación en su conjunto.</span><span class="sxs-lookup"><span data-stu-id="95cca-115">Another advantage of file queues is that you can track the progress of the installation as a whole.</span></span> <span data-ttu-id="95cca-116">Al instalar la sección por sección desde un archivo INF, los indicadores de progreso, como las barras de progreso, solo pueden realizar el seguimiento de la sección INF actual.</span><span class="sxs-lookup"><span data-stu-id="95cca-116">When installing section-by-section from an INF file, progress indicators such as progress bars can track only the current INF section.</span></span> <span data-ttu-id="95cca-117">Cuando se instala la sección siguiente, la barra de progreso comienza de nuevo.</span><span class="sxs-lookup"><span data-stu-id="95cca-117">When the next section is installed, the progress bar starts over.</span></span> <span data-ttu-id="95cca-118">Con una cola, el número total de archivos que se procesan durante toda la instalación se conoce antes de que se confirme la cola y, por lo tanto, se puede generar una barra de progreso para realizar el seguimiento de toda la instalación.</span><span class="sxs-lookup"><span data-stu-id="95cca-118">With a queue, the total number of files to be processed during the entire installation is known before the queue is committed, and thus, a progress bar can be generated to track the entire installation.</span></span>

<span data-ttu-id="95cca-119">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="95cca-119">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="95cca-120">Orden de compromiso de cola</span><span class="sxs-lookup"><span data-stu-id="95cca-120">Order of Queue Commitment</span></span>](order-of-queue-commitment.md)
-   [<span data-ttu-id="95cca-121">Notificaciones de cola</span><span class="sxs-lookup"><span data-stu-id="95cca-121">Queue Notifications</span></span>](queue-notifications.md)

 

 



