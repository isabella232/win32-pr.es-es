---
description: IPConf MSP implementa la interfaz ITParticipant. Permite que una aplicación recupere información sobre los participantes de la Conferencia y obtenga punteros a las secuencias asociadas a dichos participantes.
ms.assetid: 8c3edfc1-3165-48b7-9d83-8892c192498b
title: Interfaz ITParticipant (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8b7aa9d845d8d2489be0850bcc3fcf3f93ccdac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680783"
---
# <a name="itparticipant-interface"></a><span data-ttu-id="b319c-104">Interfaz ITParticipant</span><span class="sxs-lookup"><span data-stu-id="b319c-104">ITParticipant interface</span></span>

<span data-ttu-id="b319c-105">\[**ITParticipant** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b319c-105">\[**ITParticipant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b319c-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="b319c-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b319c-107">[IPCONF MSP](ipconf-msp.md)implementa la interfaz **ITParticipant** .</span><span class="sxs-lookup"><span data-stu-id="b319c-107">The **ITParticipant** interface is implemented by the [IPConf MSP](ipconf-msp.md).</span></span> <span data-ttu-id="b319c-108">Permite que una aplicación recupere información sobre los participantes de la Conferencia y obtenga punteros a las secuencias asociadas a dichos participantes.</span><span class="sxs-lookup"><span data-stu-id="b319c-108">It allows an application to retrieve information on conference participants, and get pointers to the streams associated with those participants.</span></span>

<span data-ttu-id="b319c-109">Esta interfaz se expone en el objeto de llamada cuando una llamada utiliza la Conferencia de IP.</span><span class="sxs-lookup"><span data-stu-id="b319c-109">This interface is exposed on the call object when a call uses the IP Conferencing.</span></span> <span data-ttu-id="b319c-110">Un puntero se puede obtener llamando a **QueryInterface** mediante un puntero [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .</span><span class="sxs-lookup"><span data-stu-id="b319c-110">A pointer can be obtained by calling **QueryInterface** using an [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) pointer.</span></span>

## <a name="members"></a><span data-ttu-id="b319c-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="b319c-111">Members</span></span>

<span data-ttu-id="b319c-112">La interfaz **ITParticipant** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b319c-112">The **ITParticipant** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b319c-113">**ITParticipant** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b319c-113">**ITParticipant** also has these types of members:</span></span>

-   [<span data-ttu-id="b319c-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="b319c-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b319c-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="b319c-115">Methods</span></span>

<span data-ttu-id="b319c-116">La interfaz **ITParticipant** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b319c-116">The **ITParticipant** interface has these methods.</span></span>



| <span data-ttu-id="b319c-117">Método</span><span class="sxs-lookup"><span data-stu-id="b319c-117">Method</span></span>                                                                      | <span data-ttu-id="b319c-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="b319c-118">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b319c-119">**EnumerateStreams**</span><span class="sxs-lookup"><span data-stu-id="b319c-119">**EnumerateStreams**</span></span>](itparticipant-enumeratestreams.md)                  | <span data-ttu-id="b319c-120">Enumera las secuencias asociadas al participante actual.</span><span class="sxs-lookup"><span data-stu-id="b319c-120">Enumerates streams associated with the current participant.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="b319c-121">**obtener \_ MediaTypes**</span><span class="sxs-lookup"><span data-stu-id="b319c-121">**get\_MediaTypes**</span></span>](itparticipant-get-mediatypes.md)                     | <span data-ttu-id="b319c-122">Obtiene los [**tipos de medios**](tapimediatype--constants.md) asociados a un participante.</span><span class="sxs-lookup"><span data-stu-id="b319c-122">Gets the [**media types**](tapimediatype--constants.md) associated with a participant.</span></span><br/>                                                                      |
| [<span data-ttu-id="b319c-123">**obtener \_ ParticipantTypedInfo**</span><span class="sxs-lookup"><span data-stu-id="b319c-123">**get\_ParticipantTypedInfo**</span></span>](itparticipant-get-participanttypedinfo.md) | <span data-ttu-id="b319c-124">Obtiene una representación BSTR del tipo de información necesaria, como PTI \_ EmailAddress.</span><span class="sxs-lookup"><span data-stu-id="b319c-124">Gets a BSTR representation of the needed type of information, such as PTI\_EMAILADDRESS.</span></span><br/>                                                                     |
| [<span data-ttu-id="b319c-125">**obtener \_ Estado**</span><span class="sxs-lookup"><span data-stu-id="b319c-125">**get\_Status**</span></span>](itparticipant-get-status.md)                             | <span data-ttu-id="b319c-126">Obtiene el estado del participante.</span><span class="sxs-lookup"><span data-stu-id="b319c-126">Gets the status of the participant.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="b319c-127">**obtener \_ secuencias**</span><span class="sxs-lookup"><span data-stu-id="b319c-127">**get\_Streams**</span></span>](itparticipant-get-streams.md)                           | <span data-ttu-id="b319c-128">Crea una colección de secuencias asociadas al participante actual.</span><span class="sxs-lookup"><span data-stu-id="b319c-128">Creates a collection of streams associated with the current participant.</span></span> <span data-ttu-id="b319c-129">Se proporciona para las aplicaciones cliente de automatización, como las escritas en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b319c-129">Provided for Automation client applications, such as those written in Visual Basic.</span></span><br/> |
| [<span data-ttu-id="b319c-130">**Estado de put \_**</span><span class="sxs-lookup"><span data-stu-id="b319c-130">**put\_Status**</span></span>](itparticipant-put-status.md)                             | <span data-ttu-id="b319c-131">Establece si una secuencia asociada al participante está habilitada.</span><span class="sxs-lookup"><span data-stu-id="b319c-131">Sets whether a stream associated with the participant is enabled.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="b319c-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b319c-132">Requirements</span></span>



| <span data-ttu-id="b319c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b319c-133">Requirement</span></span> | <span data-ttu-id="b319c-134">Value</span><span class="sxs-lookup"><span data-stu-id="b319c-134">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b319c-135">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="b319c-135">TAPI version</span></span><br/> | <span data-ttu-id="b319c-136">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="b319c-136">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="b319c-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b319c-137">Header</span></span><br/>       | <dl> <span data-ttu-id="b319c-138"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b319c-138"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b319c-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b319c-139">Library</span></span><br/>      | <dl> <span data-ttu-id="b319c-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b319c-140"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="b319c-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b319c-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="b319c-142"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b319c-142"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b319c-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="b319c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b319c-144">IPConf MSP</span><span class="sxs-lookup"><span data-stu-id="b319c-144">IPConf MSP</span></span>](ipconf-msp.md)
</dt> <dt>

[<span data-ttu-id="b319c-145">Interfaces de IPConf MSP</span><span class="sxs-lookup"><span data-stu-id="b319c-145">IPConf MSP Interfaces</span></span>](ipconf-msp-interfaces.md)
</dt> <dt>

[<span data-ttu-id="b319c-146">**ITCallInfo**</span><span class="sxs-lookup"><span data-stu-id="b319c-146">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> </dl>

 

