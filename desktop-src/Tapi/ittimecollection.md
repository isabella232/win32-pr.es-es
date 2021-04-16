---
description: La interfaz ITTimeCollection es una interfaz específica del proveedor para el objeto de BLOB de conferencia del Protocolo de descriptor de sesión (SDP).
ms.assetid: 6309e9f2-8a73-4d42-ae0a-2165352d6244
title: Interfaz ITTimeCollection (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19ca297a26b0eac34396726e6145a24fba5a2ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690234"
---
# <a name="ittimecollection-interface"></a><span data-ttu-id="672ba-103">Interfaz ITTimeCollection</span><span class="sxs-lookup"><span data-stu-id="672ba-103">ITTimeCollection interface</span></span>

<span data-ttu-id="672ba-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="672ba-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="672ba-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="672ba-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="672ba-106">La interfaz **ITTimeCollection** es una interfaz específica del proveedor para el objeto de BLOB de conferencia del Protocolo de descriptor de sesión (SDP).</span><span class="sxs-lookup"><span data-stu-id="672ba-106">The **ITTimeCollection** interface is a provider-specific interface for the Session Descriptor Protocol (SDP) conference blob object.</span></span> <span data-ttu-id="672ba-107">Esta interfaz permite el acceso a las interfaces de [**ITTime**](ittime.md) por índice y también habilita la creación y la eliminación de componentes de hora.</span><span class="sxs-lookup"><span data-stu-id="672ba-107">This interface allows access to [**ITTime**](ittime.md) interfaces by index, and also enable the creation and deletion of time components.</span></span> <span data-ttu-id="672ba-108">El método [**ITSdp:: get \_ TimeCollection**](itsdp-get-timecollection.md) crea la interfaz **ITTimeCollection** .</span><span class="sxs-lookup"><span data-stu-id="672ba-108">The [**ITSdp::get\_TimeCollection**](itsdp-get-timecollection.md) method creates the **ITTimeCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="672ba-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="672ba-109">Members</span></span>

<span data-ttu-id="672ba-110">La interfaz **ITTimeCollection** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="672ba-110">The **ITTimeCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="672ba-111">**ITTimeCollection** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="672ba-111">**ITTimeCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="672ba-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="672ba-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="672ba-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="672ba-113">Methods</span></span>

<span data-ttu-id="672ba-114">La interfaz **ITTimeCollection** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="672ba-114">The **ITTimeCollection** interface has these methods.</span></span>



| <span data-ttu-id="672ba-115">Método</span><span class="sxs-lookup"><span data-stu-id="672ba-115">Method</span></span>                                                           | <span data-ttu-id="672ba-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="672ba-116">Description</span></span>                                                                                                           |
|:-----------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="672ba-117">**A**</span><span class="sxs-lookup"><span data-stu-id="672ba-117">**Create**</span></span>](ittimecollection-create.md)                        | <span data-ttu-id="672ba-118">Crea un componente [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="672ba-118">Creates an [**ITTime**](ittime.md) component.</span></span><br/>                                                             |
| [<span data-ttu-id="672ba-119">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="672ba-119">**Delete**</span></span>](ittimecollection-delete.md)                        | <span data-ttu-id="672ba-120">Elimina un componente [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="672ba-120">Deletes an [**ITTime**](ittime.md) component.</span></span><br/>                                                             |
| [<span data-ttu-id="672ba-121">**obtener \_ \_ NewEnum**</span><span class="sxs-lookup"><span data-stu-id="672ba-121">**get\_\_NewEnum**</span></span>](ittimecollection-get--newenum.md)          | <span data-ttu-id="672ba-122">Devuelve un enumerador para la colección.</span><span class="sxs-lookup"><span data-stu-id="672ba-122">Returns an enumerator for the collection.</span></span><br/>                                                                  |
| [<span data-ttu-id="672ba-123">**obtener \_ recuento**</span><span class="sxs-lookup"><span data-stu-id="672ba-123">**get\_Count**</span></span>](ittimecollection-get-count.md)                 | <span data-ttu-id="672ba-124">Obtiene el número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="672ba-124">Gets number of items in collection.</span></span><br/>                                                                        |
| [<span data-ttu-id="672ba-125">**obtener \_ EnumerationIf**</span><span class="sxs-lookup"><span data-stu-id="672ba-125">**get\_EnumerationIf**</span></span>](ittimecollection-get-enumerationif.md) | <span data-ttu-id="672ba-126">Devuelve la interfaz de enumeración [**IEnumTime**](ienumtime.md) que enumera [**ITTime**](ittime.md).</span><span class="sxs-lookup"><span data-stu-id="672ba-126">Returns the [**IEnumTime**](ienumtime.md) enumeration interface that enumerates [**ITTime**](ittime.md).</span></span><br/> |
| [<span data-ttu-id="672ba-127">**obtener \_ elemento**</span><span class="sxs-lookup"><span data-stu-id="672ba-127">**get\_Item**</span></span>](ittimecollection-get-item.md)                   | <span data-ttu-id="672ba-128">Dado un índice, devuelve un elemento de la colección.</span><span class="sxs-lookup"><span data-stu-id="672ba-128">Given an index, returns an item in the collection.</span></span><br/>                                                         |



 

## <a name="requirements"></a><span data-ttu-id="672ba-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="672ba-129">Requirements</span></span>



| <span data-ttu-id="672ba-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="672ba-130">Requirement</span></span> | <span data-ttu-id="672ba-131">Value</span><span class="sxs-lookup"><span data-stu-id="672ba-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="672ba-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="672ba-132">TAPI version</span></span><br/> | <span data-ttu-id="672ba-133">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="672ba-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="672ba-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="672ba-134">Header</span></span><br/>       | <dl> <span data-ttu-id="672ba-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="672ba-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="672ba-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="672ba-136">Library</span></span><br/>      | <dl> <span data-ttu-id="672ba-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="672ba-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="672ba-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="672ba-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="672ba-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="672ba-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

