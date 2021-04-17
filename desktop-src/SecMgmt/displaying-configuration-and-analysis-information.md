---
description: La extensión del complemento debe mostrar la información de configuración y análisis actual a los usuarios.
ms.assetid: 503bc283-c1cd-4258-a27e-4046553882fa
title: Mostrar información de configuración y análisis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc2f0d598ced5f789d9b417d79df591a71f82ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688027"
---
# <a name="displaying-configuration-and-analysis-information"></a><span data-ttu-id="f9e25-103">Mostrar información de configuración y análisis</span><span class="sxs-lookup"><span data-stu-id="f9e25-103">Displaying Configuration and Analysis Information</span></span>

<span data-ttu-id="f9e25-104">La extensión del complemento debe mostrar la información de configuración y análisis actual a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="f9e25-104">Your snap-in extension must display the current configuration and analysis information to the users.</span></span>

<span data-ttu-id="f9e25-105">Para mostrar información, el nodo de extensión del complemento de datos adjuntos debe extender los complementos de configuración de seguridad mediante el nodo servicios.</span><span class="sxs-lookup"><span data-stu-id="f9e25-105">To display information, the attachment snap-in extension node must extend the Security Configuration snap-ins using the Services node.</span></span> <span data-ttu-id="f9e25-106">El nodo servicios es el complemento MMC que administra los servicios instalados en el sistema.</span><span class="sxs-lookup"><span data-stu-id="f9e25-106">The Services node is the MMC snap-in that administers services installed on the system.</span></span>

<span data-ttu-id="f9e25-107">Los tipos de nodo que se pueden extender son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f9e25-107">The node types that can be extended are as follows:</span></span>

-   <span data-ttu-id="f9e25-108">NodeType de servicios de configuración = {24a7f717-1f0c-11D1-affb-00c04fb984f9}</span><span class="sxs-lookup"><span data-stu-id="f9e25-108">Configuration Services NodeType={24a7f717-1f0c-11d1-affb-00c04fb984f9}</span></span>
-   <span data-ttu-id="f9e25-109">NodeType de servicios de inspección = {678050c7-1ff8-11D1-affb-00c04fb984f9}</span><span class="sxs-lookup"><span data-stu-id="f9e25-109">Inspection Services NodeType={678050c7-1ff8-11d1-affb-00c04fb984f9}</span></span>

<span data-ttu-id="f9e25-110">Cuando se expande el nodo servicios, MMC notifica a todas las extensiones de complemento registradas.</span><span class="sxs-lookup"><span data-stu-id="f9e25-110">When the Services node is expanded, the MMC notifies all registered snap-in extensions.</span></span> <span data-ttu-id="f9e25-111">Cada complemento de datos adjuntos debe insertarse en el nodo servicios y realizar las tareas siguientes:</span><span class="sxs-lookup"><span data-stu-id="f9e25-111">Each attachment snap-in should insert itself under the Services node, and perform the following tasks:</span></span>

-   <span data-ttu-id="f9e25-112">Llame a **QueryInterface** para obtener un puntero a la interfaz [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) expuesta por los complementos de configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f9e25-112">Call **QueryInterface** to get a pointer to the [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) interface exposed by the Security Configuration snap-ins.</span></span>
-   <span data-ttu-id="f9e25-113">Llame a [**ISceSvcAttachmentData:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) para informar a los complementos de configuración de seguridad que la extensión del complemento está cargada y para establecer un contexto para las comunicaciones.</span><span class="sxs-lookup"><span data-stu-id="f9e25-113">Call [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) to inform the Security Configuration snap-ins that the snap-in extension is loaded and to establish a context for communications.</span></span>
-   <span data-ttu-id="f9e25-114">Llame a [**ISceSvcAttachmentData:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata) para recuperar la información de configuración de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f9e25-114">Call [**ISceSvcAttachmentData::GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata) to retrieve configuration information from the database.</span></span> <span data-ttu-id="f9e25-115">Este paso se puede realizar cuando la extensión del complemento se inicializa o cuando el usuario abre su nodo.</span><span class="sxs-lookup"><span data-stu-id="f9e25-115">This step can be performed either when the snap-in extension initializes itself or when the user opens its node.</span></span>

<span data-ttu-id="f9e25-116">Para obtener más información, vea [Agregar un nodo de extensión del complemento de datos adjuntos](adding-an-attachment-snap-in-extension-node.md).</span><span class="sxs-lookup"><span data-stu-id="f9e25-116">For more information, see [Adding an Attachment Snap-in Extension Node](adding-an-attachment-snap-in-extension-node.md).</span></span>

 

 



