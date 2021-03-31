---
title: Interfaz IMsRdpDrive
description: Contiene información sobre un objeto de unidad.
ms.assetid: 25e76657-a898-4581-a866-d66008540f50
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpDrive
- Servicios de Escritorio remoto de la interfaz IMsRdpDrive, descrito
topic_type:
- apiref
api_name:
- IMsRdpDrive
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 032e62ca54d6adccce9b27c8f7e95160c800759b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801142"
---
# <a name="imsrdpdrive-interface"></a><span data-ttu-id="eb369-105">Interfaz IMsRdpDrive</span><span class="sxs-lookup"><span data-stu-id="eb369-105">IMsRdpDrive interface</span></span>

<span data-ttu-id="eb369-106">Contiene información sobre un objeto de unidad.</span><span class="sxs-lookup"><span data-stu-id="eb369-106">Contains information about a drive object.</span></span>

## <a name="members"></a><span data-ttu-id="eb369-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="eb369-107">Members</span></span>

<span data-ttu-id="eb369-108">La interfaz **IMsRdpDrive** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="eb369-108">The **IMsRdpDrive** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="eb369-109">**IMsRdpDrive** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="eb369-109">**IMsRdpDrive** also has these types of members:</span></span>

-   [<span data-ttu-id="eb369-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eb369-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb369-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eb369-111">Properties</span></span>

<span data-ttu-id="eb369-112">La interfaz **IMsRdpDrive** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="eb369-112">The **IMsRdpDrive** interface has these properties.</span></span>



| <span data-ttu-id="eb369-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="eb369-113">Property</span></span>                                                            | <span data-ttu-id="eb369-114">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="eb369-114">Access type</span></span>           | <span data-ttu-id="eb369-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb369-115">Description</span></span>                                              |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [<span data-ttu-id="eb369-116">**Name**</span><span class="sxs-lookup"><span data-stu-id="eb369-116">**Name**</span></span>](imsrdpdrive-name.md)<br/>                         | <span data-ttu-id="eb369-117">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb369-117">Read-only</span></span><br/>  | <span data-ttu-id="eb369-118">Recupera el nombre de la unidad.</span><span class="sxs-lookup"><span data-stu-id="eb369-118">Retrieves the name of the drive.</span></span><br/>              |
| [<span data-ttu-id="eb369-119">**RedirectionState**</span><span class="sxs-lookup"><span data-stu-id="eb369-119">**RedirectionState**</span></span>](imsrdpdrive-redirectionstate.md)<br/> | <span data-ttu-id="eb369-120">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eb369-120">Read/write</span></span><br/> | <span data-ttu-id="eb369-121">Indica el estado de redireccionamiento de la unidad.</span><span class="sxs-lookup"><span data-stu-id="eb369-121">Indicates the redirection state of the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="eb369-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb369-122">Requirements</span></span>



| <span data-ttu-id="eb369-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb369-123">Requirement</span></span> | <span data-ttu-id="eb369-124">Value</span><span class="sxs-lookup"><span data-stu-id="eb369-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb369-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb369-125">Minimum supported client</span></span><br/> | <span data-ttu-id="eb369-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb369-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="eb369-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb369-127">Minimum supported server</span></span><br/> | <span data-ttu-id="eb369-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb369-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="eb369-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="eb369-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="eb369-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb369-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="eb369-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eb369-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb369-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb369-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="eb369-133">IID</span><span class="sxs-lookup"><span data-stu-id="eb369-133">IID</span></span><br/>                      | <span data-ttu-id="eb369-134">IID \_ IMsRdpDrive se define como d28b5458-f694-47a8-8e61-40356a767e46</span><span class="sxs-lookup"><span data-stu-id="eb369-134">IID\_IMsRdpDrive is defined as d28b5458-f694-47a8-8e61-40356a767e46</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="eb369-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb369-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb369-136">Referencia de Conexión web a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="eb369-136">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="eb369-137">**IMsRdpDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="eb369-137">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

