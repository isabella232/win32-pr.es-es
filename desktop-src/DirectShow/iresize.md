---
description: 'La interfaz IResize debe ser compatible con cualquier filtro de tamaño de vídeo personalizado para los servicios de edición de DirectShow (DES). Para establecer un filtro de tamaño personalizado, llame al método IRenderEngine2:: SetResizerGUID en el motor de representación.'
ms.assetid: 4740dbff-0881-45e8-b382-98ed9d055403
title: Interfaz IResize (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1b9684ed6f2d2901159dde5a79bb4563ca0b2bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679067"
---
# <a name="iresize-interface"></a><span data-ttu-id="3b9c7-104">Interfaz IResize</span><span class="sxs-lookup"><span data-stu-id="3b9c7-104">IResize interface</span></span>

> [!Note]  
> <span data-ttu-id="3b9c7-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="3b9c7-105">\[Deprecated.</span></span> <span data-ttu-id="3b9c7-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3b9c7-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3b9c7-107">La `IResize` interfaz debe ser compatible con cualquier filtro de tamaño de vídeo personalizado para los servicios de edición de DirectShow (des).</span><span class="sxs-lookup"><span data-stu-id="3b9c7-107">The `IResize` interface must be supported by any custom video resizer filter for DirectShow Editing Services (DES).</span></span> <span data-ttu-id="3b9c7-108">Para establecer un filtro de tamaño personalizado, llame al método [**IRenderEngine2:: SetResizerGUID**](irenderengine2-setresizerguid.md) en el motor de representación.</span><span class="sxs-lookup"><span data-stu-id="3b9c7-108">To set a custom resizer filter, call the [**IRenderEngine2::SetResizerGUID**](irenderengine2-setresizerguid.md) method on the render engine.</span></span>

## <a name="members"></a><span data-ttu-id="3b9c7-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="3b9c7-109">Members</span></span>

<span data-ttu-id="3b9c7-110">La interfaz **IResize** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3b9c7-110">The **IResize** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3b9c7-111">**IResize** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3b9c7-111">**IResize** also has these types of members:</span></span>

-   [<span data-ttu-id="3b9c7-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="3b9c7-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3b9c7-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="3b9c7-113">Methods</span></span>

<span data-ttu-id="3b9c7-114">La interfaz **IResize** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="3b9c7-114">The **IResize** interface has these methods.</span></span>



| <span data-ttu-id="3b9c7-115">Método</span><span class="sxs-lookup"><span data-stu-id="3b9c7-115">Method</span></span>                                          | <span data-ttu-id="3b9c7-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b9c7-116">Description</span></span>                                                  |
|:------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="3b9c7-117">**obtener \_ Input**</span><span class="sxs-lookup"><span data-stu-id="3b9c7-117">**get\_InputSize**</span></span>](iresize-get-inputsize.md) | <span data-ttu-id="3b9c7-118">Devuelve el tamaño de entrada actual del filtro de tamaño.</span><span class="sxs-lookup"><span data-stu-id="3b9c7-118">Returns the resizer filter's current input size.</span></span><br/>  |
| [<span data-ttu-id="3b9c7-119">**obtener \_ mediatype**</span><span class="sxs-lookup"><span data-stu-id="3b9c7-119">**get\_MediaType**</span></span>](iresize-get-mediatype.md) | <span data-ttu-id="3b9c7-120">Devuelve el tipo de medio de salida del filtro de tamaño.</span><span class="sxs-lookup"><span data-stu-id="3b9c7-120">Returns the resizer filter's output media type.</span></span><br/>   |
| [<span data-ttu-id="3b9c7-121">**obtener \_ tamaño**</span><span class="sxs-lookup"><span data-stu-id="3b9c7-121">**get\_Size**</span></span>](iresize-get-size.md)           | <span data-ttu-id="3b9c7-122">Devuelve el tamaño de salida actual y el modo de ajuste.</span><span class="sxs-lookup"><span data-stu-id="3b9c7-122">Returns the current output size and stretch mode.</span></span><br/> |
| [<span data-ttu-id="3b9c7-123">**colocar \_ mediatype**</span><span class="sxs-lookup"><span data-stu-id="3b9c7-123">**put\_MediaType**</span></span>](iresize-put-mediatype.md) | <span data-ttu-id="3b9c7-124">Establece el tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="3b9c7-124">Sets the output media type.</span></span><br/>                       |
| [<span data-ttu-id="3b9c7-125">**poner \_ tamaño**</span><span class="sxs-lookup"><span data-stu-id="3b9c7-125">**put\_Size**</span></span>](iresize-put-size.md)           | <span data-ttu-id="3b9c7-126">Establece el tamaño de salida y el modo de ajuste.</span><span class="sxs-lookup"><span data-stu-id="3b9c7-126">Sets the output size and stretch mode.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="3b9c7-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b9c7-127">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3b9c7-128">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="3b9c7-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3b9c7-129">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3b9c7-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3b9c7-130">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3b9c7-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3b9c7-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b9c7-131">Requirements</span></span>



| <span data-ttu-id="3b9c7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b9c7-132">Requirement</span></span> | <span data-ttu-id="3b9c7-133">Value</span><span class="sxs-lookup"><span data-stu-id="3b9c7-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b9c7-134">Versión</span><span class="sxs-lookup"><span data-stu-id="3b9c7-134">Version</span></span><br/> | <span data-ttu-id="3b9c7-135">DirectX 9,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="3b9c7-135">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="3b9c7-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b9c7-136">Header</span></span><br/>  | <dl> <span data-ttu-id="3b9c7-137"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b9c7-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3b9c7-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b9c7-138">Library</span></span><br/> | <dl> <span data-ttu-id="3b9c7-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b9c7-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b9c7-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b9c7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b9c7-141">Proporcionar un tamaño de vídeo personalizado</span><span class="sxs-lookup"><span data-stu-id="3b9c7-141">Providing a Custom Video Resizer</span></span>](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
