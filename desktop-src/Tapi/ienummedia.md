---
description: 'La interfaz IEnumMedia proporciona métodos de enumeración estándar de COM para la interfaz ITMedia. El método ITMediaCollection:: get \_ EnumerationIf devuelve un puntero a IEnumMedia.'
ms.assetid: 827f8866-2445-4b7c-88fe-eed19f48c93b
title: Interfaz IEnumMedia (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7127e7d1d751ee487ad5b86326602cfcfe5aae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691011"
---
# <a name="ienummedia-interface"></a><span data-ttu-id="70351-104">Interfaz IEnumMedia</span><span class="sxs-lookup"><span data-stu-id="70351-104">IEnumMedia interface</span></span>

<span data-ttu-id="70351-105">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="70351-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="70351-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="70351-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="70351-107">La interfaz **IEnumMedia** proporciona métodos de enumeración estándar de com para la interfaz [**ITMedia**](itmedia.md) .</span><span class="sxs-lookup"><span data-stu-id="70351-107">The **IEnumMedia** interface provides COM-standard enumeration methods for the [**ITMedia**](itmedia.md) interface.</span></span> <span data-ttu-id="70351-108">El método [**ITMediaCollection:: get \_ EnumerationIf**](itmediacollection-get-enumerationif.md) devuelve un puntero a **IEnumMedia**.</span><span class="sxs-lookup"><span data-stu-id="70351-108">The [**ITMediaCollection::get\_EnumerationIf**](itmediacollection-get-enumerationif.md) method returns a pointer to **IEnumMedia**.</span></span>

## <a name="members"></a><span data-ttu-id="70351-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="70351-109">Members</span></span>

<span data-ttu-id="70351-110">La interfaz **IEnumMedia** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="70351-110">The **IEnumMedia** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="70351-111">**IEnumMedia** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="70351-111">**IEnumMedia** also has these types of members:</span></span>

-   [<span data-ttu-id="70351-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="70351-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="70351-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="70351-113">Methods</span></span>

<span data-ttu-id="70351-114">La interfaz **IEnumMedia** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="70351-114">The **IEnumMedia** interface has these methods.</span></span>



| <span data-ttu-id="70351-115">Método</span><span class="sxs-lookup"><span data-stu-id="70351-115">Method</span></span>                            | <span data-ttu-id="70351-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="70351-116">Description</span></span>                                                                                        |
|:----------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70351-117">**Clonar**</span><span class="sxs-lookup"><span data-stu-id="70351-117">**Clone**</span></span>](ienummedia-clone.md) | <span data-ttu-id="70351-118">Crea otro enumerador que contiene el mismo estado de enumeración que el actual.</span><span class="sxs-lookup"><span data-stu-id="70351-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="70351-119">**Next**</span><span class="sxs-lookup"><span data-stu-id="70351-119">**Next**</span></span>](ienummedia-next.md)   | <span data-ttu-id="70351-120">Obtiene el siguiente número de elementos especificado en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="70351-120">Gets the next specified number of elements in the enumeration sequence.</span></span><br/>                 |
| [<span data-ttu-id="70351-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="70351-121">**Reset**</span></span>](ienummedia-reset.md) | <span data-ttu-id="70351-122">Se restablece al principio de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="70351-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="70351-123">**Omitir**</span><span class="sxs-lookup"><span data-stu-id="70351-123">**Skip**</span></span>](ienummedia-skip.md)   | <span data-ttu-id="70351-124">Omite el siguiente número de elementos especificado en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="70351-124">Skips over the next specified number of elements in the enumeration sequence.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="70351-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70351-125">Requirements</span></span>



| <span data-ttu-id="70351-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="70351-126">Requirement</span></span> | <span data-ttu-id="70351-127">Value</span><span class="sxs-lookup"><span data-stu-id="70351-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70351-128">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="70351-128">TAPI version</span></span><br/> | <span data-ttu-id="70351-129">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="70351-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="70351-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70351-130">Header</span></span><br/>       | <dl> <span data-ttu-id="70351-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="70351-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="70351-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="70351-132">Library</span></span><br/>      | <dl> <span data-ttu-id="70351-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70351-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="70351-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="70351-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="70351-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70351-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

