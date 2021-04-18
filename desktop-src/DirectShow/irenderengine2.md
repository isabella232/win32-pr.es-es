---
description: La interfaz IRenderEngine2 permite que la aplicación Reemplace el filtro de cambio de tamaño de vídeo predeterminado utilizado por los servicios de edición de DirectShow (DES). El motor de representación básico y el motor de representación inteligente admiten esta interfaz.
ms.assetid: 37603c73-e199-431a-9a1e-a40c77755c70
title: Interfaz IRenderEngine2 (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ed7802cf3d47d745b4e4733bb1fb60c61130b44a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681025"
---
# <a name="irenderengine2-interface"></a><span data-ttu-id="775f4-104">Interfaz IRenderEngine2</span><span class="sxs-lookup"><span data-stu-id="775f4-104">IRenderEngine2 interface</span></span>

> [!Note]  
> <span data-ttu-id="775f4-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="775f4-105">\[Deprecated.</span></span> <span data-ttu-id="775f4-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="775f4-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="775f4-107">La `IRenderEngine2` interfaz permite que la aplicación Reemplace el filtro de cambio de tamaño de vídeo predeterminado utilizado por los servicios de edición de DirectShow (des).</span><span class="sxs-lookup"><span data-stu-id="775f4-107">The `IRenderEngine2` interface enables the application to replace the default video resizing filter used by DirectShow Editing Services (DES).</span></span> <span data-ttu-id="775f4-108">El [motor de representación básico](basic-render-engine.md) y el [motor de representación inteligente](smart-render-engine.md) admiten esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="775f4-108">The [Basic Render Engine](basic-render-engine.md) and the [Smart Render Engine](smart-render-engine.md) both support this interface.</span></span>

## <a name="members"></a><span data-ttu-id="775f4-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="775f4-109">Members</span></span>

<span data-ttu-id="775f4-110">La interfaz **IRenderEngine2** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="775f4-110">The **IRenderEngine2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="775f4-111">**IRenderEngine2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="775f4-111">**IRenderEngine2** also has these types of members:</span></span>

-   [<span data-ttu-id="775f4-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="775f4-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="775f4-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="775f4-113">Methods</span></span>

<span data-ttu-id="775f4-114">La interfaz **IRenderEngine2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="775f4-114">The **IRenderEngine2** interface has these methods.</span></span>



| <span data-ttu-id="775f4-115">Método</span><span class="sxs-lookup"><span data-stu-id="775f4-115">Method</span></span>                                                  | <span data-ttu-id="775f4-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="775f4-116">Description</span></span>                                                                             |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="775f4-117">**SetResizerGUID**</span><span class="sxs-lookup"><span data-stu-id="775f4-117">**SetResizerGUID**</span></span>](irenderengine2-setresizerguid.md) | <span data-ttu-id="775f4-118">Especifica el CLSID de un filtro de cambio de tamaño personalizado proporcionado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="775f4-118">Specifies the CLSID of a custom resizing filter provided by the application.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="775f4-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="775f4-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="775f4-120">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="775f4-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="775f4-121">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="775f4-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="775f4-122">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="775f4-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="775f4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="775f4-123">Requirements</span></span>



| <span data-ttu-id="775f4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="775f4-124">Requirement</span></span> | <span data-ttu-id="775f4-125">Value</span><span class="sxs-lookup"><span data-stu-id="775f4-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="775f4-126">Versión</span><span class="sxs-lookup"><span data-stu-id="775f4-126">Version</span></span><br/> | <span data-ttu-id="775f4-127">DirectX 9,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="775f4-127">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="775f4-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="775f4-128">Header</span></span><br/>  | <dl> <span data-ttu-id="775f4-129"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="775f4-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="775f4-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="775f4-130">Library</span></span><br/> | <dl> <span data-ttu-id="775f4-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="775f4-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="775f4-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="775f4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="775f4-133">Proporcionar un tamaño de vídeo personalizado</span><span class="sxs-lookup"><span data-stu-id="775f4-133">Providing a Custom Video Resizer</span></span>](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
