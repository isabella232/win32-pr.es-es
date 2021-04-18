---
description: Almacena en caché internamente la imagen sin filtrar devuelta por el controlador.
ms.assetid: 09cb242d-d1d6-4130-8b49-0770940471d8
title: 'IWiaPreview:: GetNewPreview (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.GetNewPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: c3f1251e7ec1b98d43e616c1ff6f2b3b2aacd8b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715189"
---
# <a name="iwiapreviewgetnewpreview-method"></a><span data-ttu-id="65f7a-103">IWiaPreview:: GetNewPreview (método)</span><span class="sxs-lookup"><span data-stu-id="65f7a-103">IWiaPreview::GetNewPreview method</span></span>

<span data-ttu-id="65f7a-104">Almacena en caché internamente la imagen sin filtrar devuelta por el controlador.</span><span class="sxs-lookup"><span data-stu-id="65f7a-104">Caches internally the unfiltered image returned from the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="65f7a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65f7a-105">Syntax</span></span>


```C++
HRESULT GetNewPreview(
  [in] IWiaItem2            *pWiaItem2,
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="65f7a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65f7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65f7a-107">*pWiaItem2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="65f7a-107">*pWiaItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65f7a-108">Tipo: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="65f7a-108">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="65f7a-109">Especifica un puntero al elemento [_ *IWiaItem2* \*](-wia-iwiaitem2.md) para la imagen.</span><span class="sxs-lookup"><span data-stu-id="65f7a-109">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item for the image.</span></span>

</dd> <dt>

<span data-ttu-id="65f7a-110">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="65f7a-110">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65f7a-111">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="65f7a-111">Type: **LONG**</span></span>

<span data-ttu-id="65f7a-112">Actualmente no se usa.</span><span class="sxs-lookup"><span data-stu-id="65f7a-112">Currently unused.</span></span> <span data-ttu-id="65f7a-113">Debe establecerse como cero.</span><span class="sxs-lookup"><span data-stu-id="65f7a-113">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="65f7a-114">*pWiaTransferCallback* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="65f7a-114">*pWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65f7a-115">Tipo: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="65f7a-115">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="65f7a-116">Especifica un puntero a la interfaz [_ *IWiaTransferCallback* \*](-wia-iwiatransfercallback.md) de la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="65f7a-116">Specifies a pointer to the calling application's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65f7a-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65f7a-117">Return value</span></span>

<span data-ttu-id="65f7a-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="65f7a-118">Type: **HRESULT**</span></span>

<span data-ttu-id="65f7a-119">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="65f7a-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="65f7a-120">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="65f7a-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="65f7a-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65f7a-121">Remarks</span></span>

<span data-ttu-id="65f7a-122">Una aplicación debe llamar a **IWiaPreview:: GetNewPreview** antes de llamar a [**IWiaPreview::D etectregions**](-wia-iwiapreview-detectregions.md).</span><span class="sxs-lookup"><span data-stu-id="65f7a-122">An application must call **IWiaPreview::GetNewPreview** before it calls [**IWiaPreview::DetectRegions**](-wia-iwiapreview-detectregions.md).</span></span>

<span data-ttu-id="65f7a-123">**IWiaPreview:: GetNewPreview** establece la propiedad de [**\_ \_ vista previa de DPS de WIA**](-wia-wiaitempropscannerdevice.md) (y lo restablece antes de que se devuelva, a menos que se haya establecido antes).</span><span class="sxs-lookup"><span data-stu-id="65f7a-123">**IWiaPreview::GetNewPreview** sets the [**WIA\_DPS\_PREVIEW**](-wia-wiaitempropscannerdevice.md) property (and resets it before it returns, unless it was set before).</span></span> <span data-ttu-id="65f7a-124">Esto permite que el controlador y el hardware, así como el filtro de procesamiento de imágenes, sepan que el elemento es un examen de vista previa.</span><span class="sxs-lookup"><span data-stu-id="65f7a-124">This lets the driver and hardware, as well as the image processing filter, know that the item is a preview scan.</span></span>

<span data-ttu-id="65f7a-125">Internamente, el componente de vista previa de Windows Image Acquisition (WIA) 2,0 crea una instancia del filtro de procesamiento de imágenes del controlador mediante una llamada a [**getExtension**](-wia-iwiaitem2-getextension.md) en *pWiaItem2*.</span><span class="sxs-lookup"><span data-stu-id="65f7a-125">Internally, the Windows Image Acquisition (WIA) 2.0 preview component creates an instance of the driver's image processing filter by calling [**GetExtension**](-wia-iwiaitem2-getextension.md) on *pWiaItem2*.</span></span> <span data-ttu-id="65f7a-126">El componente de vista previa de WIA 2,0 lo hace cuando la aplicación llama a **IWiaPreview:: GetNewPreview**.</span><span class="sxs-lookup"><span data-stu-id="65f7a-126">The WIA 2.0 preview component does this when the application calls **IWiaPreview::GetNewPreview**.</span></span> <span data-ttu-id="65f7a-127">El componente de vista previa de WIA 2,0 también inicializa el filtro en **IWiaPreview:: GetNewPreview**.</span><span class="sxs-lookup"><span data-stu-id="65f7a-127">The WIA 2.0 preview component also initializes the filter in **IWiaPreview::GetNewPreview**.</span></span> <span data-ttu-id="65f7a-128">El componente de vista previa de WIA 2,0 utiliza la misma instancia de filtro durante una llamada a [**IWiaPreview:: UpdatePreview**](-wia-iwiapreview-updatepreview.md).</span><span class="sxs-lookup"><span data-stu-id="65f7a-128">The same filter instance is used by the WIA 2.0 preview component during a call to [**IWiaPreview::UpdatePreview**](-wia-iwiapreview-updatepreview.md).</span></span>

<span data-ttu-id="65f7a-129">Antes de llamar al componente de vista previa de WIA 2,0, una aplicación debe llamar a [**checkExtension**](-wia-iwiaitem2-checkextension.md) para asegurarse de que el controlador incluye un filtro de procesamiento de imágenes.</span><span class="sxs-lookup"><span data-stu-id="65f7a-129">Before calling into the WIA 2.0 preview component, an application should call [**CheckExtension**](-wia-iwiaitem2-checkextension.md) to make sure that the driver comes with an image processing filter.</span></span> <span data-ttu-id="65f7a-130">Debe llamar a **checkExtension** en el elemento que se pasaría a **IWiaPreview:: GetNewPreview**.</span><span class="sxs-lookup"><span data-stu-id="65f7a-130">It should call **CheckExtension** on the item that it would pass to **IWiaPreview::GetNewPreview**.</span></span> <span data-ttu-id="65f7a-131">No es útil proporcionar vistas previas activas sin un filtro de procesamiento de imágenes.</span><span class="sxs-lookup"><span data-stu-id="65f7a-131">It is useless to provide live previews without an image processing filter.</span></span> <span data-ttu-id="65f7a-132">Si una aplicación llama a **IWiaPreview:: GetNewPreview** para un controlador sin un filtro de procesamiento de imágenes, se producirá un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="65f7a-132">If an application calls **IWiaPreview::GetNewPreview** for a driver without an image processing filter, the call will fail.</span></span>

## <a name="examples"></a><span data-ttu-id="65f7a-133">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="65f7a-133">Examples</span></span>

<span data-ttu-id="65f7a-134">CheckImgFilter comprueba si el controlador tiene un filtro de procesamiento de imágenes.</span><span class="sxs-lookup"><span data-stu-id="65f7a-134">CheckImgFilter checks if the driver has an image processing filter.</span></span> <span data-ttu-id="65f7a-135">Antes de llamar al componente de vista previa, una aplicación debe asegurarse de que el controlador tiene un filtro de procesamiento de imágenes.</span><span class="sxs-lookup"><span data-stu-id="65f7a-135">Before calling into the preview component, an application should ensure that the driver has an image processing filter.</span></span>


```C++
HRESULT
CheckImgFilter(
   IN  IWiaItem2 *pWiaItem2,
   OUT BOOL      *pbHasImgFilter)
{
   HRESULT     hr = S_OK;

   if (!pWiaItem2 || !pbHasImgFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
     *pbHasImgFilter = FALSE;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_IMAGEPROC_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->CheckExtension(0,
                                        bstrFilterString,
                                        IID_IWiaSegmentationFilter,
                                        pbHasImgFilter);

         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   return hr;

}
```



<span data-ttu-id="65f7a-136">DownloadPreviewImage descarga los datos de imagen del escáner llamando al método **IWiaPreview:: GetNewPreview** del componente de vista previa.</span><span class="sxs-lookup"><span data-stu-id="65f7a-136">DownloadPreviewImage downloads image data from the scanner by calling the preview component's **IWiaPreview::GetNewPreview** method.</span></span> <span data-ttu-id="65f7a-137">A continuación, llama a DetectSubregions si el usuario de la aplicación desea invocar el filtro de segmentación, que crea un elemento secundario en pWiaItem2 para cada región que detecta.</span><span class="sxs-lookup"><span data-stu-id="65f7a-137">It then calls DetectSubregions if the application user wants to invoke the segmentation filter, which creates a child item under pWiaItem2 for each region it detects.</span></span> <span data-ttu-id="65f7a-138">Consulte [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) para el método DetectSubregions que se usa en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="65f7a-138">See [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) for the DetectSubregions method used in this example.</span></span>

<span data-ttu-id="65f7a-139">En este ejemplo, el usuario de la aplicación establece `m_bUseSegmentationFilter` una casilla.</span><span class="sxs-lookup"><span data-stu-id="65f7a-139">In this example, the application user sets `m_bUseSegmentationFilter` by clicking a check box.</span></span> <span data-ttu-id="65f7a-140">Si la aplicación lo admite, primero debe comprobar que el controlador tiene un filtro de segmentación mediante una llamada a [**checkExtension**](-wia-iwiaitem2-checkextension.md).</span><span class="sxs-lookup"><span data-stu-id="65f7a-140">If the application supports this, it should first check that the driver has a segmentation filter by calling [**CheckExtension**](-wia-iwiaitem2-checkextension.md).</span></span> <span data-ttu-id="65f7a-141">Vea **IWiaPreview:: GetNewPreview** para obtener el ejemplo del método CheckImgFilter que muestra cómo se puede hacer esto.</span><span class="sxs-lookup"><span data-stu-id="65f7a-141">See **IWiaPreview::GetNewPreview** for the CheckImgFilter method example that shows how this can be done.</span></span>


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
         // The constructor of AppWiaTransferCallback sets the reference count to 1.
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
         // Do not create an instance of preview component if the driver does
         // not come with an image processing filter.
         // You can use segmentation filter, however, if the driver
         // comes with one (omitted here).
      }
   }

   return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="65f7a-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65f7a-142">Requirements</span></span>



| <span data-ttu-id="65f7a-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="65f7a-143">Requirement</span></span> | <span data-ttu-id="65f7a-144">Value</span><span class="sxs-lookup"><span data-stu-id="65f7a-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="65f7a-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65f7a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="65f7a-146">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="65f7a-146">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="65f7a-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65f7a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="65f7a-148">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="65f7a-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="65f7a-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65f7a-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="65f7a-150"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="65f7a-150"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="65f7a-151">IDL</span><span class="sxs-lookup"><span data-stu-id="65f7a-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="65f7a-152"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="65f7a-152"><dt>Wia.idl</dt></span></span> </dl> |



 

 




