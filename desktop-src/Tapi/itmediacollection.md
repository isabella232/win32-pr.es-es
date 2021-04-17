---
description: La interfaz ITMediaCollection proporciona acceso al conjunto de información multimedia en una descripción de la Conferencia SDP (RFC 2327).
ms.assetid: a7e7a07d-239e-432e-9984-7763f11c59ce
title: Interfaz ITMediaCollection (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21305e1d1729437b53c380b7712feee3827b3ba8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689962"
---
# <a name="itmediacollection-interface"></a><span data-ttu-id="464be-103">Interfaz ITMediaCollection</span><span class="sxs-lookup"><span data-stu-id="464be-103">ITMediaCollection interface</span></span>

<span data-ttu-id="464be-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="464be-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="464be-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="464be-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="464be-106">La interfaz **ITMediaCollection** proporciona acceso al conjunto de información multimedia en una descripción de la Conferencia SDP (RFC 2327).</span><span class="sxs-lookup"><span data-stu-id="464be-106">The **ITMediaCollection** interface provides access to the set of media information in an SDP (RFC 2327) conference description.</span></span> <span data-ttu-id="464be-107">Cada descripción de medios en SDP se describe mediante una interfaz [**ITMedia**](itmedia.md) .</span><span class="sxs-lookup"><span data-stu-id="464be-107">Each Media description in the SDP is described by an [**ITMedia**](itmedia.md) interface.</span></span> <span data-ttu-id="464be-108">**ITMediaCollection** permite la manipulación del conjunto de información de **ITMedia** para SDP, incluido:</span><span class="sxs-lookup"><span data-stu-id="464be-108">**ITMediaCollection** allows manipulation of the set of **ITMedia** information for the SDP, including:</span></span>

-   <span data-ttu-id="464be-109">Permite el acceso a los medios por índice.</span><span class="sxs-lookup"><span data-stu-id="464be-109">Allows media access by index.</span></span>
-   <span data-ttu-id="464be-110">Habilita la creación y eliminación de elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="464be-110">Enables creation and deletion of media.</span></span>

<span data-ttu-id="464be-111">El método [**ITSdp:: get \_ MediaCollection**](itsdp-get-mediacollection.md) crea la interfaz **ITMediaCollection** .</span><span class="sxs-lookup"><span data-stu-id="464be-111">The [**ITSdp::get\_MediaCollection**](itsdp-get-mediacollection.md) method creates the **ITMediaCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="464be-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="464be-112">Members</span></span>

<span data-ttu-id="464be-113">La interfaz **ITMediaCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="464be-113">The **ITMediaCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="464be-114">**ITMediaCollection** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="464be-114">**ITMediaCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="464be-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="464be-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="464be-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="464be-116">Methods</span></span>

<span data-ttu-id="464be-117">La interfaz **ITMediaCollection** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="464be-117">The **ITMediaCollection** interface has these methods.</span></span>



| <span data-ttu-id="464be-118">Método</span><span class="sxs-lookup"><span data-stu-id="464be-118">Method</span></span>                                                            | <span data-ttu-id="464be-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="464be-119">Description</span></span>                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="464be-120">**A**</span><span class="sxs-lookup"><span data-stu-id="464be-120">**Create**</span></span>](itmediacollection-create.md)                        | <span data-ttu-id="464be-121">Crea un nuevo medio con propiedades predeterminadas y lo devuelve.</span><span class="sxs-lookup"><span data-stu-id="464be-121">Creates a new media with default properties and returns it.</span></span><br/> |
| [<span data-ttu-id="464be-122">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="464be-122">**Delete**</span></span>](itmediacollection-delete.md)                        | <span data-ttu-id="464be-123">Elimina el medio correspondiente al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="464be-123">Deletes the media corresponding to the specified index.</span></span><br/>     |
| [<span data-ttu-id="464be-124">**obtener \_ \_ NewEnum**</span><span class="sxs-lookup"><span data-stu-id="464be-124">**get\_\_NewEnum**</span></span>](itmediacollection-get--newenum.md)          | <span data-ttu-id="464be-125">Devuelve un enumerador para la colección.</span><span class="sxs-lookup"><span data-stu-id="464be-125">Returns an enumerator for the collection.</span></span><br/>                   |
| [<span data-ttu-id="464be-126">**obtener \_ recuento**</span><span class="sxs-lookup"><span data-stu-id="464be-126">**get\_Count**</span></span>](itmediacollection-get-count.md)                 | <span data-ttu-id="464be-127">Obtiene el número de medios de la sesión.</span><span class="sxs-lookup"><span data-stu-id="464be-127">Gets the number of media in the session.</span></span><br/>                    |
| [<span data-ttu-id="464be-128">**obtener \_ EnumerationIf**</span><span class="sxs-lookup"><span data-stu-id="464be-128">**get\_EnumerationIf**</span></span>](itmediacollection-get-enumerationif.md) | <span data-ttu-id="464be-129">Obtiene el puntero a la interfaz de enumeración.</span><span class="sxs-lookup"><span data-stu-id="464be-129">Gets pointer to enumeration interface.</span></span><br/>                      |
| [<span data-ttu-id="464be-130">**obtener \_ elemento**</span><span class="sxs-lookup"><span data-stu-id="464be-130">**get\_Item**</span></span>](itmediacollection-get-item.md)                   | <span data-ttu-id="464be-131">Devuelve el medio correspondiente al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="464be-131">Returns the media corresponding to the specified index.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="464be-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="464be-132">Requirements</span></span>



| <span data-ttu-id="464be-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="464be-133">Requirement</span></span> | <span data-ttu-id="464be-134">Value</span><span class="sxs-lookup"><span data-stu-id="464be-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="464be-135">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="464be-135">TAPI version</span></span><br/> | <span data-ttu-id="464be-136">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="464be-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="464be-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="464be-137">Header</span></span><br/>       | <dl> <span data-ttu-id="464be-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="464be-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="464be-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="464be-139">Library</span></span><br/>      | <dl> <span data-ttu-id="464be-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="464be-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="464be-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="464be-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="464be-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="464be-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

