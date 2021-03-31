---
title: Interfaz IMsRdpDriveCollection
description: Representa una colección de objetos de unidad.
ms.assetid: 26926b85-021d-4678-845f-93ba62b2b4a3
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpDriveCollection
- Servicios de Escritorio remoto de la interfaz IMsRdpDriveCollection, descrito
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b2588ddb0945ba1fcab8fbb4c5b9b078a1af9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491627"
---
# <a name="imsrdpdrivecollection-interface"></a><span data-ttu-id="5e3bf-105">Interfaz IMsRdpDriveCollection</span><span class="sxs-lookup"><span data-stu-id="5e3bf-105">IMsRdpDriveCollection interface</span></span>

<span data-ttu-id="5e3bf-106">Representa una colección de objetos de unidad.</span><span class="sxs-lookup"><span data-stu-id="5e3bf-106">Represents a collection of drive objects.</span></span>

## <a name="members"></a><span data-ttu-id="5e3bf-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5e3bf-107">Members</span></span>

<span data-ttu-id="5e3bf-108">La interfaz **IMsRdpDriveCollection** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5e3bf-108">The **IMsRdpDriveCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5e3bf-109">**IMsRdpDriveCollection** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5e3bf-109">**IMsRdpDriveCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="5e3bf-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="5e3bf-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="5e3bf-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5e3bf-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5e3bf-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="5e3bf-112">Methods</span></span>

<span data-ttu-id="5e3bf-113">La interfaz **IMsRdpDriveCollection** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5e3bf-113">The **IMsRdpDriveCollection** interface has these methods.</span></span>



| <span data-ttu-id="5e3bf-114">Método</span><span class="sxs-lookup"><span data-stu-id="5e3bf-114">Method</span></span>                                                     | <span data-ttu-id="5e3bf-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e3bf-115">Description</span></span>                                                 |
|:-----------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="5e3bf-116">**RescanDrives**</span><span class="sxs-lookup"><span data-stu-id="5e3bf-116">**RescanDrives**</span></span>](imsrdpdrivecollection-rescandrives.md) | <span data-ttu-id="5e3bf-117">Actualiza la lista de objetos de la colección.</span><span class="sxs-lookup"><span data-stu-id="5e3bf-117">Refreshes the list of objects in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5e3bf-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5e3bf-118">Properties</span></span>

<span data-ttu-id="5e3bf-119">La interfaz **IMsRdpDriveCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5e3bf-119">The **IMsRdpDriveCollection** interface has these properties.</span></span>



| <span data-ttu-id="5e3bf-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5e3bf-120">Property</span></span>                                                              | <span data-ttu-id="5e3bf-121">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="5e3bf-121">Access type</span></span>          | <span data-ttu-id="5e3bf-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e3bf-122">Description</span></span>                                                  |
|:----------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="5e3bf-123">**DriveByIndex**</span><span class="sxs-lookup"><span data-stu-id="5e3bf-123">**DriveByIndex**</span></span>](imsrdpdrivecollection-drivebyindex.md)<br/> | <span data-ttu-id="5e3bf-124">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e3bf-124">Read-only</span></span><br/> | <span data-ttu-id="5e3bf-125">Recupera la unidad en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="5e3bf-125">Retrieves the drive at the specified index.</span></span><br/>       |
| [<span data-ttu-id="5e3bf-126">**DriveCount**</span><span class="sxs-lookup"><span data-stu-id="5e3bf-126">**DriveCount**</span></span>](imsrdpdrivecollection-drivecount.md)<br/>     | <span data-ttu-id="5e3bf-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e3bf-127">Read-only</span></span><br/> | <span data-ttu-id="5e3bf-128">Recupera el recuento de objetos de la colección.</span><span class="sxs-lookup"><span data-stu-id="5e3bf-128">Retrieves the count of objects in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5e3bf-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e3bf-129">Requirements</span></span>



| <span data-ttu-id="5e3bf-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e3bf-130">Requirement</span></span> | <span data-ttu-id="5e3bf-131">Value</span><span class="sxs-lookup"><span data-stu-id="5e3bf-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e3bf-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e3bf-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5e3bf-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e3bf-133">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="5e3bf-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e3bf-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5e3bf-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e3bf-135">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5e3bf-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5e3bf-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="5e3bf-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e3bf-137"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="5e3bf-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5e3bf-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e3bf-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e3bf-139"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="5e3bf-140">IID</span><span class="sxs-lookup"><span data-stu-id="5e3bf-140">IID</span></span><br/>                      | <span data-ttu-id="5e3bf-141">IID \_ IMsRdpDriveCollection se define como 7ff17599-da2c-4677-Ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="5e3bf-141">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5e3bf-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e3bf-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e3bf-143">Referencia de Conexión web a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="5e3bf-143">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="5e3bf-144">**IMsRdpDrive**</span><span class="sxs-lookup"><span data-stu-id="5e3bf-144">**IMsRdpDrive**</span></span>](imsrdpdrive.md)
</dt> </dl>

 

