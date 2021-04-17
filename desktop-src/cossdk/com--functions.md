---
description: A continuación se indican las funciones de COM+.
ms.assetid: fdeb70ff-17ae-4ee4-a8b1-7fffb65ba2b2
title: Funciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f7ce33e729a12c37ff1f2dcef516ab13d9b69a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105717436"
---
# <a name="com-functions"></a><span data-ttu-id="6eb5d-103">Funciones COM+</span><span class="sxs-lookup"><span data-stu-id="6eb5d-103">COM+ Functions</span></span>

<span data-ttu-id="6eb5d-104">A continuación se indican las funciones de COM+.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-104">The following are the COM+ functions.</span></span>



| <span data-ttu-id="6eb5d-105">Función</span><span class="sxs-lookup"><span data-stu-id="6eb5d-105">Function</span></span>                                                                 | <span data-ttu-id="6eb5d-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="6eb5d-106">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6eb5d-107">**CoCreateActivity**</span><span class="sxs-lookup"><span data-stu-id="6eb5d-107">**CoCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)                             | <span data-ttu-id="6eb5d-108">Crea una actividad para realizar trabajo por lotes sincrónico y asincrónico que pueda utilizar los servicios COM+ sin necesidad de crear un componente COM+.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-108">Creates an activity to do synchronous or asynchronous batch work that can use COM+ services without needing to create a COM+ component.</span></span> |
| [<span data-ttu-id="6eb5d-109">**CoEnterServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="6eb5d-109">**CoEnterServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)                     | <span data-ttu-id="6eb5d-110">Se utiliza para escribir código que puede usar los servicios COM+.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-110">Used to enter code that can then use COM+ services.</span></span>                                                                                     |
| [<span data-ttu-id="6eb5d-111">**CoGetDefaultContext**</span><span class="sxs-lookup"><span data-stu-id="6eb5d-111">**CoGetDefaultContext**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogetdefaultcontext)                       | <span data-ttu-id="6eb5d-112">Recupera una referencia al contexto predeterminado del contenedor especificado.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-112">Retrieves a reference to the default context of the specified apartment.</span></span>                                                                |
| [<span data-ttu-id="6eb5d-113">**CoLeaveServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="6eb5d-113">**CoLeaveServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)                     | <span data-ttu-id="6eb5d-114">Se usa para dejar el código que utiliza los servicios COM+.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-114">Used to leave code that uses COM+ services.</span></span>                                                                                             |
| <span data-ttu-id="6eb5d-115">**ComPlusCompleteCbbSetup**</span><span class="sxs-lookup"><span data-stu-id="6eb5d-115">**ComPlusCompleteCbbSetup**</span></span>               | <span data-ttu-id="6eb5d-116">Completa una migración de catálogo en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-116">Completes a catalog migration on the destination computer.</span></span>                                                                              |
| <span data-ttu-id="6eb5d-117">**GetComPlusPackageInstallStatus**</span><span class="sxs-lookup"><span data-stu-id="6eb5d-117">**GetComPlusPackageInstallStatus**</span></span> | <span data-ttu-id="6eb5d-118">Indica si Common Language Runtime (CLR) de 64 bits está instalado.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-118">Indicates whether the 64-bit Common Language Runtime (CLR) is installed.</span></span>                                                                |
| [<span data-ttu-id="6eb5d-119">**GetDispenserManager**</span><span class="sxs-lookup"><span data-stu-id="6eb5d-119">**GetDispenserManager**</span></span>](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager)                       | <span data-ttu-id="6eb5d-120">Recupera la interfaz [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) del administrador del dispensador.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-120">Retrieves the dispenser manager's [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) interface.</span></span>                                             |
| [<span data-ttu-id="6eb5d-121">**GetManagedExtensions**</span><span class="sxs-lookup"><span data-stu-id="6eb5d-121">**GetManagedExtensions**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-getmanagedextensions)                     | <span data-ttu-id="6eb5d-122">Determina si la versión instalada de COM+ admite características especiales que se proporcionan para administrar componentes con servicio (objetos administrados).</span><span class="sxs-lookup"><span data-stu-id="6eb5d-122">Determines whether the installed version of COM+ supports special features provided to manage serviced components (managed objects).</span></span>    |
| [<span data-ttu-id="6eb5d-123">**GetObjectContext**</span><span class="sxs-lookup"><span data-stu-id="6eb5d-123">**GetObjectContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext)                             | <span data-ttu-id="6eb5d-124">Recupera una referencia al contexto asociado al objeto COM+ actual.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-124">Retrieves a reference to the context that is associated with the current COM+ object.</span></span>                                                   |
| [<span data-ttu-id="6eb5d-125">**MTSCreateActivity**</span><span class="sxs-lookup"><span data-stu-id="6eb5d-125">**MTSCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-mtscreateactivity)                           | <span data-ttu-id="6eb5d-126">Crea una actividad en un contenedor uniproceso para realizar trabajos por lotes sincrónicos o asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-126">Creates an activity in a single-threaded apartment to do synchronous or asynchronous batch work.</span></span>                                        |
| [<span data-ttu-id="6eb5d-127">**RecycleSurrogate**</span><span class="sxs-lookup"><span data-stu-id="6eb5d-127">**RecycleSurrogate**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-recyclesurrogate)                             | <span data-ttu-id="6eb5d-128">Recicla el proceso de llamada.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-128">Recycles the calling process.</span></span>                                                                                                           |
| [<span data-ttu-id="6eb5d-129">**SafeRef**</span><span class="sxs-lookup"><span data-stu-id="6eb5d-129">**SafeRef**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef)                                               | <span data-ttu-id="6eb5d-130">Obsoleto No use.</span><span class="sxs-lookup"><span data-stu-id="6eb5d-130">Obsolete; do not use.</span></span>                                                                                                                   |



 

 

 



