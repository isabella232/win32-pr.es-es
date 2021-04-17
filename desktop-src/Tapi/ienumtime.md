---
description: 'La interfaz IEnumTime proporciona métodos de enumeración estándar de COM para la interfaz ITTime. El método ITTimeCollection:: get \_ EnumerationIf devuelve un puntero a IEnumTime.'
ms.assetid: 395d7830-9a70-473a-8a89-4b4db48d5774
title: Interfaz IEnumTime (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2336f435ec322694847c776ac92ade93e8791207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680322"
---
# <a name="ienumtime-interface"></a><span data-ttu-id="8ba99-104">Interfaz IEnumTime</span><span class="sxs-lookup"><span data-stu-id="8ba99-104">IEnumTime interface</span></span>

<span data-ttu-id="8ba99-105">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8ba99-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8ba99-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="8ba99-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8ba99-107">La interfaz **IEnumTime** proporciona métodos de enumeración estándar de com para la interfaz [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="8ba99-107">The **IEnumTime** interface provides COM-standard enumeration methods for the [**ITTime**](ittime.md) interface.</span></span> <span data-ttu-id="8ba99-108">El método [**ITTimeCollection:: get \_ EnumerationIf**](ittimecollection-get-enumerationif.md) devuelve un puntero a **IEnumTime**.</span><span class="sxs-lookup"><span data-stu-id="8ba99-108">The [**ITTimeCollection::get\_EnumerationIf**](ittimecollection-get-enumerationif.md) method returns a pointer to **IEnumTime**.</span></span>

## <a name="members"></a><span data-ttu-id="8ba99-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="8ba99-109">Members</span></span>

<span data-ttu-id="8ba99-110">La interfaz **IEnumTime** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8ba99-110">The **IEnumTime** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8ba99-111">**IEnumTime** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8ba99-111">**IEnumTime** also has these types of members:</span></span>

-   [<span data-ttu-id="8ba99-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="8ba99-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8ba99-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="8ba99-113">Methods</span></span>

<span data-ttu-id="8ba99-114">La interfaz **IEnumTime** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="8ba99-114">The **IEnumTime** interface has these methods.</span></span>



| <span data-ttu-id="8ba99-115">Método</span><span class="sxs-lookup"><span data-stu-id="8ba99-115">Method</span></span>                           | <span data-ttu-id="8ba99-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ba99-116">Description</span></span>                                                                                        |
|:---------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ba99-117">**Clonar**</span><span class="sxs-lookup"><span data-stu-id="8ba99-117">**Clone**</span></span>](ienumtime-clone.md) | <span data-ttu-id="8ba99-118">Crea otro enumerador que contiene el mismo estado de enumeración que el actual.</span><span class="sxs-lookup"><span data-stu-id="8ba99-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="8ba99-119">**Next**</span><span class="sxs-lookup"><span data-stu-id="8ba99-119">**Next**</span></span>](ienumtime-next.md)   | <span data-ttu-id="8ba99-120">Obtiene el siguiente número de elementos especificado en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="8ba99-120">Gets the next specified number of elements in the enumeration sequence.</span></span><br/>                 |
| [<span data-ttu-id="8ba99-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="8ba99-121">**Reset**</span></span>](ienumtime-reset.md) | <span data-ttu-id="8ba99-122">Se restablece al principio de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="8ba99-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="8ba99-123">**Omitir**</span><span class="sxs-lookup"><span data-stu-id="8ba99-123">**Skip**</span></span>](ienumtime-skip.md)   | <span data-ttu-id="8ba99-124">Omite el siguiente número de elementos especificado en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="8ba99-124">Skips over the next specified number of elements in the enumeration sequence.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="8ba99-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ba99-125">Requirements</span></span>



| <span data-ttu-id="8ba99-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ba99-126">Requirement</span></span> | <span data-ttu-id="8ba99-127">Value</span><span class="sxs-lookup"><span data-stu-id="8ba99-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ba99-128">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="8ba99-128">TAPI version</span></span><br/> | <span data-ttu-id="8ba99-129">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="8ba99-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8ba99-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ba99-130">Header</span></span><br/>       | <dl> <span data-ttu-id="8ba99-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ba99-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8ba99-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ba99-132">Library</span></span><br/>      | <dl> <span data-ttu-id="8ba99-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ba99-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8ba99-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8ba99-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="8ba99-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ba99-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

