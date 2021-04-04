---
description: Determina las subregiones de una imagen que se distribuyen en la placa de plano, de modo que cada una de las subregiones pueda adquirirse en un elemento de imagen independiente.
ms.assetid: 899d61f0-2dd8-4a68-827e-89e85ebb5143
title: IWiaSegmentationFilter::D método etectRegions (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 94fe2f5076e9ff7cc0de0f7c916f6edacf2d03fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154395"
---
# <a name="iwiasegmentationfilterdetectregions-method"></a><span data-ttu-id="71916-103">IWiaSegmentationFilter::D método etectRegions</span><span class="sxs-lookup"><span data-stu-id="71916-103">IWiaSegmentationFilter::DetectRegions method</span></span>

<span data-ttu-id="71916-104">Determina las subregiones de una imagen que se distribuyen en la placa de plano, de modo que cada una de las subregiones pueda adquirirse en un elemento de imagen independiente.</span><span class="sxs-lookup"><span data-stu-id="71916-104">Determines the sub-regions of an image laid out on the flatbed platen so that each of sub-region can be acquired into a separate image item.</span></span>

## <a name="syntax"></a><span data-ttu-id="71916-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71916-105">Syntax</span></span>


```C++
HRESULT DetectRegions(
  [in] LONG      lFlags,
  [in] IStream   *pInputStream,
  [in] IWiaItem2 *pWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="71916-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71916-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71916-107">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="71916-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71916-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="71916-108">Type: **LONG**</span></span>

<span data-ttu-id="71916-109">Actualmente no se usa.</span><span class="sxs-lookup"><span data-stu-id="71916-109">Currently unused.</span></span> <span data-ttu-id="71916-110">Debe establecerse como cero.</span><span class="sxs-lookup"><span data-stu-id="71916-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="71916-111">*pInputStream* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="71916-111">*pInputStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71916-112">Tipo: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="71916-112">Type: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="71916-113">Especifica un puntero a la imagen de vista previa de [IStream](/windows/win32/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="71916-113">Specifies a pointer to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) preview image.</span></span>

</dd> <dt>

<span data-ttu-id="71916-114">_pWiaItem2 \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="71916-114">_pWiaItem2\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71916-115">Tipo: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="71916-115">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="71916-116">Especifica un puntero al elemento [_ *IWiaItem2* \*](-wia-iwiaitem2.md) para el que se adquirió *pInputStream* .</span><span class="sxs-lookup"><span data-stu-id="71916-116">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item for which *pInputStream* was acquired.</span></span> <span data-ttu-id="71916-117">El filtro segmentación crea elementos secundarios para este elemento.</span><span class="sxs-lookup"><span data-stu-id="71916-117">The segmentation filter creates child items for this item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71916-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71916-118">Return value</span></span>

<span data-ttu-id="71916-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="71916-119">Type: **HRESULT**</span></span>

<span data-ttu-id="71916-120">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="71916-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="71916-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="71916-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="71916-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71916-122">Remarks</span></span>

<span data-ttu-id="71916-123">Este método determina las subregiones de la imagen representada por pInputStream.</span><span class="sxs-lookup"><span data-stu-id="71916-123">This method determines the sub-regions of the image represented by pInputStream.</span></span> <span data-ttu-id="71916-124">Para cada subregión detectada, se crea un elemento secundario para el elemento [**IWiaItem2**](-wia-iwiaitem2.md) especificado en el parámetro *pWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="71916-124">For each sub-region that it detects, it creates a child item for the [**IWiaItem2**](-wia-iwiaitem2.md) item specified in the *pWiaItem2* parameter.</span></span> <span data-ttu-id="71916-125">Para cada elemento secundario, el filtro de segmentación debe establecer valores para el rectángulo delimitador del área que se va a examinar, mediante las siguientes [**constantes de propiedades de elemento WIA de escáner**](-wia-wiaitempropscanneritem.md).</span><span class="sxs-lookup"><span data-stu-id="71916-125">For each child item, the segmentation filter must set values for the bounding rectangle of the area to scan, using the following [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md).</span></span>

-   [<span data-ttu-id="71916-126">**IP de WIA ( \_ \_ XPOS)**</span><span class="sxs-lookup"><span data-stu-id="71916-126">**WIA\_IPS\_XPOS**</span></span>](-wia-wiaitempropscanneritem.md)
-   [<span data-ttu-id="71916-127">**WIA \_ IP \_ YPOS**</span><span class="sxs-lookup"><span data-stu-id="71916-127">**WIA\_IPS\_YPOS**</span></span>](-wia-wiaitempropscanneritem.md)
-   [<span data-ttu-id="71916-128">**\_XEXTENT de IP WIA \_**</span><span class="sxs-lookup"><span data-stu-id="71916-128">**WIA\_IPS\_XEXTENT**</span></span>](-wia-wiaitempropscanneritem.md)
-   [<span data-ttu-id="71916-129">**\_YEXTENT de IP WIA \_**</span><span class="sxs-lookup"><span data-stu-id="71916-129">**WIA\_IPS\_YEXTENT**</span></span>](-wia-wiaitempropscanneritem.md)

<span data-ttu-id="71916-130">Un filtro más avanzado también puede requerir otras [**constantes de propiedad del elemento WIA del escáner**](-wia-wiaitempropscanneritem.md) , como la desfragmentación de las direcciones **IP de WIA \_ \_ \_ X** y **WIA, \_ \_ dessesgado \_ y**, si el controlador admite la anulación del sesgo.</span><span class="sxs-lookup"><span data-stu-id="71916-130">A more advanced filter may also require other [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md) such as **WIA\_IPS\_DESKEW\_X** and **WIA\_IPS\_DESKEW\_Y**, if the driver supports de-skewing.</span></span>

<span data-ttu-id="71916-131">Si la aplicación llama a **IWiaSegmentationFilter::D etectregions** más de una vez, la aplicación debe eliminar primero los elementos secundarios creados por la última llamada a **IWiaSegmentationFilter::D etectregions**.</span><span class="sxs-lookup"><span data-stu-id="71916-131">If the application calls **IWiaSegmentationFilter::DetectRegions** more than once, the application must first delete the child items created by the last call to **IWiaSegmentationFilter::DetectRegions**.</span></span>

<span data-ttu-id="71916-132">Si una aplicación cambia cualquier propiedad en *pWiaItem2*, entre la adquisición de la imagen en *pInputStream* y su llamada a **IWiaSegmentationFilter::D etectregions**, se deben restaurar las propiedades originales (es decir, las propiedades que tenía el elemento cuando se adquirió la secuencia).</span><span class="sxs-lookup"><span data-stu-id="71916-132">If an application changes any properties into *pWiaItem2*, between acquiring the image into *pInputStream* and its call to **IWiaSegmentationFilter::DetectRegions**, the original properties (that is, the properties the item had when the stream was acquired) must be restored.</span></span> <span data-ttu-id="71916-133">Esto puede realizarse mediante [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) y [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream).</span><span class="sxs-lookup"><span data-stu-id="71916-133">This can be done by [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) and [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream).</span></span>

<span data-ttu-id="71916-134">La aplicación debe restablecer la [IStream](/windows/win32/api/objidl/nn-objidl-istream) si su llamada pasa el mismo flujo al filtro de segmentación más de una vez.</span><span class="sxs-lookup"><span data-stu-id="71916-134">The application must reset the [IStream](/windows/win32/api/objidl/nn-objidl-istream) if its call passes the same stream into the segmentation filter more than once.</span></span> <span data-ttu-id="71916-135">La aplicación también debe restablecer la secuencia después de la descarga inicial y antes de llamar a **IWiaSegmentationFilter::D etectregions**.</span><span class="sxs-lookup"><span data-stu-id="71916-135">The application must also reset the stream after the initial download and before calling **IWiaSegmentationFilter::DetectRegions**.</span></span>

## <a name="examples"></a><span data-ttu-id="71916-136">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="71916-136">Examples</span></span>

<span data-ttu-id="71916-137">La segmentación realiza la detección de regiones en la secuencia ( `pImageStream` ) que se pasa a DetectSubregions.</span><span class="sxs-lookup"><span data-stu-id="71916-137">The segmentation performs region detection on the stream (`pImageStream`) passed into DetectSubregions.</span></span> <span data-ttu-id="71916-138">Vea el método [**getExtension**](-wia-iwiaitem2-getextension.md) para CreateSegmentationFilter que se usa en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="71916-138">See the [**GetExtension**](-wia-iwiaitem2-getextension.md) for CreateSegmentationFilter method used in this example.</span></span>


```C++
HRESULT
DetectSubregions(
   IN IStream   *pImageStream,
   IN IWiaItem2 *pWiaItem2)
{
   HRESULT                 hr                  = S_OK;
   IWiaSegmentationFilter* pSegmentationFilter = NULL;

   if (!pWiaItem2 || !pImageStream)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      hr = CreateSegmentationFilter(pWiaItem2, &pSegmentationFilter);
   }

   if (SUCCEEDED(hr))
   {
      hr = pSegmentationFilter->DetectRegions(0,pImageStream, pWiaItem2); 
   }

   if (pSegmentationFilter)
   {
      pSegmentationFilter->Release();
      pSegmentationFilter = NULL;
   }

   return hr;
}
```



<span data-ttu-id="71916-139">DownloadPreviewImage descarga los datos de imagen del escáner llamando al método [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) del componente de vista previa.</span><span class="sxs-lookup"><span data-stu-id="71916-139">DownloadPreviewImage downloads image data from the scanner by calling the preview component's [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="71916-140">A continuación, llama a DetectSubregions si el usuario de la aplicación desea invocar el filtro de segmentación, que crea un elemento secundario en pWiaItem2 para cada región que detecta.</span><span class="sxs-lookup"><span data-stu-id="71916-140">It then calls DetectSubregions if the application user wants to invoke the segmentation filter, which creates a child item under pWiaItem2 for each region it detects.</span></span> <span data-ttu-id="71916-141">Vea **IWiaSegmentationFilter::D etectregions** para el método DetectSubregions que se usa en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="71916-141">See **IWiaSegmentationFilter::DetectRegions** for the DetectSubregions method used in this example.</span></span>

<span data-ttu-id="71916-142">En este ejemplo, el usuario de la aplicación establece `m_bUseSegmentationFilter` una casilla.</span><span class="sxs-lookup"><span data-stu-id="71916-142">In this example, the application user sets `m_bUseSegmentationFilter` by clicking a check box.</span></span> <span data-ttu-id="71916-143">Si la aplicación lo admite, primero debe comprobar que el controlador tiene un filtro de segmentación mediante una llamada a [**checkExtension**](-wia-iwiaitem2-checkextension.md).</span><span class="sxs-lookup"><span data-stu-id="71916-143">If the application supports this, it should first check that the driver has a segmentation filter by calling [**CheckExtension**](-wia-iwiaitem2-checkextension.md).</span></span> <span data-ttu-id="71916-144">Consulte [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) para ver el ejemplo de método CheckImgFilter que muestra cómo se puede hacer esto.</span><span class="sxs-lookup"><span data-stu-id="71916-144">See [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) for the CheckImgFilter method example that shows how this can be done.</span></span>


```C++
HRESULT
DownloadPreviewImage(
   IN IWiaItem2 *pWiaFlatbedItem2)
{
   HRESULT hr              = S_OK;
   BOOL    bHasImgFilter   = FALSE;

   IWiaTransferCallback *pAppWiaTransferCallback = NULL;

   hr = CheckImgFilter(pWiaFlatbedItem2, &bHasImgFilter)

   if (SUCCEEDED(hr))
   {
      if (bHasImgFilter)
      {
         IWiaPreview *pWiaPreview = NULL;

         // In this example, the AppWiaTransferCallback class implements 
         // the IWiaTransferCallback interface.  
         // The constructor of AppWiaTransferCallback sets the reference count 
         // to 1.
         pAppWiaTransferCallback = new AppWiaTransferCallback();

         hr = pAppWiaTransferCallback ? S_OK : E_OUTOFMEMORY;

         if (SUCCEEDED(hr))
         {
            // Acquire image from scanner
            hr = m_pWiaPreview->GetNewPreview(pWiaFlatbedItem2,
                                              0,
                                              pAppWiaTransferCallback);    
         }

         //
         // Check the application UI for whether the user wants
         // to use the segmentation filter indicated by the value 
         // of m_bUseSegmentationFilter.
         //
         // m_FlatbedPreviewStream is the stream that
         // AppWiaTransferCallback::GetNextStream returned for the
         // flatbed item.
         // This stream is where the image data is stored after
         // the successful return of GetNewPreview.
         // The stream is passed into the segmentation filter
         // for region detection.
         if (SUCCEEDED(hr) && m_bUseSegmentationFilter)
         {
            DetectSubregions(m_FlatbedPreviewStream, pWiaFlatbedItem2);
         }

         if (pAppWiaTransferCallback)
         {
            // If the call to GetNewPreview was successful, the
            // preview component calls AddRef on the callback so
            // this call doesn't delete the object.

            pAppWiaTransferCallback->Release();
         }

      }
      else
      {
         // Do not create an instance of preview component if the driver 
         // does not come with an image-processing filter.
         // You can use a segmentation filter, however, if the driver
         // comes with one (omitted here).
      }
   }

   return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="71916-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71916-145">Requirements</span></span>



| <span data-ttu-id="71916-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="71916-146">Requirement</span></span> | <span data-ttu-id="71916-147">Value</span><span class="sxs-lookup"><span data-stu-id="71916-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="71916-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71916-148">Minimum supported client</span></span><br/> | <span data-ttu-id="71916-149">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="71916-149">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="71916-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71916-150">Minimum supported server</span></span><br/> | <span data-ttu-id="71916-151">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="71916-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="71916-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71916-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="71916-153"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="71916-153"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="71916-154">IDL</span><span class="sxs-lookup"><span data-stu-id="71916-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="71916-155"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="71916-155"><dt>Wia.idl</dt></span></span> </dl> |



 

 
