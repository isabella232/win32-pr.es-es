---
title: EC_WMT_INDEX_EVENT (Windows Media Format 11 SDK)
description: '\_evento de \_ Índice \_ WMT de EC'
ms.assetid: 46e6a011-7f25-470b-9e10-fa59f0ddbf22
keywords:
- SDK de Windows Media Format, EC_WMT_INDEX_EVENT
- DirectShow, EC_WMT_INDEX_EVENT
- EC_WMT_INDEX_EVENT
- Advanced Systems Format (ASF), EC_WMT_INDEX_EVENT
- ASF (formato de sistemas avanzados), EC_WMT_INDEX_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f34bca14ed02ac78fcfc77d1b9b716f75115a24f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078699"
---
# <a name="ec_wmt_index_event-windows-media-format-11-sdk"></a><span data-ttu-id="1f28d-108">EC_WMT_INDEX_EVENT (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="1f28d-108">EC_WMT_INDEX_EVENT (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="1f28d-109">Lo envía el SDK de Windows Media Format cuando una aplicación utiliza el escritor ASF para indizar Windows Media Video archivos.</span><span class="sxs-lookup"><span data-stu-id="1f28d-109">Sent by the Windows Media Format SDK when an application uses the ASF Writer to index Windows Media Video files.</span></span>

<span data-ttu-id="1f28d-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f28d-110">Parameters</span></span>

<span data-ttu-id="1f28d-111">*lParam1*</span><span class="sxs-lookup"><span data-stu-id="1f28d-111">*lParam1*</span></span>

<span data-ttu-id="1f28d-112">Puede ser cualquiera de los siguientes mensajes **de \_ Estado de WMT** .</span><span class="sxs-lookup"><span data-stu-id="1f28d-112">Can be any one of the following **WMT\_STATUS** messages.</span></span>



| <span data-ttu-id="1f28d-113">Message</span><span class="sxs-lookup"><span data-stu-id="1f28d-113">Message</span></span>              | <span data-ttu-id="1f28d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f28d-114">Description</span></span>                                     |
|----------------------|-------------------------------------------------|
| <span data-ttu-id="1f28d-115">WMT \_ iniciado</span><span class="sxs-lookup"><span data-stu-id="1f28d-115">WMT\_STARTED</span></span>         | <span data-ttu-id="1f28d-116">La indización ha comenzado.</span><span class="sxs-lookup"><span data-stu-id="1f28d-116">Indexing has begun.</span></span> <span data-ttu-id="1f28d-117">*lParam2* es cero.</span><span class="sxs-lookup"><span data-stu-id="1f28d-117">*lParam2* is zero.</span></span>          |
| <span data-ttu-id="1f28d-118">WMT \_ cerrado</span><span class="sxs-lookup"><span data-stu-id="1f28d-118">WMT\_CLOSED</span></span>          | <span data-ttu-id="1f28d-119">Se ha completado la indexación.</span><span class="sxs-lookup"><span data-stu-id="1f28d-119">Indexing has been completed.</span></span> <span data-ttu-id="1f28d-120">*lParam2* es cero.</span><span class="sxs-lookup"><span data-stu-id="1f28d-120">*lParam2* is zero.</span></span> |
| <span data-ttu-id="1f28d-121">\_progreso del índice WMT \_</span><span class="sxs-lookup"><span data-stu-id="1f28d-121">WMT\_INDEX\_PROGRESS</span></span> | <span data-ttu-id="1f28d-122">La indexación está en curso.</span><span class="sxs-lookup"><span data-stu-id="1f28d-122">Indexing is in progress.</span></span>                        |



 

<span data-ttu-id="1f28d-123">*lParam2*</span><span class="sxs-lookup"><span data-stu-id="1f28d-123">*lParam2*</span></span>

<span data-ttu-id="1f28d-124">Si *lParam1* es WMT \_ Closed o WMT \_ iniciado, entonces *lParam2* es cero.</span><span class="sxs-lookup"><span data-stu-id="1f28d-124">If *lParam1* is WMT\_CLOSED or WMT\_STARTED, then *lParam2* is zero.</span></span> <span data-ttu-id="1f28d-125">Si *lParam1* es \_ \_ el progreso del índice WMT, *lParam2* es un **valor DWORD** que expresa la cantidad de progreso como un porcentaje del tamaño total de la descarga.</span><span class="sxs-lookup"><span data-stu-id="1f28d-125">If *lParam1* is WMT\_INDEX\_PROGRESS, then *lParam2* is a **DWORD** that expresses the amount of progress as a percentage of the total download size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f28d-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1f28d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f28d-127">**Referencia de QASF de DirectShow**</span><span class="sxs-lookup"><span data-stu-id="1f28d-127">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> </dl>

 

 




