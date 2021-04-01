---
description: TAPI 3 implica una serie de objetos que son independientes de los cinco objetos TAPI principales (TAPI, dirección, llamada, CallHub y terminal).
ms.assetid: 090fa8e5-58a5-46ee-89a3-bd97fcfbf0f0
title: Objetos Stand-Alone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e71fdea9c7ed4b66f57c3c0fe35625f35656555e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909621"
---
# <a name="stand-alone-objects"></a><span data-ttu-id="210ad-103">Objetos Stand-Alone</span><span class="sxs-lookup"><span data-stu-id="210ad-103">Stand-Alone Objects</span></span>

<span data-ttu-id="210ad-104">TAPI 3 implica una serie de objetos que son independientes de los cinco objetos TAPI principales (TAPI, dirección, llamada, CallHub y terminal).</span><span class="sxs-lookup"><span data-stu-id="210ad-104">TAPI 3 involves a number of objects that are independent of its five main TAPI objects (TAPI, Address, Call, CallHub, and Terminal).</span></span> <span data-ttu-id="210ad-105">Las interfaces de [eventos](./event-interfaces.md) y los [enumeradores](enumerator-interfaces.md) son objetos independientes y se resumen por separado.</span><span class="sxs-lookup"><span data-stu-id="210ad-105">[Event Interfaces](./event-interfaces.md) and [Enumerator Interfaces](enumerator-interfaces.md) are stand-alone objects, and are summarized separately.</span></span> <span data-ttu-id="210ad-106">A continuación se resumen las interfaces independientes sin eventos y sin enumerador.</span><span class="sxs-lookup"><span data-stu-id="210ad-106">The following summarizes non-event and non-enumerator stand-alone interfaces.</span></span>



| <span data-ttu-id="210ad-107">Interfaz</span><span class="sxs-lookup"><span data-stu-id="210ad-107">Interface</span></span>                                             | <span data-ttu-id="210ad-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="210ad-108">Description</span></span>                                                                                                                                                                                                   |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="210ad-109">**ITCollection**</span><span class="sxs-lookup"><span data-stu-id="210ad-109">**ITCollection**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)                  | <span data-ttu-id="210ad-110">Proporciona métodos para permitir que las aplicaciones cliente de automatización como Visual Basic recuperen información de la colección.</span><span class="sxs-lookup"><span data-stu-id="210ad-110">Provides methods to allow Automation client applications such as Visual Basic to retrieve collection information.</span></span>                                                                                             |
| [<span data-ttu-id="210ad-111">**ITCollection2**</span><span class="sxs-lookup"><span data-stu-id="210ad-111">**ITCollection2**</span></span>](/windows/desktop/api/Tapi3if/nn-tapi3if-itcollection2)                | <span data-ttu-id="210ad-112">Extiende [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) proporcionando métodos adicionales para modificar colecciones.</span><span class="sxs-lookup"><span data-stu-id="210ad-112">Extends [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) by providing additional methods for modifying collections.</span></span>                                                                                                       |
| [<span data-ttu-id="210ad-113">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="210ad-113">**IDispatch**</span></span>](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) | <span data-ttu-id="210ad-114">Interfaz COM estándar para implementar la automatización.</span><span class="sxs-lookup"><span data-stu-id="210ad-114">Standard COM interface for implementing Automation.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="210ad-115">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="210ad-115">**IUnknown**</span></span>](/windows/win32/api/unknwn/nn-unknwn-iunknown)                         | <span data-ttu-id="210ad-116">Interfaz COM estándar para obtener punteros a interfaces de objeto.</span><span class="sxs-lookup"><span data-stu-id="210ad-116">Standard COM interface for getting pointers to object interfaces.</span></span>                                                                                                                                             |
| [<span data-ttu-id="210ad-117">**ITDispatchMapper**</span><span class="sxs-lookup"><span data-stu-id="210ad-117">**ITDispatchMapper**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper)          | <span data-ttu-id="210ad-118">Permite que una aplicación recupere el puntero de envío de otra interfaz en un objeto, dado un puntero [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) actual.</span><span class="sxs-lookup"><span data-stu-id="210ad-118">Allows an application to retrieve the dispatch pointer of another interface on an object, given a current [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) pointer.</span></span> <span data-ttu-id="210ad-119">Útil para algunos lenguajes de scripting.</span><span class="sxs-lookup"><span data-stu-id="210ad-119">Useful for some scripting languages.</span></span> |
| [<span data-ttu-id="210ad-120">**ITRequest**</span><span class="sxs-lookup"><span data-stu-id="210ad-120">**ITRequest**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest)                        | <span data-ttu-id="210ad-121">Proporciona métodos que permiten a una aplicación TAPI 3 usar [telefonía asistida](assisted-telephony-overview.md).</span><span class="sxs-lookup"><span data-stu-id="210ad-121">Provides methods that allow a TAPI 3 application to use [Assisted Telephony](assisted-telephony-overview.md).</span></span>                                                                                                |



 



| <span data-ttu-id="210ad-122">Interfaz</span><span class="sxs-lookup"><span data-stu-id="210ad-122">Interface</span></span>                                  | <span data-ttu-id="210ad-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="210ad-123">Description</span></span>                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="210ad-124">**ITMediaControl**</span><span class="sxs-lookup"><span data-stu-id="210ad-124">**ITMediaControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol)   | <span data-ttu-id="210ad-125">Inicia, detiene y pausa las acciones actuales, como una reproducción.</span><span class="sxs-lookup"><span data-stu-id="210ad-125">Starts, stops, and pauses current actions, such as a playback.</span></span>                                                                                                             |
| [<span data-ttu-id="210ad-126">**ITMediaPlayback**</span><span class="sxs-lookup"><span data-stu-id="210ad-126">**ITMediaPlayback**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) | <span data-ttu-id="210ad-127">Proporciona métodos específicos de reproducción que permiten que una aplicación realice operaciones como establecer la lista de archivos que se van a reproducir y cambiar la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="210ad-127">Provides playback-specific methods that allow an application to perform such operations as setting the list of files to play and changing the playback speed.</span></span>              |
| [<span data-ttu-id="210ad-128">**ITMediaRecord**</span><span class="sxs-lookup"><span data-stu-id="210ad-128">**ITMediaRecord**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord)     | <span data-ttu-id="210ad-129">Proporciona métodos específicos del registro que permiten que una aplicación realice operaciones como establecer los nombres de los archivos que se van a registrar y cambiar la duración de una grabación.</span><span class="sxs-lookup"><span data-stu-id="210ad-129">Provides recording-specific methods that allow an application to perform such operations as setting the names of files to record and changing the duration of a recording.</span></span> |



 



| <span data-ttu-id="210ad-130">Interfaz</span><span class="sxs-lookup"><span data-stu-id="210ad-130">Interface</span></span>                                                  | <span data-ttu-id="210ad-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="210ad-131">Description</span></span>                                                                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="210ad-132">**ITScriptableAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="210ad-132">**ITScriptableAudioFormat**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat) | <span data-ttu-id="210ad-133">Recupera el formato de audio de, o establece el formato de audio de una pista.</span><span class="sxs-lookup"><span data-stu-id="210ad-133">Retrieves the audio format from, or sets the audio format for, a track.</span></span>                                                                                             |
| [<span data-ttu-id="210ad-134">**ITStaticAudioTerminal**</span><span class="sxs-lookup"><span data-stu-id="210ad-134">**ITStaticAudioTerminal**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itstaticaudioterminal)     | <span data-ttu-id="210ad-135">Proporciona métodos de objetos de terminal de audio estáticos que son necesarios para admitir dispositivos telefónicos.</span><span class="sxs-lookup"><span data-stu-id="210ad-135">Provides methods on static audio terminal objects that are needed to support phone devices.</span></span> <span data-ttu-id="210ad-136">TAPI 3,1 MSP debe exponer esta interfaz en todos los terminales de audio estáticos.</span><span class="sxs-lookup"><span data-stu-id="210ad-136">TAPI 3.1 MSPs must expose this interface on all static audio terminals.</span></span> |



 

 

 
