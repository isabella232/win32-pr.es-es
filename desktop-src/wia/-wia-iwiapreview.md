---
description: La interfaz IWiaPreview almacena en caché las imágenes sin filtrar internamente y las pasa a través de filtros de procesamiento de imágenes.
ms.assetid: 8a51c42b-aa1d-4df0-aba3-6aeb8e1ca2cf
title: Interfaz IWiaPreview (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 5e1c01daae4e86fa18c087b67bf902daaf6f8793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275461"
---
# <a name="iwiapreview-interface"></a><span data-ttu-id="5abb8-103">Interfaz IWiaPreview</span><span class="sxs-lookup"><span data-stu-id="5abb8-103">IWiaPreview interface</span></span>

<span data-ttu-id="5abb8-104">La interfaz **IWiaPreview** almacena en caché las imágenes sin filtrar internamente y las pasa a través de filtros de procesamiento de imágenes.</span><span class="sxs-lookup"><span data-stu-id="5abb8-104">The **IWiaPreview** interface caches unfiltered images internally and passes them through image processing filters.</span></span>

## <a name="members"></a><span data-ttu-id="5abb8-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="5abb8-105">Members</span></span>

<span data-ttu-id="5abb8-106">La interfaz **IWiaPreview** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5abb8-106">The **IWiaPreview** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5abb8-107">**IWiaPreview** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5abb8-107">**IWiaPreview** also has these types of members:</span></span>

-   [<span data-ttu-id="5abb8-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="5abb8-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5abb8-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5abb8-109">Methods</span></span>

<span data-ttu-id="5abb8-110">La interfaz **IWiaPreview** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5abb8-110">The **IWiaPreview** interface has these methods.</span></span>



| <span data-ttu-id="5abb8-111">Método</span><span class="sxs-lookup"><span data-stu-id="5abb8-111">Method</span></span>                                                  | <span data-ttu-id="5abb8-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5abb8-112">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5abb8-113">**Claridad**</span><span class="sxs-lookup"><span data-stu-id="5abb8-113">**Clear**</span></span>](-wia-iwiapreview-clear.md)                 | <span data-ttu-id="5abb8-114">Libera la imagen sin filtrar almacenada en memoria caché por el método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="5abb8-114">Releases the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="5abb8-115">También libera el filtro de procesamiento de imágenes.</span><span class="sxs-lookup"><span data-stu-id="5abb8-115">It also releases the image processing filter.</span></span> <br/>          |
| [<span data-ttu-id="5abb8-116">**DetectRegions**</span><span class="sxs-lookup"><span data-stu-id="5abb8-116">**DetectRegions**</span></span>](-wia-iwiapreview-detectregions.md) | <span data-ttu-id="5abb8-117">Invoca el filtro de segmentación de controladores y pasa al filtro la imagen sin filtrar almacenada en memoria caché por el método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="5abb8-117">Invokes the driver segmentation filter and passes the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method to the filter.</span></span> <br/> |
| [<span data-ttu-id="5abb8-118">**GetNewPreview**</span><span class="sxs-lookup"><span data-stu-id="5abb8-118">**GetNewPreview**</span></span>](-wia-iwiapreview-getnewpreview.md) | <span data-ttu-id="5abb8-119">Almacena en caché internamente la imagen sin filtrar devuelta por el controlador.</span><span class="sxs-lookup"><span data-stu-id="5abb8-119">Caches internally the unfiltered image returned from the driver.</span></span> <br/>                                                                                                                |
| [<span data-ttu-id="5abb8-120">**UpdatePreview**</span><span class="sxs-lookup"><span data-stu-id="5abb8-120">**UpdatePreview**</span></span>](-wia-iwiapreview-updatepreview.md) | <span data-ttu-id="5abb8-121">Obtiene la imagen sin filtrar almacenada en memoria caché por el método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="5abb8-121">Gets the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="5abb8-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5abb8-122">Remarks</span></span>

<span data-ttu-id="5abb8-123">El método [**IWiaTransfer::D scargar**](-wia-iwiatransfer-download.md) llama automáticamente a este filtro.</span><span class="sxs-lookup"><span data-stu-id="5abb8-123">This filter is called automatically by the [**IWiaTransfer::Download**](-wia-iwiatransfer-download.md) method.</span></span>

<span data-ttu-id="5abb8-124">La interfaz **IWiaPreview** , al igual que todas las interfaces del modelo de objetos componentes (com), hereda los métodos de interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5abb8-124">The **IWiaPreview** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="5abb8-125">Métodos IUnknown</span><span class="sxs-lookup"><span data-stu-id="5abb8-125">IUnknown Methods</span></span>                                        | <span data-ttu-id="5abb8-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="5abb8-126">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="5abb8-127">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="5abb8-127">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="5abb8-128">Devuelve punteros a las interfaces compatibles.</span><span class="sxs-lookup"><span data-stu-id="5abb8-128">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="5abb8-129">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="5abb8-129">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="5abb8-130">Incrementa el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="5abb8-130">Increments reference count.</span></span>               |
| [<span data-ttu-id="5abb8-131">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="5abb8-131">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="5abb8-132">Reduce el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="5abb8-132">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="5abb8-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5abb8-133">Requirements</span></span>



| <span data-ttu-id="5abb8-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5abb8-134">Requirement</span></span> | <span data-ttu-id="5abb8-135">Value</span><span class="sxs-lookup"><span data-stu-id="5abb8-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5abb8-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5abb8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5abb8-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5abb8-137">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5abb8-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5abb8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5abb8-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5abb8-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5abb8-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5abb8-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5abb8-141"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="5abb8-141"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="5abb8-142">IDL</span><span class="sxs-lookup"><span data-stu-id="5abb8-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5abb8-143"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5abb8-143"><dt>Wia.idl</dt></span></span> </dl> |



 

 
