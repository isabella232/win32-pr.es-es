---
description: El método SetSmartRecompressFormat especifica un formato de compresión de vídeo que se usará para la recompresión inteligente.
ms.assetid: 80c02215-6da2-4b3e-ab0d-004e49480fb9
title: 'IAMTimelineGroup:: SetSmartRecompressFormat (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9c8505f54d6ee9f6b2ec02216fd875fddbc619de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690788"
---
# <a name="iamtimelinegroupsetsmartrecompressformat-method"></a><span data-ttu-id="5ea96-103">IAMTimelineGroup:: SetSmartRecompressFormat (método)</span><span class="sxs-lookup"><span data-stu-id="5ea96-103">IAMTimelineGroup::SetSmartRecompressFormat method</span></span>

> [!Note]  
> <span data-ttu-id="5ea96-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="5ea96-104">\[Deprecated.</span></span> <span data-ttu-id="5ea96-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5ea96-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5ea96-106">El `SetSmartRecompressFormat` método especifica un formato de compresión de vídeo que se utilizará para la recompresión inteligente.</span><span class="sxs-lookup"><span data-stu-id="5ea96-106">The `SetSmartRecompressFormat` method specifies a video compression format to use for smart recompression.</span></span>

<span data-ttu-id="5ea96-107">La recompresión inteligente no es compatible con los grupos de audio.</span><span class="sxs-lookup"><span data-stu-id="5ea96-107">Smart recompression is not supported for audio groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ea96-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ea96-108">Syntax</span></span>


```C++
HRESULT SetSmartRecompressFormat(
   long *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="5ea96-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ea96-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ea96-110">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="5ea96-110">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="5ea96-111">Puntero a una estructura que describe el formato de compresión.</span><span class="sxs-lookup"><span data-stu-id="5ea96-111">Pointer to a structure describing the compression format.</span></span> <span data-ttu-id="5ea96-112">Actualmente, solo la estructura [**SCompFmt0**](scompfmt0.md) es válida.</span><span class="sxs-lookup"><span data-stu-id="5ea96-112">Currently, only the [**SCompFmt0**](scompfmt0.md) structure is valid.</span></span> <span data-ttu-id="5ea96-113">Debe convertir este parámetro en un puntero de tipo **Long**.</span><span class="sxs-lookup"><span data-stu-id="5ea96-113">You must cast this parameter to a pointer of type **long**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ea96-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ea96-114">Return value</span></span>

<span data-ttu-id="5ea96-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="5ea96-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5ea96-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5ea96-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ea96-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ea96-117">Remarks</span></span>

<span data-ttu-id="5ea96-118">Antes de llamar a este método, llame al método [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md) en el mismo grupo para especificar un formato sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="5ea96-118">Before calling this method, call the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method on the same group, to specify an uncompressed format.</span></span>

<span data-ttu-id="5ea96-119">Si el `SetSmartRecompressFormat` método se ejecuta correctamente, puede usar el motor de representación inteligente para generar un flujo de vídeo comprimido.</span><span class="sxs-lookup"><span data-stu-id="5ea96-119">If the `SetSmartRecompressFormat` method succeeds, you can use the Smart Render Engine to output a compressed video stream.</span></span> <span data-ttu-id="5ea96-120">El vídeo comprimido tendrá el ancho, el alto y la velocidad de fotogramas que se especificó en el parámetro *pFormat* .</span><span class="sxs-lookup"><span data-stu-id="5ea96-120">The compressed video will have the width, height, and frame rate that was specified in the *pFormat* parameter.</span></span> <span data-ttu-id="5ea96-121">Estos valores reemplazan a los que se proporcionan para el formato sin comprimir en el método **SetMediaType** .</span><span class="sxs-lookup"><span data-stu-id="5ea96-121">These values will override those given for the uncompressed format in the **SetMediaType** method.</span></span> <span data-ttu-id="5ea96-122">Sin embargo, para obtener las ventajas de la recompresión inteligente, los dos formatos deben coincidir.</span><span class="sxs-lookup"><span data-stu-id="5ea96-122">However, to get the benefits of smart recompression, the two formats should match.</span></span> <span data-ttu-id="5ea96-123">En otras palabras, los formatos comprimidos y sin comprimir deben tener el mismo alto, ancho y velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="5ea96-123">In other words, the compressed and uncompressed formats should have the same height, width, and frame rate.</span></span>

<span data-ttu-id="5ea96-124">Si el motor de representación inteligente no puede generar el formato comprimido, producirá una secuencia de vídeo sin comprimir en su lugar.</span><span class="sxs-lookup"><span data-stu-id="5ea96-124">If the Smart Render Engine is unable to produce the compressed format, it will produce an uncompressed video stream instead.</span></span> <span data-ttu-id="5ea96-125">Si esto ocurre, el motor de representación inteligente informa de un error de representación del compresor de los identificadores de DEX en \_ \_ \_ \_ el método [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) .</span><span class="sxs-lookup"><span data-stu-id="5ea96-125">If that occurs, the Smart Render Engine reports a DEX\_IDS\_CANT\_FIND\_COMPRESSOR rendering error during the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method.</span></span> <span data-ttu-id="5ea96-126">La aplicación puede detectar este error a través del método [**IAMErrorLog:: LogError**](iamerrorlog-logerror.md) .</span><span class="sxs-lookup"><span data-stu-id="5ea96-126">The application can catch this error through the [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) method.</span></span> <span data-ttu-id="5ea96-127">(Para obtener más información, vea [registrar errores](logging-errors.md) y [errores de representación](rendering-errors.md)).</span><span class="sxs-lookup"><span data-stu-id="5ea96-127">(For more information, see [Logging Errors](logging-errors.md) and [Rendering Errors](rendering-errors.md).)</span></span>

<span data-ttu-id="5ea96-128">El formato de recompresión inteligente no es persistente.</span><span class="sxs-lookup"><span data-stu-id="5ea96-128">The smart recompression format is not persistent.</span></span> <span data-ttu-id="5ea96-129">Si una aplicación utiliza la recompresión inteligente, debe establecer el formato de recompresión cada vez que cargue un archivo de proyecto.</span><span class="sxs-lookup"><span data-stu-id="5ea96-129">If an application uses smart recompression, it must set the recompression format whenever it loads a project file.</span></span>

> [!Note]  
> <span data-ttu-id="5ea96-130">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="5ea96-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5ea96-131">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5ea96-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5ea96-132">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5ea96-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5ea96-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ea96-133">Requirements</span></span>



| <span data-ttu-id="5ea96-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ea96-134">Requirement</span></span> | <span data-ttu-id="5ea96-135">Value</span><span class="sxs-lookup"><span data-stu-id="5ea96-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea96-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ea96-136">Header</span></span><br/>  | <dl> <span data-ttu-id="5ea96-137"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ea96-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5ea96-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5ea96-138">Library</span></span><br/> | <dl> <span data-ttu-id="5ea96-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ea96-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ea96-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ea96-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ea96-141">**Interfaz IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="5ea96-141">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="5ea96-142">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="5ea96-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="5ea96-143">Smart Render Engine</span><span class="sxs-lookup"><span data-stu-id="5ea96-143">Smart Render Engine</span></span>](smart-render-engine.md)
</dt> <dt>

[<span data-ttu-id="5ea96-144">Escribir un proyecto en un archivo</span><span class="sxs-lookup"><span data-stu-id="5ea96-144">Writing a Project to a File</span></span>](writing-a-project-to-a-file.md)
</dt> </dl>

 

 




