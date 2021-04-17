---
description: Un proveedor de hora se implementa como un archivo DLL. Cada archivo DLL puede admitir varios proveedores de hora. Cada proveedor es responsable de su propia configuración y sincronización.
ms.assetid: 04f523d7-7e99-4bf5-941f-ae67f4b9df0a
title: Creación de un proveedor de hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ac5a12e19651d88c3328ac72280c486a54c4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669974"
---
# <a name="creating-a-time-provider"></a><span data-ttu-id="2da1e-105">Creación de un proveedor de hora</span><span class="sxs-lookup"><span data-stu-id="2da1e-105">Creating a Time Provider</span></span>

<span data-ttu-id="2da1e-106">Un proveedor de hora se implementa como un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="2da1e-106">A time provider is implemented as a DLL.</span></span> <span data-ttu-id="2da1e-107">Cada archivo DLL puede admitir varios proveedores de hora.</span><span class="sxs-lookup"><span data-stu-id="2da1e-107">Each DLL can support multiple time providers.</span></span> <span data-ttu-id="2da1e-108">Cada proveedor es responsable de su propia configuración y sincronización.</span><span class="sxs-lookup"><span data-stu-id="2da1e-108">Each provider is responsible for its own configuration and synchronization.</span></span>

<span data-ttu-id="2da1e-109">Los proveedores de tiempo deben implementar las siguientes funciones de devolución de llamada:</span><span class="sxs-lookup"><span data-stu-id="2da1e-109">Time providers must implement the following callback functions:</span></span>

-   [<span data-ttu-id="2da1e-110">**TimeProvClose**</span><span class="sxs-lookup"><span data-stu-id="2da1e-110">**TimeProvClose**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)
-   [<span data-ttu-id="2da1e-111">**TimeProvCommand**</span><span class="sxs-lookup"><span data-stu-id="2da1e-111">**TimeProvCommand**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)
-   [<span data-ttu-id="2da1e-112">**TimeProvOpen**</span><span class="sxs-lookup"><span data-stu-id="2da1e-112">**TimeProvOpen**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)

<span data-ttu-id="2da1e-113">Una vez cargado el archivo DLL del proveedor, el administrador de proveedores de hora llama a [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen), pasando el nombre del proveedor y punteros a las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="2da1e-113">After it has loaded the provider DLL, the time provider manager calls [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen), passing the name of the provider and pointers to the following functions:</span></span>

-   [<span data-ttu-id="2da1e-114">**AlertSamplesAvailFunc**</span><span class="sxs-lookup"><span data-stu-id="2da1e-114">**AlertSamplesAvailFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)
-   [<span data-ttu-id="2da1e-115">**GetTimeSysInfoFunc**</span><span class="sxs-lookup"><span data-stu-id="2da1e-115">**GetTimeSysInfoFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)
-   [<span data-ttu-id="2da1e-116">**LogTimeProvEventFunc**</span><span class="sxs-lookup"><span data-stu-id="2da1e-116">**LogTimeProvEventFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)

<span data-ttu-id="2da1e-117">Estas funciones son para su uso por parte del proveedor de hora.</span><span class="sxs-lookup"><span data-stu-id="2da1e-117">These functions are for use by the time provider.</span></span> <span data-ttu-id="2da1e-118">El proveedor de hora usa [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) para devolver un identificador de proveedor que utiliza el administrador de proveedores de hora al enviar comandos al proveedor de hora.</span><span class="sxs-lookup"><span data-stu-id="2da1e-118">The time provider uses [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) to return a provider handle that the time provider manager uses when sending commands to the time provider.</span></span> <span data-ttu-id="2da1e-119">El proveedor de hora define el valor del identificador y se usa principalmente para distinguir entre los distintos proveedores implementados en el mismo archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="2da1e-119">The handle value is defined by the time provider and is used primarily to distinguish between different providers implemented in the same DLL.</span></span> <span data-ttu-id="2da1e-120">El proveedor de hora puede registrar eventos importantes mediante [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc).</span><span class="sxs-lookup"><span data-stu-id="2da1e-120">The time provider can log significant events using [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc).</span></span>

<span data-ttu-id="2da1e-121">El administrador de proveedores de hora usa [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) para enviar comandos al proveedor de hora.</span><span class="sxs-lookup"><span data-stu-id="2da1e-121">The time provider manager uses [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) to send commands to the time provider.</span></span> <span data-ttu-id="2da1e-122">Cuando el proveedor de hora debe notificar a la hora en que el administrador de proveedores tiene ejemplos de tiempo disponibles, llama a [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc).</span><span class="sxs-lookup"><span data-stu-id="2da1e-122">When the time provider needs to notify the time provider manager that it has time samples available, it calls [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc).</span></span> <span data-ttu-id="2da1e-123">A continuación, el administrador de proveedores de hora llama a **TimeProvCommand** con el \_ comando TPC GetSamples para recuperar los ejemplos de tiempo.</span><span class="sxs-lookup"><span data-stu-id="2da1e-123">The time provider manager then calls **TimeProvCommand** with the TPC\_GetSamples command to retrieve the time samples.</span></span> <span data-ttu-id="2da1e-124">El administrador de proveedores de tiempo puede tardar hasta 16 segundos en solicitar el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2da1e-124">It can take up to 16 seconds for the time provider manager to request the sample.</span></span> <span data-ttu-id="2da1e-125">Por lo tanto, la aplicación no debe esperar a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2da1e-125">Therefore, the application should not wait for the request.</span></span>

<span data-ttu-id="2da1e-126">Para garantizar la precisión, el proveedor de hora debe recuperar toda la información relacionada con el tiempo mediante [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc).</span><span class="sxs-lookup"><span data-stu-id="2da1e-126">To ensure accuracy, the time provider should retrieve all time-related information using [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc).</span></span>

<span data-ttu-id="2da1e-127">Cuando es el momento de apagar el proveedor de hora, el administrador de proveedores de hora llama a [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose).</span><span class="sxs-lookup"><span data-stu-id="2da1e-127">When it is time to shut down the time provider, the time provider manager calls [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose).</span></span>

 

 



