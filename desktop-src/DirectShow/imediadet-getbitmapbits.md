---
description: El método GetBitmapBits recupera un fotograma de vídeo en el tiempo medio especificado. El marco devuelto siempre tiene el formato RGB de 24 bits.
ms.assetid: b51df9d1-9c54-41bd-b0f8-ec290525deca
title: 'IMediaDet:: GetBitmapBits (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 95aea5281f77b32868e0f0856bc63063e4f08639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680964"
---
# <a name="imediadetgetbitmapbits-method"></a><span data-ttu-id="82ce1-104">IMediaDet:: GetBitmapBits (método)</span><span class="sxs-lookup"><span data-stu-id="82ce1-104">IMediaDet::GetBitmapBits method</span></span>

> [!Note]  
> <span data-ttu-id="82ce1-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="82ce1-105">\[Deprecated.</span></span> <span data-ttu-id="82ce1-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="82ce1-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="82ce1-107">El `GetBitmapBits` método recupera un fotograma de vídeo en el tiempo medio especificado.</span><span class="sxs-lookup"><span data-stu-id="82ce1-107">The `GetBitmapBits` method retrieves a video frame at the specified media time.</span></span> <span data-ttu-id="82ce1-108">El marco devuelto siempre tiene el formato RGB de 24 bits.</span><span class="sxs-lookup"><span data-stu-id="82ce1-108">The returned frame is always in 24-bit RGB format.</span></span>

## <a name="syntax"></a><span data-ttu-id="82ce1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82ce1-109">Syntax</span></span>


```C++
HRESULT GetBitmapBits(
   double StreamTime,
   long   *pBufferSize,
   char   *pBuffer,
   long   Width,
   long   Height
);
```



## <a name="parameters"></a><span data-ttu-id="82ce1-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82ce1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82ce1-111">*StreamTime*</span><span class="sxs-lookup"><span data-stu-id="82ce1-111">*StreamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="82ce1-112">Hora a la que se va a recuperar el fotograma de vídeo, en segundos.</span><span class="sxs-lookup"><span data-stu-id="82ce1-112">Time at which to retrieve the video frame, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="82ce1-113">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="82ce1-113">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="82ce1-114">Recibe el tamaño de búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="82ce1-114">Receives the required buffer size.</span></span> <span data-ttu-id="82ce1-115">Si *pBuffer* es **null**, la variable recibe el tamaño del búfer necesario para recuperar el marco.</span><span class="sxs-lookup"><span data-stu-id="82ce1-115">If *pBuffer* is **NULL**, the variable receives the size of the buffer needed to retrieve the frame.</span></span> <span data-ttu-id="82ce1-116">Si *pBuffer* no es **null**, se omite este parámetro.</span><span class="sxs-lookup"><span data-stu-id="82ce1-116">If *pBuffer* is not **NULL**, this parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="82ce1-117">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="82ce1-117">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="82ce1-118">Puntero a un búfer que recibe una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) seguido de los bits Dib.</span><span class="sxs-lookup"><span data-stu-id="82ce1-118">Pointer to a buffer that receives a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure followed by the DIB bits.</span></span>

</dd> <dt>

<span data-ttu-id="82ce1-119">*Width*</span><span class="sxs-lookup"><span data-stu-id="82ce1-119">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="82ce1-120">Ancho de la imagen de vídeo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="82ce1-120">Width of the video image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="82ce1-121">*Height*</span><span class="sxs-lookup"><span data-stu-id="82ce1-121">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="82ce1-122">Alto de la imagen de vídeo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="82ce1-122">Height of the video image, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82ce1-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82ce1-123">Return value</span></span>

<span data-ttu-id="82ce1-124">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="82ce1-124">Returns an **HRESULT** value.</span></span> <span data-ttu-id="82ce1-125">Entre los valores posibles figuran los siguientes:</span><span class="sxs-lookup"><span data-stu-id="82ce1-125">Possible values include the following:</span></span>



| <span data-ttu-id="82ce1-126">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="82ce1-126">Return code</span></span>                                                                                             | <span data-ttu-id="82ce1-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="82ce1-127">Description</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="82ce1-128"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="82ce1-128"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="82ce1-129">Correcto.</span><span class="sxs-lookup"><span data-stu-id="82ce1-129">Success.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="82ce1-130"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="82ce1-130"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="82ce1-131">No se pudo agregar el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) al gráfico.</span><span class="sxs-lookup"><span data-stu-id="82ce1-131">Could not add the [**Sample Grabber**](sample-grabber-filter.md) filter to the graph.</span></span><br/> |
| <dl> <span data-ttu-id="82ce1-132"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="82ce1-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>           | <span data-ttu-id="82ce1-133">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="82ce1-133">Insufficient memory.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="82ce1-134"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="82ce1-134"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="82ce1-135">Error de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="82ce1-135">**NULL** pointer error.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="82ce1-136"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="82ce1-136"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>            | <span data-ttu-id="82ce1-137">error inesperado.</span><span class="sxs-lookup"><span data-stu-id="82ce1-137">Unexpected error.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="82ce1-138"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="82ce1-138"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="82ce1-139">Tipo de medio no válido.</span><span class="sxs-lookup"><span data-stu-id="82ce1-139">Invalid media type.</span></span><br/>                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="82ce1-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82ce1-140">Remarks</span></span>

<span data-ttu-id="82ce1-141">Antes de llamar a este método, establezca el nombre de archivo y el flujo mediante una llamada a [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) y [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="82ce1-141">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="82ce1-142">Para determinar el tamaño del búfer necesario, llame a este método con *pBuffer* igual a **null**.</span><span class="sxs-lookup"><span data-stu-id="82ce1-142">To determine the size of the buffer that is required, call this method with *pBuffer* equal to **NULL**.</span></span> <span data-ttu-id="82ce1-143">El tamaño se devuelve en la variable a la que apunta *pBufferSize*.</span><span class="sxs-lookup"><span data-stu-id="82ce1-143">The size is returned in the variable pointed to by *pBufferSize*.</span></span> <span data-ttu-id="82ce1-144">A continuación, cree el búfer y llame de nuevo al método, con *pBuffer* igual a la dirección del búfer.</span><span class="sxs-lookup"><span data-stu-id="82ce1-144">Then create the buffer and call the method again, with *pBuffer* equal to the address of the buffer.</span></span> <span data-ttu-id="82ce1-145">Cuando el método devuelve, el búfer contiene una estructura **BITMAPINFOHEADER** seguida del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="82ce1-145">When the method returns, the buffer contains a **BITMAPINFOHEADER** structure followed by the bitmap.</span></span> <span data-ttu-id="82ce1-146">El mapa de bits se escala a las dimensiones especificadas en los parámetros *ancho* y *alto* .</span><span class="sxs-lookup"><span data-stu-id="82ce1-146">The bitmap is scaled to the dimensions specified in the *Width* and *Height* parameters.</span></span>

<span data-ttu-id="82ce1-147">Este método coloca el detector de medios en el modo de agarre de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="82ce1-147">This method puts the media detector into bitmap grab mode.</span></span> <span data-ttu-id="82ce1-148">Una vez que se ha llamado a este método, los distintos métodos de información de secuencia de **IMediaDet** no funcionan, a menos que cree una nueva instancia del detector de medios.</span><span class="sxs-lookup"><span data-stu-id="82ce1-148">Once this method has been called, the various stream information methods in **IMediaDet** do not work, unless you create a new instance of the media detector.</span></span>

> [!Note]  
> <span data-ttu-id="82ce1-149">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="82ce1-149">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="82ce1-150">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="82ce1-150">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="82ce1-151">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="82ce1-151">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="examples"></a><span data-ttu-id="82ce1-152">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="82ce1-152">Examples</span></span>

<span data-ttu-id="82ce1-153">En el código siguiente se usa el `GetBitmapBits` método para crear un mapa de bits independiente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="82ce1-153">The following code uses the `GetBitmapBits` method to create a device-independent bitmap.</span></span>


```C++
long size;
hr = pDet->GetBitmapBits(0, &size, 0, width, height);
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[size];
    if (!pBuffer)
        return E_OUTOFMEMORY;
    try {
        hr = pDet->GetBitmapBits(0, 0, pBuffer, width, height);
    }
    catch (...) {
        delete [] pBuffer;
        throw;
    }
    if (SUCCEEDED(hr))
    {
        BITMAPINFOHEADER *bmih = (BITMAPINFOHEADER*)pBuffer;
        HDC hdcDest = GetDC(0);
        
        // Find the address of the start of the image data.
        void *pData = pBuffer + sizeof(BITMAPINFOHEADER);
        
        // Note: In general a BITMAPINFOHEADER can include extra color
        // information at the end, so calculating the offset to the image
        // data is not generally correct. However, the IMediaDet interface
        // always returns an RGB-24 image with no extra color information.
        
        BITMAPINFO bmi;
        ZeroMemory(&bmi, sizeof(BITMAPINFO));
        CopyMemory(&(bmi.bmiHeader), bmih, sizeof(BITMAPINFOHEADER));
        HBITMAP hBitmap = CreateDIBitmap(hdcDest, bmih, CBM_INIT, 
            pData, &bmi, DIB_RGB_COLORS);
    }
    delete[] pBuffer;
}
```



## <a name="requirements"></a><span data-ttu-id="82ce1-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82ce1-154">Requirements</span></span>



| <span data-ttu-id="82ce1-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="82ce1-155">Requirement</span></span> | <span data-ttu-id="82ce1-156">Value</span><span class="sxs-lookup"><span data-stu-id="82ce1-156">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82ce1-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82ce1-157">Header</span></span><br/>  | <dl> <span data-ttu-id="82ce1-158"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="82ce1-158"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="82ce1-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="82ce1-159">Library</span></span><br/> | <dl> <span data-ttu-id="82ce1-160"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82ce1-160"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82ce1-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="82ce1-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82ce1-162">**Interfaz IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="82ce1-162">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="82ce1-163">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="82ce1-163">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




