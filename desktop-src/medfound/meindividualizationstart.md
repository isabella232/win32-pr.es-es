---
description: Generado por el motor de directivas cuando la individualización está a punto de comenzar. La individualización se realiza mediante la implementación de aplicaciones de la interfaz IMFContentProtectionManager.
ms.assetid: a3ba98ee-4d2e-466d-be9a-c7e3b5f920a7
title: Evento MEIndividualizationStart (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbb8d50bbc2081c4efa41d8b15cc3e41a14ab5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659862"
---
# <a name="meindividualizationstart-event"></a><span data-ttu-id="756c6-104">Evento MEIndividualizationStart</span><span class="sxs-lookup"><span data-stu-id="756c6-104">MEIndividualizationStart event</span></span>

<span data-ttu-id="756c6-105">Generado por el motor de directivas cuando la individualización está a punto de comenzar.</span><span class="sxs-lookup"><span data-stu-id="756c6-105">Raised by the policy engine when individualization is about to begin.</span></span> <span data-ttu-id="756c6-106">La individualización se realiza mediante la implementación de la aplicación de la interfaz [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) .</span><span class="sxs-lookup"><span data-stu-id="756c6-106">Individualization is performed using the application's implementation of the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span>

<span data-ttu-id="756c6-107">Una aplicación individualizada es aquella que ha recibido una actualización a sus componentes de administración de derechos digitales (DRM) que la diferencia de todas las demás copias de la misma aplicación.</span><span class="sxs-lookup"><span data-stu-id="756c6-107">An individualized application is one that has received an upgrade to its digital rights management (DRM) components that differentiates it from all other copies of the same application.</span></span> <span data-ttu-id="756c6-108">Los propietarios de contenido pueden exigir que sus archivos protegidos se reproduzcan solo en una aplicación que se ha individualizado.</span><span class="sxs-lookup"><span data-stu-id="756c6-108">Content owners can require that their protected files be played only on an application that has been individualized.</span></span>

## <a name="event-values"></a><span data-ttu-id="756c6-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="756c6-109">Event values</span></span>

<span data-ttu-id="756c6-110">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="756c6-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="756c6-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="756c6-111">VARTYPE</span></span>              | <span data-ttu-id="756c6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="756c6-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="756c6-113">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="756c6-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="756c6-114">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="756c6-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="756c6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="756c6-115">Remarks</span></span>

<span data-ttu-id="756c6-116">Cuando se completa la adquisición de licencias, el motor de directivas genera el evento [MEIndividualizationCompleted](meindividualizationcompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="756c6-116">When license acquisition is completed, the policy engine raises the [MEIndividualizationCompleted](meindividualizationcompleted.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="756c6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="756c6-117">Requirements</span></span>



| <span data-ttu-id="756c6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="756c6-118">Requirement</span></span> | <span data-ttu-id="756c6-119">Value</span><span class="sxs-lookup"><span data-stu-id="756c6-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="756c6-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="756c6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="756c6-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="756c6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="756c6-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="756c6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="756c6-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="756c6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="756c6-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="756c6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="756c6-125"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="756c6-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="756c6-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="756c6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="756c6-127">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="756c6-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




