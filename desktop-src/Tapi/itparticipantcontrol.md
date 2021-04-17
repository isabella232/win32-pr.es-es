---
description: IPConf MSP implementa la interfaz ITParticipantControl.
ms.assetid: e617f2a4-6be8-4cb1-9f03-470c5100b834
title: Interfaz ITParticipantControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96075748f0c35cbc5af3c6cd07277d15222e0658
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690491"
---
# <a name="itparticipantcontrol-interface"></a><span data-ttu-id="9e468-103">Interfaz ITParticipantControl</span><span class="sxs-lookup"><span data-stu-id="9e468-103">ITParticipantControl interface</span></span>

<span data-ttu-id="9e468-104">\[**ITParticipantControl** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9e468-104">\[**ITParticipantControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9e468-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="9e468-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9e468-106">IPConf MSP implementa la interfaz **ITParticipantControl** .</span><span class="sxs-lookup"><span data-stu-id="9e468-106">The **ITParticipantControl** interface is implemented by the IPConf MSP.</span></span> <span data-ttu-id="9e468-107">Esta interfaz se expone en el objeto de llamada.</span><span class="sxs-lookup"><span data-stu-id="9e468-107">This interface is exposed on the call object.</span></span> <span data-ttu-id="9e468-108">Esta interfaz permite que una aplicación recupere punteros a los participantes de una conferencia.</span><span class="sxs-lookup"><span data-stu-id="9e468-108">This interface allows an application to retrieve pointers to the participants in a conference.</span></span> <span data-ttu-id="9e468-109">La interfaz **ITParticipantControl** se crea llamando a **QueryInterface** en [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span><span class="sxs-lookup"><span data-stu-id="9e468-109">The **ITParticipantControl** interface is created by calling **QueryInterface** on [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span></span>

## <a name="members"></a><span data-ttu-id="9e468-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="9e468-110">Members</span></span>

<span data-ttu-id="9e468-111">La interfaz **ITParticipantControl** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9e468-111">The **ITParticipantControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9e468-112">**ITParticipantControl** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9e468-112">**ITParticipantControl** also has these types of members:</span></span>

-   [<span data-ttu-id="9e468-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="9e468-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9e468-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="9e468-114">Methods</span></span>

<span data-ttu-id="9e468-115">La interfaz **ITParticipantControl** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9e468-115">The **ITParticipantControl** interface has these methods.</span></span>



| <span data-ttu-id="9e468-116">Método</span><span class="sxs-lookup"><span data-stu-id="9e468-116">Method</span></span>                                                                      | <span data-ttu-id="9e468-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e468-117">Description</span></span>                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e468-118">**EnumerateParticipants**</span><span class="sxs-lookup"><span data-stu-id="9e468-118">**EnumerateParticipants**</span></span>](itparticipantcontrol-enumerateparticipants.md) | <span data-ttu-id="9e468-119">Enumera los participantes actualmente implicados en la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="9e468-119">Enumerates participants currently involved in the conference.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="9e468-120">**obtener \_ participantes**</span><span class="sxs-lookup"><span data-stu-id="9e468-120">**get\_Participants**</span></span>](itparticipantcontrol-get-participants.md)          | <span data-ttu-id="9e468-121">Crea una colección de participantes asociados a la Conferencia actual.</span><span class="sxs-lookup"><span data-stu-id="9e468-121">Creates a collection of participants associated with the current conference.</span></span> <span data-ttu-id="9e468-122">Se proporciona para las aplicaciones cliente de automatización, como las escritas en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9e468-122">Provided for Automation client applications, such as those written in Visual Basic.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9e468-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e468-123">Requirements</span></span>



| <span data-ttu-id="9e468-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e468-124">Requirement</span></span> | <span data-ttu-id="9e468-125">Value</span><span class="sxs-lookup"><span data-stu-id="9e468-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e468-126">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="9e468-126">TAPI version</span></span><br/> | <span data-ttu-id="9e468-127">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="9e468-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9e468-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e468-128">Header</span></span><br/>       | <dl> <span data-ttu-id="9e468-129"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e468-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="9e468-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e468-130">Library</span></span><br/>      | <dl> <span data-ttu-id="9e468-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e468-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9e468-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9e468-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="9e468-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e468-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

