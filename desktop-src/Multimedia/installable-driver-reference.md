---
title: Referencia del controlador instalable
description: Referencia del controlador instalable
ms.assetid: 869b92f1-2711-4198-9911-3df1ebc58d5f
keywords:
- Windows multimedia, referencia del controlador instalable
- multimedia, referencia del controlador instalable
- Controladores instalables, referencia
- Referencia del controlador instalable, acerca de
- referencia de controladores instalables, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90475063f9d9211e841902fe73d2f09dc6130d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904530"
---
# <a name="installable-driver-reference"></a><span data-ttu-id="c63d3-108">Referencia del controlador instalable</span><span class="sxs-lookup"><span data-stu-id="c63d3-108">Installable Driver Reference</span></span>

<span data-ttu-id="c63d3-109">Las funciones y los mensajes asociados a los controladores instalables se agrupan de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="c63d3-109">The functions and messages associated with installable drivers are grouped as follows.</span></span>

## <a name="loading-and-unloading-drivers"></a><span data-ttu-id="c63d3-110">Cargar y descargar controladores</span><span class="sxs-lookup"><span data-stu-id="c63d3-110">Loading and Unloading Drivers</span></span>

-   [<span data-ttu-id="c63d3-111">GetDriverModuleHandle</span><span class="sxs-lookup"><span data-stu-id="c63d3-111">GetDriverModuleHandle</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle)
-   [<span data-ttu-id="c63d3-112">OpenDriver</span><span class="sxs-lookup"><span data-stu-id="c63d3-112">OpenDriver</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver)
-   [<span data-ttu-id="c63d3-113">SendDriverMessage</span><span class="sxs-lookup"><span data-stu-id="c63d3-113">SendDriverMessage</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage)

## <a name="closedriver"></a><span data-ttu-id="c63d3-114">CloseDriver</span><span class="sxs-lookup"><span data-stu-id="c63d3-114">CloseDriver</span></span>

-   [<span data-ttu-id="c63d3-115">**DRV \_ cerrar**</span><span class="sxs-lookup"><span data-stu-id="c63d3-115">**DRV\_CLOSE**</span></span>](drv-close.md)
-   [<span data-ttu-id="c63d3-116">**DRV \_ Disable**</span><span class="sxs-lookup"><span data-stu-id="c63d3-116">**DRV\_DISABLE**</span></span>](drv-disable.md)
-   [<span data-ttu-id="c63d3-117">**DRV ( \_ Habilitar)**</span><span class="sxs-lookup"><span data-stu-id="c63d3-117">**DRV\_ENABLE**</span></span>](drv-enable.md)
-   [<span data-ttu-id="c63d3-118">**DRV \_ gratis**</span><span class="sxs-lookup"><span data-stu-id="c63d3-118">**DRV\_FREE**</span></span>](drv-free.md)
-   [<span data-ttu-id="c63d3-119">**carga de DRV \_**</span><span class="sxs-lookup"><span data-stu-id="c63d3-119">**DRV\_LOAD**</span></span>](drv-load.md)
-   [<span data-ttu-id="c63d3-120">**DRV \_ Open**</span><span class="sxs-lookup"><span data-stu-id="c63d3-120">**DRV\_OPEN**</span></span>](drv-open.md)

## <a name="configuring-a-driver"></a><span data-ttu-id="c63d3-121">Configuración de un controlador</span><span class="sxs-lookup"><span data-stu-id="c63d3-121">Configuring a Driver</span></span>

-   [<span data-ttu-id="c63d3-122">**configuración de DRV \_**</span><span class="sxs-lookup"><span data-stu-id="c63d3-122">**DRV\_CONFIGURE**</span></span>](drv-configure.md)
-   [<span data-ttu-id="c63d3-123">**DRV \_ QUERYCONFIGURE**</span><span class="sxs-lookup"><span data-stu-id="c63d3-123">**DRV\_QUERYCONFIGURE**</span></span>](drv-queryconfigure.md)
-   [<span data-ttu-id="c63d3-124">**DRVCONFIGINFO**</span><span class="sxs-lookup"><span data-stu-id="c63d3-124">**DRVCONFIGINFO**</span></span>](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo)

## <a name="installing-a-driver"></a><span data-ttu-id="c63d3-125">Instalación de un controlador</span><span class="sxs-lookup"><span data-stu-id="c63d3-125">Installing a Driver</span></span>

-   [<span data-ttu-id="c63d3-126">**instalación de DRV \_**</span><span class="sxs-lookup"><span data-stu-id="c63d3-126">**DRV\_INSTALL**</span></span>](drv-install.md)
-   [<span data-ttu-id="c63d3-127">**DRV \_ Remove**</span><span class="sxs-lookup"><span data-stu-id="c63d3-127">**DRV\_REMOVE**</span></span>](drv-remove.md)

## <a name="driver-functions"></a><span data-ttu-id="c63d3-128">Funciones de controlador</span><span class="sxs-lookup"><span data-stu-id="c63d3-128">Driver Functions</span></span>

-   [<span data-ttu-id="c63d3-129">DefDriverProc</span><span class="sxs-lookup"><span data-stu-id="c63d3-129">DefDriverProc</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc)
-   [<span data-ttu-id="c63d3-130">DriverCallback</span><span class="sxs-lookup"><span data-stu-id="c63d3-130">DriverCallback</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback)
-   [<span data-ttu-id="c63d3-131">DriverProc</span><span class="sxs-lookup"><span data-stu-id="c63d3-131">DriverProc</span></span>](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc)

## <a name="related-topics"></a><span data-ttu-id="c63d3-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c63d3-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c63d3-133">Controladores instalables</span><span class="sxs-lookup"><span data-stu-id="c63d3-133">Installable Drivers</span></span>](installable-drivers.md)
</dt> </dl>

 

 