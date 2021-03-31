---
title: Interfaz IMsRdpDriveV2
description: Contiene información sobre un objeto de unidad. Se trata de una mejora de la interfaz IMsRdpDrive.
ms.assetid: 0d804fcc-960f-48f7-9794-b7be8d7e258e
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpDriveV2
- Servicios de Escritorio remoto de la interfaz IMsRdpDriveV2, descrito
topic_type:
- apiref
api_name:
- IMsRdpDriveV2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c397e96d4f3b0dbb172c6e10eba4e09ff96e37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149996"
---
# <a name="imsrdpdrivev2-interface"></a><span data-ttu-id="0d6e7-106">Interfaz IMsRdpDriveV2</span><span class="sxs-lookup"><span data-stu-id="0d6e7-106">IMsRdpDriveV2 interface</span></span>

<span data-ttu-id="0d6e7-107">Contiene información sobre un objeto de unidad.</span><span class="sxs-lookup"><span data-stu-id="0d6e7-107">Contains information about a drive object.</span></span> <span data-ttu-id="0d6e7-108">Se trata de una mejora de la interfaz [**IMsRdpDrive**](imsrdpdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="0d6e7-108">This is an enhancement of the [**IMsRdpDrive**](imsrdpdrive.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="0d6e7-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="0d6e7-109">Members</span></span>

<span data-ttu-id="0d6e7-110">La interfaz **IMsRdpDriveV2** hereda de [**IMsRdpDrive**](imsrdpdrive.md).</span><span class="sxs-lookup"><span data-stu-id="0d6e7-110">The **IMsRdpDriveV2** interface inherits from [**IMsRdpDrive**](imsrdpdrive.md).</span></span> <span data-ttu-id="0d6e7-111">**IMsRdpDriveV2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0d6e7-111">**IMsRdpDriveV2** also has these types of members:</span></span>

-   [<span data-ttu-id="0d6e7-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0d6e7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d6e7-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0d6e7-113">Properties</span></span>

<span data-ttu-id="0d6e7-114">La interfaz **IMsRdpDriveV2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0d6e7-114">The **IMsRdpDriveV2** interface has these properties.</span></span>



| <span data-ttu-id="0d6e7-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0d6e7-115">Property</span></span>                                                              | <span data-ttu-id="0d6e7-116">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="0d6e7-116">Access type</span></span>          | <span data-ttu-id="0d6e7-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d6e7-117">Description</span></span>                                                |
|:----------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="0d6e7-118">**DriveLetterIndex**</span><span class="sxs-lookup"><span data-stu-id="0d6e7-118">**DriveLetterIndex**</span></span>](imsrdpdrivev2-driveletterindex.md)<br/> | <span data-ttu-id="0d6e7-119">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0d6e7-119">Read-only</span></span><br/> | <span data-ttu-id="0d6e7-120">Contiene el índice de la letra de la unidad.</span><span class="sxs-lookup"><span data-stu-id="0d6e7-120">Contains the index of the letter for the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0d6e7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d6e7-121">Requirements</span></span>



| <span data-ttu-id="0d6e7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d6e7-122">Requirement</span></span> | <span data-ttu-id="0d6e7-123">Value</span><span class="sxs-lookup"><span data-stu-id="0d6e7-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d6e7-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d6e7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0d6e7-125">Windows 7 con SP1</span><span class="sxs-lookup"><span data-stu-id="0d6e7-125">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="0d6e7-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d6e7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0d6e7-127">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0d6e7-127">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="0d6e7-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0d6e7-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="0d6e7-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d6e7-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0d6e7-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0d6e7-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d6e7-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d6e7-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0d6e7-132">IID</span><span class="sxs-lookup"><span data-stu-id="0d6e7-132">IID</span></span><br/>                      | <span data-ttu-id="0d6e7-133">IID \_ IMsRdpDriveV2 se define como 3e05417c-2721-4008-9d80-4edf1539c817</span><span class="sxs-lookup"><span data-stu-id="0d6e7-133">IID\_IMsRdpDriveV2 is defined as 3e05417c-2721-4008-9d80-4edf1539c817</span></span><br/>       |



 

 





