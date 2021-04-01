---
title: Constantes de estado del trabajo de impresión ADSI (Adssts. h)
description: Las constantes siguientes se usan con la propiedad IADsPrintJobOperations. status para indicar el estado de un trabajo de impresión.
ms.assetid: 44a981cc-1098-4b6d-8332-e678953c9112
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- ADS_JOB_PAUSED
- ADS_JOB_ERROR
- ADS_JOB_DELETING
- ADS_JOB_SPOOLING
- ADS_JOB_PRINTING
- ADS_JOB_OFFLINE
- ADS_JOB_PAPEROUT
- ADS_JOB_PRINTED
- ADS_JOB_DELETED
api_location:
- Adssts.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51e83393aa0322ef142ee45b4a893f980293ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996838"
---
# <a name="adsi-print-job-status-constants"></a><span data-ttu-id="fbbcf-103">Constantes de estado del trabajo de impresión ADSI</span><span class="sxs-lookup"><span data-stu-id="fbbcf-103">ADSI Print Job Status Constants</span></span>

<span data-ttu-id="fbbcf-104">Las constantes siguientes se usan con la propiedad [**IADsPrintJobOperations. status**](iadsprintjoboperations-property-methods.md) para indicar el estado de un trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="fbbcf-104">The following constants are used with the [**IADsPrintJobOperations.Status**](iadsprintjoboperations-property-methods.md) property to indicate the status of a print job.</span></span>

<dl> <dt>

<span data-ttu-id="fbbcf-105"><span id="ADS_JOB_PAUSED"></span><span id="ads_job_paused"></span>**trabajo de ADS en \_ \_ pausa**</span><span class="sxs-lookup"><span data-stu-id="fbbcf-105"><span id="ADS_JOB_PAUSED"></span><span id="ads_job_paused"></span>**ADS\_JOB\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbcf-106">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="fbbcf-106">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="fbbcf-107">El trabajo de impresión está en pausa.</span><span class="sxs-lookup"><span data-stu-id="fbbcf-107">The print job is paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbcf-108"><span id="ADS_JOB_ERROR"></span><span id="ads_job_error"></span>**\_error de trabajo de ADS \_**</span><span class="sxs-lookup"><span data-stu-id="fbbcf-108"><span id="ADS_JOB_ERROR"></span><span id="ads_job_error"></span>**ADS\_JOB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbcf-109">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="fbbcf-109">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="fbbcf-110">Se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="fbbcf-110">An error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbcf-111"><span id="ADS_JOB_DELETING"></span><span id="ads_job_deleting"></span>**\_eliminación de trabajos de ADS \_**</span><span class="sxs-lookup"><span data-stu-id="fbbcf-111"><span id="ADS_JOB_DELETING"></span><span id="ads_job_deleting"></span>**ADS\_JOB\_DELETING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbcf-112">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="fbbcf-112">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="fbbcf-113">Se está eliminando el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="fbbcf-113">The print job is being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbcf-114"><span id="ADS_JOB_SPOOLING"></span><span id="ads_job_spooling"></span>**\_cola de trabajos de ADS \_**</span><span class="sxs-lookup"><span data-stu-id="fbbcf-114"><span id="ADS_JOB_SPOOLING"></span><span id="ads_job_spooling"></span>**ADS\_JOB\_SPOOLING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbcf-115">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="fbbcf-115">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="fbbcf-116">El trabajo de impresión se está poniendo en cola.</span><span class="sxs-lookup"><span data-stu-id="fbbcf-116">The print job is being spooled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbcf-117"><span id="ADS_JOB_PRINTING"></span><span id="ads_job_printing"></span>**\_impresión de trabajos de ADS \_**</span><span class="sxs-lookup"><span data-stu-id="fbbcf-117"><span id="ADS_JOB_PRINTING"></span><span id="ads_job_printing"></span>**ADS\_JOB\_PRINTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbcf-118">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="fbbcf-118">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="fbbcf-119">Se está imprimiendo el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="fbbcf-119">The print job is being printed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbcf-120"><span id="ADS_JOB_OFFLINE"></span><span id="ads_job_offline"></span>**trabajo de ADS \_ \_ sin conexión**</span><span class="sxs-lookup"><span data-stu-id="fbbcf-120"><span id="ADS_JOB_OFFLINE"></span><span id="ads_job_offline"></span>**ADS\_JOB\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbcf-121">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="fbbcf-121">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="fbbcf-122">La impresora no está conectada.</span><span class="sxs-lookup"><span data-stu-id="fbbcf-122">The printer is offline.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbcf-123"><span id="ADS_JOB_PAPEROUT"></span><span id="ads_job_paperout"></span>**trabajo de ADS \_ \_ PAPEROUT**</span><span class="sxs-lookup"><span data-stu-id="fbbcf-123"><span id="ADS_JOB_PAPEROUT"></span><span id="ads_job_paperout"></span>**ADS\_JOB\_PAPEROUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbcf-124">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="fbbcf-124">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="fbbcf-125">La impresora se ha quedado sin papel.</span><span class="sxs-lookup"><span data-stu-id="fbbcf-125">The printer is out of paper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbcf-126"><span id="ADS_JOB_PRINTED"></span><span id="ads_job_printed"></span>**trabajo de ADS \_ \_ impreso**</span><span class="sxs-lookup"><span data-stu-id="fbbcf-126"><span id="ADS_JOB_PRINTED"></span><span id="ads_job_printed"></span>**ADS\_JOB\_PRINTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbcf-127">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="fbbcf-127">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="fbbcf-128">Se ha impreso el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="fbbcf-128">The print job has been printed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbcf-129"><span id="ADS_JOB_DELETED"></span><span id="ads_job_deleted"></span>**trabajo de ADS \_ \_ eliminado**</span><span class="sxs-lookup"><span data-stu-id="fbbcf-129"><span id="ADS_JOB_DELETED"></span><span id="ads_job_deleted"></span>**ADS\_JOB\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbcf-130">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="fbbcf-130">256 (0x100)</span></span>
</dt> <dt>



<span data-ttu-id="fbbcf-131">Se ha eliminado el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="fbbcf-131">The print job has been deleted.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fbbcf-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbbcf-132">Requirements</span></span>



| <span data-ttu-id="fbbcf-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbbcf-133">Requirement</span></span> | <span data-ttu-id="fbbcf-134">Value</span><span class="sxs-lookup"><span data-stu-id="fbbcf-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fbbcf-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbbcf-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fbbcf-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fbbcf-136">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="fbbcf-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbbcf-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fbbcf-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fbbcf-138">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="fbbcf-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fbbcf-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbbcf-140"><dt>Adssts. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbbcf-140"><dt>Adssts.h</dt></span></span> </dl> |



 

 





