---
description: La interfaz IWiaSegmentationFilter detecta subregiones de una secuencia de imágenes y crea elementos IWiaItem2 independientes para cada una de ellas.
ms.assetid: eb7f1284-ab98-4d86-8b30-7abd504cee12
title: Interfaz IWiaSegmentationFilter (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: b9c0bcdee5b40c37fb38b390f5085fe275f0f660
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908003"
---
# <a name="iwiasegmentationfilter-interface"></a><span data-ttu-id="f7187-103">Interfaz IWiaSegmentationFilter</span><span class="sxs-lookup"><span data-stu-id="f7187-103">IWiaSegmentationFilter interface</span></span>

<span data-ttu-id="f7187-104">La interfaz **IWiaSegmentationFilter** detecta subregiones de una secuencia de imágenes y crea elementos [**IWiaItem2**](-wia-iwiaitem2.md) independientes para cada una de ellas.</span><span class="sxs-lookup"><span data-stu-id="f7187-104">The **IWiaSegmentationFilter** interface detects sub-regions of an image stream and makes separate [**IWiaItem2**](-wia-iwiaitem2.md) items for each.</span></span>

## <a name="members"></a><span data-ttu-id="f7187-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="f7187-105">Members</span></span>

<span data-ttu-id="f7187-106">La interfaz **IWiaSegmentationFilter** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f7187-106">The **IWiaSegmentationFilter** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f7187-107">**IWiaSegmentationFilter** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f7187-107">**IWiaSegmentationFilter** also has these types of members:</span></span>

-   [<span data-ttu-id="f7187-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="f7187-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f7187-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="f7187-109">Methods</span></span>

<span data-ttu-id="f7187-110">La interfaz **IWiaSegmentationFilter** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="f7187-110">The **IWiaSegmentationFilter** interface has these methods.</span></span>



| <span data-ttu-id="f7187-111">Método</span><span class="sxs-lookup"><span data-stu-id="f7187-111">Method</span></span>                                                             | <span data-ttu-id="f7187-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7187-112">Description</span></span>                                                                                                                                              |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7187-113">**DetectRegions**</span><span class="sxs-lookup"><span data-stu-id="f7187-113">**DetectRegions**</span></span>](-wia-iwiasegmentationfilter-detectregions.md) | <span data-ttu-id="f7187-114">Determina las subregiones de una imagen que se distribuyen en la placa de plano, de modo que cada una de las subregiones pueda adquirirse en un elemento de imagen independiente.</span><span class="sxs-lookup"><span data-stu-id="f7187-114">Determines the sub-regions of an image laid out on the flatbed platen so that each of sub-region can be acquired into a separate image item.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="f7187-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f7187-115">Remarks</span></span>

<span data-ttu-id="f7187-116">Una aplicación debe usar [**IWiaItem2:: getExtension**](-wia-iwiaitem2-getextension.md) para crear una nueva instancia del filtro de segmentación.</span><span class="sxs-lookup"><span data-stu-id="f7187-116">An application should use [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) to create a new instance of the segmentation filter.</span></span> <span data-ttu-id="f7187-117">Una aplicación normalmente llama a esta función antes de mostrar su ventana de vista previa.</span><span class="sxs-lookup"><span data-stu-id="f7187-117">An application typically calls this function before displaying its preview window.</span></span>

<span data-ttu-id="f7187-118">Al implementar este filtro, use [**IWiaItem2:: CreateChildItem**](-wia-iwiaitem2-createchilditem.md) para crear los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="f7187-118">When implementing this filter, use [**IWiaItem2::CreateChildItem**](-wia-iwiaitem2-createchilditem.md) to create the child items.</span></span> <span data-ttu-id="f7187-119">La aplicación debe pasar **\_ \_ \_ los valores de la propiedad primaria Copy** al parámetro *ICreationFlags* para asegurarse de que las propiedades, como el formato de imagen y la resolución, son las mismas en el elemento secundario recién creado como en el elemento primario.</span><span class="sxs-lookup"><span data-stu-id="f7187-119">The application should pass **COPY\_PARENT\_PROPERTY\_VALUES** to the *ICreationFlags* parameter to ensure that properties such as image format and resolution is the same in the newly created child as in the parent item.</span></span>

<span data-ttu-id="f7187-120">Un filtro de segmentación debe admitir todos los formatos de imagen que admite el controlador con el que se usa.</span><span class="sxs-lookup"><span data-stu-id="f7187-120">A segmentation filter must support all the image formats that the driver it is used with supports.</span></span> <span data-ttu-id="f7187-121">El filtro proporcionado por Microsoft admite mapas de bits (BMP), formato de intercambio de gráficos (GIF), JPEG, gráficos de red portátiles (PNG) y Tagged Image File Format (TIFF).</span><span class="sxs-lookup"><span data-stu-id="f7187-121">The Microsoft provided filter supports bitmap (BMP), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG), and Tagged Image File Format (TIFF).</span></span>

<span data-ttu-id="f7187-122">El filtro de segmentación solo se debe usar en elementos de película y escáner plano.</span><span class="sxs-lookup"><span data-stu-id="f7187-122">The segmentation filter should be used only on film and flatbed scanner items.</span></span> <span data-ttu-id="f7187-123">En el análisis de películas, un escáner suele tener fotogramas fijos, en cuyo caso el controlador creó los elementos secundarios y la aplicación no debe invocar el filtro de segmentación.</span><span class="sxs-lookup"><span data-stu-id="f7187-123">For film scanning, a scanner often comes with fixed frames in which case the driver created the child items and the application should not invoke the segmentation filter.</span></span>

<span data-ttu-id="f7187-124">La interfaz **IWiaSegmentationFilter** , al igual que todas las interfaces del modelo de objetos componentes (com), hereda los métodos de interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f7187-124">The **IWiaSegmentationFilter** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="f7187-125">Métodos IUnknown</span><span class="sxs-lookup"><span data-stu-id="f7187-125">IUnknown Methods</span></span>                                        | <span data-ttu-id="f7187-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7187-126">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="f7187-127">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="f7187-127">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="f7187-128">Devuelve punteros a las interfaces compatibles.</span><span class="sxs-lookup"><span data-stu-id="f7187-128">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="f7187-129">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="f7187-129">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="f7187-130">Incrementa el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="f7187-130">Increments reference count.</span></span>               |
| [<span data-ttu-id="f7187-131">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="f7187-131">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="f7187-132">Reduce el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="f7187-132">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="f7187-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7187-133">Requirements</span></span>



| <span data-ttu-id="f7187-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7187-134">Requirement</span></span> | <span data-ttu-id="f7187-135">Value</span><span class="sxs-lookup"><span data-stu-id="f7187-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f7187-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7187-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f7187-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f7187-137">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f7187-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7187-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f7187-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f7187-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f7187-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f7187-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7187-141"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7187-141"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="f7187-142">IDL</span><span class="sxs-lookup"><span data-stu-id="f7187-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f7187-143"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f7187-143"><dt>Wia.idl</dt></span></span> </dl> |



 

 
