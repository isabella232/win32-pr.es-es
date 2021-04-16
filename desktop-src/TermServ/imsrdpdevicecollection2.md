---
title: Interfaz IMsRdpDeviceCollection2
description: Representa una colección de objetos de dispositivo. Se trata de una mejora de la interfaz IMsRdpDeviceCollection.
ms.assetid: df4d704c-e031-4df1-aed1-11aacf8a6992
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpDeviceCollection2
- Servicios de Escritorio remoto de la interfaz IMsRdpDeviceCollection2, descrito
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ea35c0a66ad8bf5d291062eafb7be3ceae4ac58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686066"
---
# <a name="imsrdpdevicecollection2-interface"></a><span data-ttu-id="ab2fa-106">Interfaz IMsRdpDeviceCollection2</span><span class="sxs-lookup"><span data-stu-id="ab2fa-106">IMsRdpDeviceCollection2 interface</span></span>

<span data-ttu-id="ab2fa-107">Representa una colección de objetos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab2fa-107">Represents a collection of device objects.</span></span> <span data-ttu-id="ab2fa-108">Se trata de una mejora de la interfaz [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md) .</span><span class="sxs-lookup"><span data-stu-id="ab2fa-108">This is an enhancement to the [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="ab2fa-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="ab2fa-109">Members</span></span>

<span data-ttu-id="ab2fa-110">La interfaz **IMsRdpDeviceCollection2** hereda de [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md).</span><span class="sxs-lookup"><span data-stu-id="ab2fa-110">The **IMsRdpDeviceCollection2** interface inherits from [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md).</span></span> <span data-ttu-id="ab2fa-111">**IMsRdpDeviceCollection2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ab2fa-111">**IMsRdpDeviceCollection2** also has these types of members:</span></span>

-   [<span data-ttu-id="ab2fa-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="ab2fa-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ab2fa-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="ab2fa-113">Methods</span></span>

<span data-ttu-id="ab2fa-114">La interfaz **IMsRdpDeviceCollection2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ab2fa-114">The **IMsRdpDeviceCollection2** interface has these methods.</span></span>



| <span data-ttu-id="ab2fa-115">Método</span><span class="sxs-lookup"><span data-stu-id="ab2fa-115">Method</span></span>                                                                         | <span data-ttu-id="ab2fa-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab2fa-116">Description</span></span>                                                                                                 |
|:-------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab2fa-117">**AddDeviceByInstanceId**</span><span class="sxs-lookup"><span data-stu-id="ab2fa-117">**AddDeviceByInstanceId**</span></span>](imsrdpdevicecollection2-adddevicebyinstanceid.md) | <span data-ttu-id="ab2fa-118">Agrega un dispositivo que no está en la lista a la recopilación de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ab2fa-118">Adds an unlisted device to the device collection.</span></span><br/>                                                |
| [<span data-ttu-id="ab2fa-119">**RedirectNow**</span><span class="sxs-lookup"><span data-stu-id="ab2fa-119">**RedirectNow**</span></span>](imsrdpdevicecollection2-redirectnow.md)                     | <span data-ttu-id="ab2fa-120">Fuerza la redirección o eliminación de los dispositivos que se seleccionaron o anularon de la colección.</span><span class="sxs-lookup"><span data-stu-id="ab2fa-120">Forces devices that were selected or unselected from the collection to be redirected or removed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ab2fa-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab2fa-121">Requirements</span></span>



| <span data-ttu-id="ab2fa-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab2fa-122">Requirement</span></span> | <span data-ttu-id="ab2fa-123">Value</span><span class="sxs-lookup"><span data-stu-id="ab2fa-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab2fa-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab2fa-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ab2fa-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ab2fa-125">Windows 8</span></span><br/>                                                                       |
| <span data-ttu-id="ab2fa-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab2fa-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ab2fa-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ab2fa-127">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="ab2fa-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ab2fa-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="ab2fa-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab2fa-129"><dt>MsTscAx.dll</dt></span></span> </dl>     |
| <span data-ttu-id="ab2fa-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ab2fa-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab2fa-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab2fa-131"><dt>MsTscAx.dll</dt></span></span> </dl>     |
| <span data-ttu-id="ab2fa-132">IID</span><span class="sxs-lookup"><span data-stu-id="ab2fa-132">IID</span></span><br/>                      | <span data-ttu-id="ab2fa-133">IID \_ IMsRdpDeviceCollection2 se define como e0e5d68a-f2e7-4350-ADFE-ac0e08d74de0</span><span class="sxs-lookup"><span data-stu-id="ab2fa-133">IID\_IMsRdpDeviceCollection2 is defined as e0e5d68a-f2e7-4350-adfe-ac0e08d74de0</span></span><br/> |



 

 





