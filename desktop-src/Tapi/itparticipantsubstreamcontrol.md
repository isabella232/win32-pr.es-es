---
description: IPConf MSP implementa la interfaz ITParticipantSubStreamControl.
ms.assetid: d5af0fb1-af18-4efb-9b68-1fa60c1272f6
title: Interfaz ITParticipantSubStreamControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 799b1a85c6619e1175e620f2c5c5ef851005ba50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691072"
---
# <a name="itparticipantsubstreamcontrol-interface"></a><span data-ttu-id="808f2-103">Interfaz ITParticipantSubStreamControl</span><span class="sxs-lookup"><span data-stu-id="808f2-103">ITParticipantSubStreamControl interface</span></span>

<span data-ttu-id="808f2-104">\[**ITParticipantSubStreamControl** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="808f2-104">\[**ITParticipantSubStreamControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="808f2-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="808f2-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="808f2-106">IPConf MSP implementa la interfaz **ITParticipantSubStreamControl** .</span><span class="sxs-lookup"><span data-stu-id="808f2-106">The **ITParticipantSubStreamControl** interface is implemented by the IPConf MSP.</span></span> <span data-ttu-id="808f2-107">Esta interfaz se expone en el objeto de llamada.</span><span class="sxs-lookup"><span data-stu-id="808f2-107">This interface is exposed on the call object.</span></span> <span data-ttu-id="808f2-108">Esta interfaz proporciona métodos que permiten a una aplicación detectar o controlar la coincidencia del subflujo con el participante.</span><span class="sxs-lookup"><span data-stu-id="808f2-108">This interface provides methods that allow an application to either discover or control the matching of substream to participant.</span></span> <span data-ttu-id="808f2-109">La interfaz **ITParticipantSubStreamControl** se crea llamando a **QueryInterface** en [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span><span class="sxs-lookup"><span data-stu-id="808f2-109">The **ITParticipantSubStreamControl** interface is created by calling **QueryInterface** on [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span></span>

## <a name="members"></a><span data-ttu-id="808f2-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="808f2-110">Members</span></span>

<span data-ttu-id="808f2-111">La interfaz **ITParticipantSubStreamControl** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="808f2-111">The **ITParticipantSubStreamControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="808f2-112">**ITParticipantSubStreamControl** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="808f2-112">**ITParticipantSubStreamControl** also has these types of members:</span></span>

-   [<span data-ttu-id="808f2-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="808f2-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="808f2-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="808f2-114">Methods</span></span>

<span data-ttu-id="808f2-115">La interfaz **ITParticipantSubStreamControl** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="808f2-115">The **ITParticipantSubStreamControl** interface has these methods.</span></span>



| <span data-ttu-id="808f2-116">Método</span><span class="sxs-lookup"><span data-stu-id="808f2-116">Method</span></span>                                                                                              | <span data-ttu-id="808f2-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="808f2-117">Description</span></span>                                                     |
|:----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [<span data-ttu-id="808f2-118">**obtener \_ ParticipantFromSubStream**</span><span class="sxs-lookup"><span data-stu-id="808f2-118">**get\_ParticipantFromSubStream**</span></span>](itparticipantsubstreamcontrol-get-participantfromsubstream.md) | <span data-ttu-id="808f2-119">Obtiene los participantes asociados a un subflujo determinado.</span><span class="sxs-lookup"><span data-stu-id="808f2-119">Gets participants associated with a given substream.</span></span><br/> |
| [<span data-ttu-id="808f2-120">**obtener \_ SubStreamFromParticipant**</span><span class="sxs-lookup"><span data-stu-id="808f2-120">**get\_SubStreamFromParticipant**</span></span>](itparticipantsubstreamcontrol-get-substreamfromparticipant.md) | <span data-ttu-id="808f2-121">Obtiene subsecuencias asociadas a un participante determinado.</span><span class="sxs-lookup"><span data-stu-id="808f2-121">Gets substreams associated with a given participant.</span></span><br/> |
| [<span data-ttu-id="808f2-122">**SwitchTerminalToSubStream**</span><span class="sxs-lookup"><span data-stu-id="808f2-122">**SwitchTerminalToSubStream**</span></span>](itparticipantsubstreamcontrol-switchterminaltosubstream.md)        | <span data-ttu-id="808f2-123">Establece un participante en una subsecuencia.</span><span class="sxs-lookup"><span data-stu-id="808f2-123">Sets a participant on a substream.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="808f2-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="808f2-124">Requirements</span></span>



| <span data-ttu-id="808f2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="808f2-125">Requirement</span></span> | <span data-ttu-id="808f2-126">Value</span><span class="sxs-lookup"><span data-stu-id="808f2-126">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="808f2-127">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="808f2-127">TAPI version</span></span><br/> | <span data-ttu-id="808f2-128">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="808f2-128">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="808f2-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="808f2-129">Header</span></span><br/>       | <dl> <span data-ttu-id="808f2-130"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="808f2-130"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="808f2-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="808f2-131">Library</span></span><br/>      | <dl> <span data-ttu-id="808f2-132"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="808f2-132"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="808f2-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="808f2-133">DLL</span></span><br/>          | <dl> <span data-ttu-id="808f2-134"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="808f2-134"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="808f2-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="808f2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="808f2-136">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="808f2-136">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="808f2-137">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="808f2-137">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

