---
description: La interfaz ISmartRenderEngine proporciona métodos que admiten la recompresión inteligente en los servicios de edición de DirectShow (DES). El motor de representación inteligente expone esta interfaz.
ms.assetid: 0e03708f-e471-4188-a212-ec5e951d20fa
title: Interfaz ISmartRenderEngine (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e82ba73764adc27ff366533c3b5cfdc2eebc7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679472"
---
# <a name="ismartrenderengine-interface"></a><span data-ttu-id="9c112-104">Interfaz ISmartRenderEngine</span><span class="sxs-lookup"><span data-stu-id="9c112-104">ISmartRenderEngine interface</span></span>

> [!Note]  
> <span data-ttu-id="9c112-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="9c112-105">\[Deprecated.</span></span> <span data-ttu-id="9c112-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9c112-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9c112-107">La `ISmartRenderEngine` interfaz proporciona métodos que admiten la recompresión inteligente en los [servicios de edición de DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="9c112-107">The `ISmartRenderEngine` interface provides methods that support smart recompression in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="9c112-108">El motor de representación inteligente expone esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="9c112-108">The smart render engine exposes this interface.</span></span>

## <a name="members"></a><span data-ttu-id="9c112-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="9c112-109">Members</span></span>

<span data-ttu-id="9c112-110">La interfaz **ISmartRenderEngine** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9c112-110">The **ISmartRenderEngine** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9c112-111">**ISmartRenderEngine** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9c112-111">**ISmartRenderEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="9c112-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="9c112-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9c112-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="9c112-113">Methods</span></span>

<span data-ttu-id="9c112-114">La interfaz **ISmartRenderEngine** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9c112-114">The **ISmartRenderEngine** interface has these methods.</span></span>



| <span data-ttu-id="9c112-115">Método</span><span class="sxs-lookup"><span data-stu-id="9c112-115">Method</span></span>                                                                | <span data-ttu-id="9c112-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c112-116">Description</span></span>                                                                          |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c112-117">**GetGroupCompressor**</span><span class="sxs-lookup"><span data-stu-id="9c112-117">**GetGroupCompressor**</span></span>](ismartrenderengine-getgroupcompressor.md)   | <span data-ttu-id="9c112-118">Recupera el filtro de compresión para el grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="9c112-118">Retrieves the compression filter for the specified group.</span></span><br/>                 |
| [<span data-ttu-id="9c112-119">**SetFindCompressorCB**</span><span class="sxs-lookup"><span data-stu-id="9c112-119">**SetFindCompressorCB**</span></span>](ismartrenderengine-setfindcompressorcb.md) | <span data-ttu-id="9c112-120">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="9c112-120">Not implemented.</span></span><br/>                                                          |
| [<span data-ttu-id="9c112-121">**SetGroupCompressor**</span><span class="sxs-lookup"><span data-stu-id="9c112-121">**SetGroupCompressor**</span></span>](ismartrenderengine-setgroupcompressor.md)   | <span data-ttu-id="9c112-122">Especifica un filtro de compresión que se va a utilizar al representar el grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="9c112-122">Specifies a compression filter to use when rendering the specified group.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9c112-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c112-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9c112-124">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="9c112-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9c112-125">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9c112-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9c112-126">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9c112-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9c112-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c112-127">Requirements</span></span>



| <span data-ttu-id="9c112-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c112-128">Requirement</span></span> | <span data-ttu-id="9c112-129">Value</span><span class="sxs-lookup"><span data-stu-id="9c112-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c112-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c112-130">Header</span></span><br/>  | <dl> <span data-ttu-id="9c112-131"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c112-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9c112-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c112-132">Library</span></span><br/> | <dl> <span data-ttu-id="9c112-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c112-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c112-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c112-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c112-135">Representar un proyecto</span><span class="sxs-lookup"><span data-stu-id="9c112-135">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 
