---
description: 'Invoca el filtro de segmentación de controladores y pasa al filtro la imagen sin filtrar almacenada en memoria caché por el método IWiaPreview:: GetNewPreview.'
ms.assetid: 4ae817b5-7091-432e-b004-0e53ae14fdb2
title: IWiaPreview::D método etectRegions (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 40665d2aae6e1e2dffa4356540afb05d45050492
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275462"
---
# <a name="iwiapreviewdetectregions-method"></a><span data-ttu-id="8a747-103">IWiaPreview::D método etectRegions</span><span class="sxs-lookup"><span data-stu-id="8a747-103">IWiaPreview::DetectRegions method</span></span>

<span data-ttu-id="8a747-104">Invoca el filtro de segmentación de controladores y pasa al filtro la imagen sin filtrar almacenada en memoria caché por el método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="8a747-104">Invokes the driver segmentation filter and passes the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method to the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a747-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a747-105">Syntax</span></span>


```C++
HRESULT DetectRegions(
  [in] LONG lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8a747-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a747-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a747-107">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a747-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a747-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="8a747-108">Type: **LONG**</span></span>

<span data-ttu-id="8a747-109">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="8a747-109">Not used.</span></span> <span data-ttu-id="8a747-110">Se establece en cero (0).</span><span class="sxs-lookup"><span data-stu-id="8a747-110">Set to zero (0).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a747-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a747-111">Return value</span></span>

<span data-ttu-id="8a747-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8a747-112">Type: **HRESULT**</span></span>

<span data-ttu-id="8a747-113">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="8a747-113">This method can return one of these values.</span></span>



| <span data-ttu-id="8a747-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8a747-114">Return code</span></span>                                                                               | <span data-ttu-id="8a747-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a747-115">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="8a747-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8a747-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="8a747-117">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8a747-117">The operation is successful.</span></span><br/>              |
| <dl> <span data-ttu-id="8a747-118"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="8a747-118"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="8a747-119">El controlador no admite la segmentación.</span><span class="sxs-lookup"><span data-stu-id="8a747-119">The driver does not support segmentation.</span></span><br/> |
| <dl> <span data-ttu-id="8a747-120"><dt>**otherwise**</dt></span><span class="sxs-lookup"><span data-stu-id="8a747-120"><dt>**otherwise**</dt></span></span> </dl>  | <span data-ttu-id="8a747-121">Un código de error COM estándar.</span><span class="sxs-lookup"><span data-stu-id="8a747-121">A standard COM error code.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="8a747-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a747-122">Remarks</span></span>

<span data-ttu-id="8a747-123">Una aplicación debe llamar a [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) antes de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="8a747-123">An application must call [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) before it calls this function.</span></span>

<span data-ttu-id="8a747-124">Cuando el componente de vista previa de la adquisición de imágenes de Windows (WIA) 2,0 llama a **IWiaPreview::D etectregions**, invoca el filtro de segmentación de controladores y pasa la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) que se pasó previamente a [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span><span class="sxs-lookup"><span data-stu-id="8a747-124">When the Windows Image Acquisition (WIA) 2.0 Preview Component calls **IWiaPreview::DetectRegions**, it invokes the driver segmentation filter and passes the [**IWiaItem2**](-wia-iwiaitem2.md) interface that was previously passed to [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span> <span data-ttu-id="8a747-125">También pasa la imagen almacenada en caché internamente al filtro.</span><span class="sxs-lookup"><span data-stu-id="8a747-125">It also passes the internally cached image to the filter.</span></span> <span data-ttu-id="8a747-126">El filtro segmentación utiliza la imagen almacenada en caché para crear las extensiones secundarias.</span><span class="sxs-lookup"><span data-stu-id="8a747-126">The segmentation filter uses the cached image to create the child extents.</span></span>

<span data-ttu-id="8a747-127">Si una aplicación cambia cualquier propiedad de la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) después de llamar a [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md), se deben restaurar las propiedades originales antes de que la aplicación llame a **IWiaPreview::D etectregions**.</span><span class="sxs-lookup"><span data-stu-id="8a747-127">If an application changes any properties of the [**IWiaItem2**](-wia-iwiaitem2.md) interface after it calls [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md), then the original properties must be restored before the application calls **IWiaPreview::DetectRegions**.</span></span> <span data-ttu-id="8a747-128">Use [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) y [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream) para restaurar las propiedades originales.</span><span class="sxs-lookup"><span data-stu-id="8a747-128">Use [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) and [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream) to restore the original properties.</span></span>

<span data-ttu-id="8a747-129">**IWiaPreview::D etectregions** se usa para determinar las "subregiones" de la imagen almacenada en caché.</span><span class="sxs-lookup"><span data-stu-id="8a747-129">**IWiaPreview::DetectRegions** is used to determine the "sub-regions" of the cached image.</span></span> <span data-ttu-id="8a747-130">Para cada subregión detectada, se crea un nuevo elemento secundario de WIA 2,0 en la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="8a747-130">For each sub-region detected, a new child WIA 2.0 item is created under the [**IWiaItem2**](-wia-iwiaitem2.md) interface.</span></span> <span data-ttu-id="8a747-131">Para cada elemento secundario, el filtro de segmentación debe establecer los valores de las siguientes propiedades de WIA 2,0: direcciones IP de WIA, las IP de WIA, XEXTENT y las IP de WIA \_ \_ \_ \_ \_ \_ \_ \_ YEXTENT.</span><span class="sxs-lookup"><span data-stu-id="8a747-131">For each child item, the segmentation filter must set the values for the following WIA 2.0 properties: WIA\_IPS\_XPOS, WIA\_IPS\_YPOS, WIA\_IPS\_XEXTENT, and WIA\_IPS\_YEXTENT.</span></span> <span data-ttu-id="8a747-132">Un filtro más avanzado establece otras propiedades de WIA 2,0, como la desfragmentación de las direcciones \_ IP \_ de WIA \_ X y WIA, \_ \_ dessesgado \_ y, si el controlador admite la anulación del sesgo.</span><span class="sxs-lookup"><span data-stu-id="8a747-132">A more advanced filter sets other WIA 2.0 properties, such as WIA\_IPS\_DESKEW\_X and WIA\_IPS\_DESKEW\_Y, if the driver supports de-skewing.</span></span> <span data-ttu-id="8a747-133">Las \_ propiedades WIA IP \_ XPOS, WIA \_ IP \_ YPOS, WIA \_ IP \_ XEXTENT y WIA \_ IPS \_ YEXTENT representan el rectángulo delimitador del área que se va a examinar.</span><span class="sxs-lookup"><span data-stu-id="8a747-133">The WIA\_IPS\_XPOS, WIA\_IPS\_YPOS, WIA\_IPS\_XEXTENT, and WIA\_IPS\_YEXTENT properties represent the bounding rectangle of the area to scan.</span></span>

<span data-ttu-id="8a747-134">Es posible que el controlador no admita la segmentación.</span><span class="sxs-lookup"><span data-stu-id="8a747-134">The driver might not support segmentation.</span></span> <span data-ttu-id="8a747-135">Antes de llamar a **IWiaPreview::D etectregions**, una aplicación comprueba normalmente si el controlador admite la \_ propiedad de segmentación de IP de WIA \_ .</span><span class="sxs-lookup"><span data-stu-id="8a747-135">Before calling **IWiaPreview::DetectRegions**, an application typically checks whether the driver supports the WIA\_IPS\_SEGMENTATION property.</span></span> <span data-ttu-id="8a747-136">Si la propiedad no está implementada, no se admite la segmentación y **IWiaPreview::D etectregions** produce un error y devuelve e \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="8a747-136">If the property is not implemented, segmentation is not supported, and **IWiaPreview::DetectRegions** fails and returns E\_NOTIMPL.</span></span>

<span data-ttu-id="8a747-137">La aplicación debe limpiar los elementos secundarios que se crean mediante una llamada a **IWiaPreview::D etectregions**.</span><span class="sxs-lookup"><span data-stu-id="8a747-137">The application must clean up the child items that are created by calling **IWiaPreview::DetectRegions**.</span></span> <span data-ttu-id="8a747-138">Por ejemplo, si una aplicación realiza una llamada adicional a **IWiaPreview::D etectregions** en el mismo elemento, debe limpiar los elementos secundarios anteriores.</span><span class="sxs-lookup"><span data-stu-id="8a747-138">For example, if an application makes an additional call to **IWiaPreview::DetectRegions** on the same item, it must clean up the previous child items.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a747-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a747-139">Requirements</span></span>



| <span data-ttu-id="8a747-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a747-140">Requirement</span></span> | <span data-ttu-id="8a747-141">Value</span><span class="sxs-lookup"><span data-stu-id="8a747-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8a747-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a747-142">Minimum supported client</span></span><br/> | <span data-ttu-id="8a747-143">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8a747-143">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8a747-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a747-144">Minimum supported server</span></span><br/> | <span data-ttu-id="8a747-145">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8a747-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8a747-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a747-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a747-147"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a747-147"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a747-148">IDL</span><span class="sxs-lookup"><span data-stu-id="8a747-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8a747-149"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8a747-149"><dt>Wia.idl</dt></span></span> </dl> |



 

 




