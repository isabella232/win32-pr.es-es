---
description: Generado por el motor de directivas cuando la adquisición de licencias está a punto de comenzar. La adquisición de licencias se realiza mediante la implementación de aplicaciones de la interfaz IMFContentProtectionManager.
ms.assetid: c328743c-a69b-431e-8a05-0e140aad9b4d
title: Evento MELicenseAcquisitionStart (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914d2580c95cf40986a844a994c1e284c5ad9e22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687226"
---
# <a name="melicenseacquisitionstart-event"></a><span data-ttu-id="cf648-104">Evento MELicenseAcquisitionStart</span><span class="sxs-lookup"><span data-stu-id="cf648-104">MELicenseAcquisitionStart event</span></span>

<span data-ttu-id="cf648-105">Generado por el motor de directivas cuando la adquisición de licencias está a punto de comenzar.</span><span class="sxs-lookup"><span data-stu-id="cf648-105">Raised by the policy engine when license acquisition is about to begin.</span></span> <span data-ttu-id="cf648-106">La adquisición de licencias se realiza mediante la implementación de la aplicación de la interfaz [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) .</span><span class="sxs-lookup"><span data-stu-id="cf648-106">License acquisition is performed using the application's implementation of the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span>

## <a name="event-values"></a><span data-ttu-id="cf648-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="cf648-107">Event values</span></span>

<span data-ttu-id="cf648-108">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="cf648-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="cf648-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cf648-109">VARTYPE</span></span>              | <span data-ttu-id="cf648-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf648-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="cf648-111">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="cf648-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="cf648-112">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="cf648-112">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="cf648-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf648-113">Remarks</span></span>

<span data-ttu-id="cf648-114">Cuando se completa la adquisición de licencias, el motor de directivas genera el evento [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="cf648-114">When license acquisition is completed, the policy engine raises the [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf648-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf648-115">Requirements</span></span>



| <span data-ttu-id="cf648-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf648-116">Requirement</span></span> | <span data-ttu-id="cf648-117">Value</span><span class="sxs-lookup"><span data-stu-id="cf648-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf648-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf648-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cf648-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cf648-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cf648-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf648-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cf648-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cf648-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cf648-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf648-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf648-123"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf648-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf648-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf648-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf648-125">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cf648-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




