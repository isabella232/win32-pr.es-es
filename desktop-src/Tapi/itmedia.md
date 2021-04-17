---
description: La interfaz ITMedia es una representación de los medios en un protocolo de descriptor de sesión (SDP, consulte RFC 2327).
ms.assetid: f5cd7971-3456-4e2f-8808-deb16678099a
title: Interfaz ITMedia (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd00d7eab685fe99b089556bcdb0ed2bf6329df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680464"
---
# <a name="itmedia-interface"></a><span data-ttu-id="2d78c-103">Interfaz ITMedia</span><span class="sxs-lookup"><span data-stu-id="2d78c-103">ITMedia interface</span></span>

<span data-ttu-id="2d78c-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2d78c-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2d78c-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="2d78c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2d78c-106">La interfaz **ITMedia** es una representación de los medios en un protocolo de descriptor de sesión (SDP, consulte RFC 2327).</span><span class="sxs-lookup"><span data-stu-id="2d78c-106">The **ITMedia** interface is a representation of media in a Session Descriptor Protocol (SDP, see RFC 2327).</span></span> <span data-ttu-id="2d78c-107">Esta interfaz exporta métodos para obtener y establecer las propiedades de los elementos multimedia básicos, como el tipo.</span><span class="sxs-lookup"><span data-stu-id="2d78c-107">This interface exports methods to get and set basic media properties, such as type.</span></span> <span data-ttu-id="2d78c-108">Los métodos [**ITMediaCollection:: get \_ Item**](itmediacollection-get-item.md) y [**ITMediaCollection:: Create**](itmediacollection-create.md) crean la interfaz **ITMedia** .</span><span class="sxs-lookup"><span data-stu-id="2d78c-108">The [**ITMediaCollection::get\_Item**](itmediacollection-get-item.md) and [**ITMediaCollection::Create**](itmediacollection-create.md) methods create the **ITMedia** interface.</span></span>

## <a name="members"></a><span data-ttu-id="2d78c-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2d78c-109">Members</span></span>

<span data-ttu-id="2d78c-110">La interfaz **ITMedia** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="2d78c-110">The **ITMedia** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="2d78c-111">**ITMedia** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2d78c-111">**ITMedia** also has these types of members:</span></span>

-   [<span data-ttu-id="2d78c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="2d78c-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2d78c-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="2d78c-113">Methods</span></span>

<span data-ttu-id="2d78c-114">La interfaz **ITMedia** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2d78c-114">The **ITMedia** interface has these methods.</span></span>



| <span data-ttu-id="2d78c-115">Método</span><span class="sxs-lookup"><span data-stu-id="2d78c-115">Method</span></span>                                                          | <span data-ttu-id="2d78c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d78c-116">Description</span></span>                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d78c-117">**obtener \_ FormatCodes**</span><span class="sxs-lookup"><span data-stu-id="2d78c-117">**get\_FormatCodes**</span></span>](itmedia-get-formatcodes.md)             | <span data-ttu-id="2d78c-118">Obtiene la lista de códigos de formato de carga de medios.</span><span class="sxs-lookup"><span data-stu-id="2d78c-118">Gets the list of media payload format codes.</span></span><br/>                                          |
| [<span data-ttu-id="2d78c-119">**obtener \_ MEDIANAME**</span><span class="sxs-lookup"><span data-stu-id="2d78c-119">**get\_MediaName**</span></span>](itmedia-get-medianame.md)                 | <span data-ttu-id="2d78c-120">Obtiene el nombre del medio.</span><span class="sxs-lookup"><span data-stu-id="2d78c-120">Gets the media name.</span></span><br/>                                                                  |
| [<span data-ttu-id="2d78c-121">**obtener \_ MediaTitle**</span><span class="sxs-lookup"><span data-stu-id="2d78c-121">**get\_MediaTitle**</span></span>](itmedia-get-mediatitle.md)               | <span data-ttu-id="2d78c-122">Obtiene el título del medio.</span><span class="sxs-lookup"><span data-stu-id="2d78c-122">Gets the media title.</span></span><br/>                                                                 |
| [<span data-ttu-id="2d78c-123">**obtener \_ NumPorts**</span><span class="sxs-lookup"><span data-stu-id="2d78c-123">**get\_NumPorts**</span></span>](itmedia-get-numports.md)                   | <span data-ttu-id="2d78c-124">Obtiene el número de puertos necesarios para la sesión.</span><span class="sxs-lookup"><span data-stu-id="2d78c-124">Gets the number of ports needed for the session.</span></span><br/>                                      |
| [<span data-ttu-id="2d78c-125">**obtener \_ StartPort**</span><span class="sxs-lookup"><span data-stu-id="2d78c-125">**get\_StartPort**</span></span>](itmedia-get-startport.md)                 | <span data-ttu-id="2d78c-126">Obtiene el valor del puerto de 16 bits para el primer puerto.</span><span class="sxs-lookup"><span data-stu-id="2d78c-126">Gets the 16-bit port value for the first port.</span></span><br/>                                        |
| [<span data-ttu-id="2d78c-127">**obtener \_ TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="2d78c-127">**get\_TransportProtocol**</span></span>](itmedia-get-transportprotocol.md) | <span data-ttu-id="2d78c-128">Obtiene el protocolo de transporte.</span><span class="sxs-lookup"><span data-stu-id="2d78c-128">Gets the transport protocol.</span></span><br/>                                                          |
| [<span data-ttu-id="2d78c-129">**Put \_ FormatCodes**</span><span class="sxs-lookup"><span data-stu-id="2d78c-129">**put\_FormatCodes**</span></span>](itmedia-put-formatcodes.md)             | <span data-ttu-id="2d78c-130">Establece la lista de códigos de formato de carga de medios.</span><span class="sxs-lookup"><span data-stu-id="2d78c-130">Sets the list of media payload format codes.</span></span><br/>                                          |
| [<span data-ttu-id="2d78c-131">**Put \_ MEDIANAME**</span><span class="sxs-lookup"><span data-stu-id="2d78c-131">**put\_MediaName**</span></span>](itmedia-put-medianame.md)                 | <span data-ttu-id="2d78c-132">Establece el nombre del medio.</span><span class="sxs-lookup"><span data-stu-id="2d78c-132">Sets the media name.</span></span><br/>                                                                  |
| [<span data-ttu-id="2d78c-133">**Put \_ MediaTitle**</span><span class="sxs-lookup"><span data-stu-id="2d78c-133">**put\_MediaTitle**</span></span>](itmedia-put-mediatitle.md)               | <span data-ttu-id="2d78c-134">Establece el título del medio.</span><span class="sxs-lookup"><span data-stu-id="2d78c-134">Sets the media title.</span></span><br/>                                                                 |
| [<span data-ttu-id="2d78c-135">**Put \_ TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="2d78c-135">**put\_TransportProtocol**</span></span>](itmedia-put-transportprotocol.md) | <span data-ttu-id="2d78c-136">Establece el protocolo de transporte.</span><span class="sxs-lookup"><span data-stu-id="2d78c-136">Sets the transport protocol.</span></span><br/>                                                          |
| [<span data-ttu-id="2d78c-137">**SetPortInfo**</span><span class="sxs-lookup"><span data-stu-id="2d78c-137">**SetPortInfo**</span></span>](itmedia-setportinfo.md)                      | <span data-ttu-id="2d78c-138">Establece el valor del puerto de 16 bits para el primer puerto y el número de puertos necesarios para la sesión.</span><span class="sxs-lookup"><span data-stu-id="2d78c-138">Sets the 16-bit port value for the first port and number of ports needed for session.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2d78c-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d78c-139">Requirements</span></span>



| <span data-ttu-id="2d78c-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d78c-140">Requirement</span></span> | <span data-ttu-id="2d78c-141">Value</span><span class="sxs-lookup"><span data-stu-id="2d78c-141">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d78c-142">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="2d78c-142">TAPI version</span></span><br/> | <span data-ttu-id="2d78c-143">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="2d78c-143">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2d78c-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d78c-144">Header</span></span><br/>       | <dl> <span data-ttu-id="2d78c-145"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d78c-145"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d78c-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d78c-146">Library</span></span><br/>      | <dl> <span data-ttu-id="2d78c-147"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d78c-147"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2d78c-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2d78c-148">DLL</span></span><br/>          | <dl> <span data-ttu-id="2d78c-149"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d78c-149"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d78c-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d78c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d78c-151">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="2d78c-151">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="2d78c-152">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="2d78c-152">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> <dt>

[<span data-ttu-id="2d78c-153">**ITSDP**</span><span class="sxs-lookup"><span data-stu-id="2d78c-153">**ITSDP**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="2d78c-154">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="2d78c-154">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

