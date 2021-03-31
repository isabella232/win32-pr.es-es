---
description: 'Obtiene la imagen sin filtrar almacenada en memoria caché por el método IWiaPreview:: GetNewPreview.'
ms.assetid: 121b6866-cca1-4170-9bdf-225491f942f5
title: 'IWiaPreview:: UpdatePreview (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.UpdatePreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 4a5d469179f341f3bad5d2b9b5ed25a5715be694
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154396"
---
# <a name="iwiapreviewupdatepreview-method"></a><span data-ttu-id="a5f49-103">IWiaPreview:: UpdatePreview (método)</span><span class="sxs-lookup"><span data-stu-id="a5f49-103">IWiaPreview::UpdatePreview method</span></span>

<span data-ttu-id="a5f49-104">Obtiene la imagen sin filtrar almacenada en memoria caché por el método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f49-104">Gets the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5f49-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5f49-105">Syntax</span></span>


```C++
HRESULT UpdatePreview(
  [in] LONG      lOptions,
  [in] IWiaItem2 *pChildWiaItem
);
```



## <a name="parameters"></a><span data-ttu-id="a5f49-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5f49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5f49-107">*lOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a5f49-107">*lOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5f49-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="a5f49-108">Type: **LONG**</span></span>

<span data-ttu-id="a5f49-109">Especifica si la aplicación requiere que el componente de vista previa de WIA 2,0 pase una subregión de la imagen almacenada en caché o toda la imagen almacenada en caché al filtro de procesamiento de imágenes.</span><span class="sxs-lookup"><span data-stu-id="a5f49-109">Specifies whether the application requires the WIA 2.0 Preview Component to pass a sub-region of the cached image or the entire cached image to the image processing filter.</span></span>

<dt>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>

<span data-ttu-id="a5f49-110"><span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**WiaPreviewReturnOriginalImage**</span><span class="sxs-lookup"><span data-stu-id="a5f49-110"><span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**WiaPreviewReturnOriginalImage**</span></span>


</dt> <dd>

<span data-ttu-id="a5f49-111">Pase toda la imagen almacenada en caché al filtro de procesamiento de imágenes.</span><span class="sxs-lookup"><span data-stu-id="a5f49-111">Pass the entire cached image to the image processing filter.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a5f49-112">*pChildWiaItem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a5f49-112">*pChildWiaItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5f49-113">Tipo: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="a5f49-113">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="a5f49-114">Especifica un puntero al elemento [_ *IWiaItem2* \*](-wia-iwiaitem2.md) , que es un elemento secundario del elemento **IWiaItem2** especificado por el parámetro *pWiaItem2* del método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f49-114">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item, which is a child of the **IWiaItem2** item specified by the *pWiaItem2* parameter of the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="a5f49-115">O bien, si la aplicación requiere una vista previa de todo el plano, especifica un puntero al parámetro *pWiaItem2* del método **IWiaPreview:: GetNewPreview** .</span><span class="sxs-lookup"><span data-stu-id="a5f49-115">Or, if the application requires a preview of the whole flatbed, specifies a pointer to the *pWiaItem2* parameter of the **IWiaPreview::GetNewPreview** method.</span></span> <span data-ttu-id="a5f49-116">Cuando *pChildWiaItem* es un elemento secundario del parámetro *pWiaItem2* de **IWiaPreview:: GetNewPreview**, este elemento secundario se crea normalmente mediante el filtro de segmentación.</span><span class="sxs-lookup"><span data-stu-id="a5f49-116">When *pChildWiaItem* is a child of **IWiaPreview::GetNewPreview**'s *pWiaItem2* parameter, this child item is typically created by the segmentation filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5f49-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5f49-117">Return value</span></span>

<span data-ttu-id="a5f49-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a5f49-118">Type: **HRESULT**</span></span>

<span data-ttu-id="a5f49-119">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a5f49-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a5f49-120">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a5f49-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5f49-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5f49-121">Remarks</span></span>

<span data-ttu-id="a5f49-122">Este método pasa la imagen almacenada en caché sin filtrar a través del filtro de procesamiento de imágenes, que después escribe los datos filtrados en la secuencia proporcionada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a5f49-122">This method passes the cached, unfiltered image through the image processing filter, which then writes the filtered data to the application-provided stream.</span></span> <span data-ttu-id="a5f49-123">El componente de vista previa de WIA 2,0 recupera esta secuencia llamando al método [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) del filtro de procesamiento de imágenes, que luego llama a la implementación de **GetNextStream** de la devolución de llamada de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a5f49-123">The WIA 2.0 Preview Component retrieves this stream by calling the image processing filter's [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) method, which then calls the application callback's **GetNextStream** implementation.</span></span> <span data-ttu-id="a5f49-124">Antes de llamar a **IWiaPreview:: UpdatePreview**, una aplicación debe llamar primero a [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) para adquirir la imagen del escáner. de lo contrario, el método devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="a5f49-124">Before calling **IWiaPreview::UpdatePreview**, an application must first call [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) to acquire the image from the scanner; otherwise, the method returns an error.</span></span>

<span data-ttu-id="a5f49-125">El componente WIA 2,0 Preview almacena la imagen sin filtrar descargada del controlador.</span><span class="sxs-lookup"><span data-stu-id="a5f49-125">The WIA 2.0 Preview Component stores the unfiltered image downloaded from the driver.</span></span> <span data-ttu-id="a5f49-126">Es posible que el elemento de WIA 2,0 pasado a **IWiaPreview:: UpdatePreview** represente solo una pequeña región de la imagen descargada del controlador.</span><span class="sxs-lookup"><span data-stu-id="a5f49-126">It is possible that the WIA 2.0 item passed into **IWiaPreview::UpdatePreview** represents only a small region of the image downloaded from the driver.</span></span> <span data-ttu-id="a5f49-127">Si este es el caso, el componente de vista previa de WIA 2,0 descompone realmente esta región de la imagen almacenada en caché antes de pasarla al filtro de procesamiento de imágenes, que a su vez pasa los datos de la imagen filtrada de nuevo a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a5f49-127">If this is the case the WIA 2.0 Preview Component actually cuts out this region from the cached image before it passes it to the image processing filter, which in turn passes the filtered image data back to the application.</span></span>

<span data-ttu-id="a5f49-128">Para que una aplicación pase toda la imagen almacenada en caché al filtro de procesamiento de imágenes (que a su vez la pasa a la aplicación), debe establecer *lOptions* en **WiaPreviewReturnOriginalImage** al llamar a **IWiaPreview:: UpdatePreview**.</span><span class="sxs-lookup"><span data-stu-id="a5f49-128">For an application to pass the entire cached image to the image processing filter (which in turn passes it to the application), it must set the *lOptions* to **WiaPreviewReturnOriginalImage** when calling **IWiaPreview::UpdatePreview**.</span></span> <span data-ttu-id="a5f49-129">Al establecer *lOptions* en **WiaPreviewReturnOriginalImage**, la aplicación debe asegurarse de que la configuración de extensión ([**IP de WIA \_ IP \_ XEXTENT**](-wia-wiaitempropscanneritem.md) y **WIA \_ IP \_ YEXTENT**) del elemento pasado a **IWiaPreview:: UpdatePreview** coincide con la imagen almacenada en caché completa.</span><span class="sxs-lookup"><span data-stu-id="a5f49-129">When setting *lOptions* to **WiaPreviewReturnOriginalImage**, the application must ensure that the extent settings ([**WIA\_IPS\_XEXTENT**](-wia-wiaitempropscanneritem.md) and **WIA\_IPS\_YEXTENT**) of the item passed into **IWiaPreview::UpdatePreview** matches the full-cached image.</span></span> <span data-ttu-id="a5f49-130">El filtro de procesamiento de imágenes no necesita hacer nada diferente en este caso; simplemente filtra la imagen, en función de las propiedades de *pChildWiaItem* (normalmente, en este caso, *pChildWiaItem* es el mismo elemento que se pasó a [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md)).</span><span class="sxs-lookup"><span data-stu-id="a5f49-130">The image processing filter need not do anything different in this case; it simply filters the image, based on the properties of *pChildWiaItem* (typically in this case *pChildWiaItem* is the same item that was passed to [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md)).</span></span> <span data-ttu-id="a5f49-131">Se omiten las distintas subregiones y se filtra toda la imagen con la misma configuración.</span><span class="sxs-lookup"><span data-stu-id="a5f49-131">The different sub-regions are ignored and the whole image is filtered using the same settings.</span></span> <span data-ttu-id="a5f49-132">Hay un par de razones por las que una aplicación lo haría.</span><span class="sxs-lookup"><span data-stu-id="a5f49-132">There are a couple of reasons why an application would do this.</span></span>

1.  <span data-ttu-id="a5f49-133">Es posible que la aplicación no admita el cambio de la configuración (por ejemplo, el contraste de [**\_ IP \_**](-wia-wiaitempropscanneritem.md) de WIA y el contraste de las **\_ direcciones \_ IP de WIA**) individualmente para cada región detectada por el filtro de segmentación (o incluso puede que no desee usar el filtro de segmentación).</span><span class="sxs-lookup"><span data-stu-id="a5f49-133">The application may not support changing the settings (like [**WIA\_IPS\_BRIGHTNESS**](-wia-wiaitempropscanneritem.md) and **WIA\_IPS\_CONTRAST**) individually for each region that the segmentation filter detects (or it may not even want to use the segmentation filter).</span></span> <span data-ttu-id="a5f49-134">Es más fácil que la aplicación llame a **IWiaPreview:: UpdatePreview** con **WiaPreviewReturnOriginalImage** para que siempre reciba la imagen completa del componente de vista previa de WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="a5f49-134">It is easier for the application to call **IWiaPreview::UpdatePreview** with **WiaPreviewReturnOriginalImage** so that it always receives the full image from the WIA 2.0 Preview Component.</span></span>
2.  <span data-ttu-id="a5f49-135">El componente de vista previa de WIA 2,0 no admite el formato de imagen de la imagen de vista previa, en cuyo caso no puede realizar las acciones para cortar la región deseada.</span><span class="sxs-lookup"><span data-stu-id="a5f49-135">The WIA 2.0 Preview Component does not support the image format of the preview image, in which case it cannot perform the actions to cut out the desired region.</span></span> <span data-ttu-id="a5f49-136">La compatibilidad con el formato de imagen del componente de vista previa de WIA 2,0 está limitada a formatos para los que hay codificadores y descodificadores de Windows GDI+ 1,1.</span><span class="sxs-lookup"><span data-stu-id="a5f49-136">The WIA 2.0 Preview Component's image format support is limited to formats for which there are Windows GDI+ 1.1 encoders and decoders.</span></span> <span data-ttu-id="a5f49-137">Estos formatos son Bitmap (BMP) (un mapa de bits que incluye BITMAPFILEHEADER), formato de intercambio de gráficos (GIF), JPEG, Portable Network Graphics (PNG) y Tagged Image File Format (TIFF).</span><span class="sxs-lookup"><span data-stu-id="a5f49-137">These formats are bitmap (BMP) (a bitmap that includes the BITMAPFILEHEADER), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG), and Tagged Image File Format (TIFF).</span></span>

<span data-ttu-id="a5f49-138">Tenga en cuenta que si la aplicación pasa **WiaPreviewReturnOriginalImage** a **IWiaPreview:: UpdatePreview**, el componente de vista previa de WIA 2,0 puede admitir cualquier formato de imagen o píxel.</span><span class="sxs-lookup"><span data-stu-id="a5f49-138">Note that if the application passes **WiaPreviewReturnOriginalImage** into **IWiaPreview::UpdatePreview**, the WIA 2.0 Preview Component can support any image or pixel format.</span></span>

<span data-ttu-id="a5f49-139">**IWiaPreview:: UpdatePreview** establece la propiedad de [**\_ \_ vista previa de DPS de WIA**](-wia-wiaitempropscannerdevice.md) (y lo restablece antes de que se devuelva, a menos que se haya establecido antes).</span><span class="sxs-lookup"><span data-stu-id="a5f49-139">**IWiaPreview::UpdatePreview** sets the [**WIA\_DPS\_PREVIEW**](-wia-wiaitempropscannerdevice.md) property (and resets it before it returns, unless it was set before).</span></span> <span data-ttu-id="a5f49-140">Esto permite que el controlador (y el hardware) y el filtro de procesamiento de imágenes sepan que el elemento es un examen de vista previa.</span><span class="sxs-lookup"><span data-stu-id="a5f49-140">This lets the driver (and hardware) as well as the image processing filter, know that the item is a preview scan.</span></span>

<span data-ttu-id="a5f49-141">Una aplicación debe asegurarse de *que pChildWiaItem* tenga el mismo formato de imagen ([**\_ \_ formato de IPA de WIA**](-wia-wiaitempropcommonitem.md)) y la resolución (IP de [**WIA \_ \_ XRES**](-wia-wiaitempropscanneritem.md) y **WIA \_ IPS \_ YRES**) que tenía *pWiaItem* cuando se pasó a [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span><span class="sxs-lookup"><span data-stu-id="a5f49-141">An application must ensure that *pChildWiaItem* has the same image format ([**WIA\_IPA\_FORMAT**](-wia-wiaitempropcommonitem.md)) and resolution ([**WIA\_IPS\_XRES**](-wia-wiaitempropscanneritem.md) and **WIA\_IPS\_YRES**) as *pWiaItem* had when it was passed into [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span> <span data-ttu-id="a5f49-142">El formato del elemento secundario debe coincidir con el formato de la imagen almacenada en caché del componente WIA 2,0 Preview (el componente WIA 2,0 Preview no realiza ninguna conversión de imagen).</span><span class="sxs-lookup"><span data-stu-id="a5f49-142">The format of the child item must correspond to the format of the WIA 2.0 Preview Component's cached image (the WIA 2.0 Preview Component performs no image conversion).</span></span>

## <a name="examples"></a><span data-ttu-id="a5f49-143">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a5f49-143">Examples</span></span>

<span data-ttu-id="a5f49-144">Se debe llamar a UpdateRegion cada vez que un usuario cambia, por ejemplo, el brillo o el contraste del elemento secundario representado por `dwRegionNumber` .</span><span class="sxs-lookup"><span data-stu-id="a5f49-144">UpdateRegion should be called each time a user changes, for example, the brightness or contrast for the child item represented by `dwRegionNumber`.</span></span> <span data-ttu-id="a5f49-145">Este elemento secundario se ha creado anteriormente con el filtro de segmentación ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md).</span><span class="sxs-lookup"><span data-stu-id="a5f49-145">This child item has previously been created by the segmentation filter ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md).</span></span> <span data-ttu-id="a5f49-146">La imagen escrita en [IStream](/windows/win32/api/objidl/nn-objidl-istream) se devuelve mediante el método [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) de la interfaz de devolución de llamada de transferencia.</span><span class="sxs-lookup"><span data-stu-id="a5f49-146">The image written to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) is returned by the transfer callback interface's [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) method.</span></span> <span data-ttu-id="a5f49-147">El código de GetSubRegionItem se omite en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a5f49-147">The code for GetSubRegionItem is omitted in this example.</span></span>

<span data-ttu-id="a5f49-148">Después de llamar a esta función, una aplicación normalmente volvería a dibujar la región en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a5f49-148">After this function has been called, an application would typically redraw the region on the screen.</span></span>


```C++
HRESULT
UpdateRegion(
   IN  DWORD dwRegionNumber)
{
   IWiaItem2 *pSubRegion = GetSubRegionItem(dwRegionNumber);

   return m_pWiaPreview->UpdatePreview(0,pSubRegion);
}
```



## <a name="requirements"></a><span data-ttu-id="a5f49-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5f49-149">Requirements</span></span>



| <span data-ttu-id="a5f49-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5f49-150">Requirement</span></span> | <span data-ttu-id="a5f49-151">Value</span><span class="sxs-lookup"><span data-stu-id="a5f49-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a5f49-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5f49-152">Minimum supported client</span></span><br/> | <span data-ttu-id="a5f49-153">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a5f49-153">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a5f49-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5f49-154">Minimum supported server</span></span><br/> | <span data-ttu-id="a5f49-155">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a5f49-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a5f49-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5f49-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5f49-157"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5f49-157"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="a5f49-158">IDL</span><span class="sxs-lookup"><span data-stu-id="a5f49-158">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a5f49-159"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a5f49-159"><dt>Wia.idl</dt></span></span> </dl> |



 

 
