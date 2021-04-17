---
description: El método WriteBitmapBits recupera un fotograma de vídeo en el tiempo medio especificado y lo escribe en un archivo. El fotograma de vídeo siempre tiene el formato RGB de 24 bits.
ms.assetid: 8b21f37b-553d-4de2-8725-c94c29fa3a1a
title: 'IMediaDet:: WriteBitmapBits (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.WriteBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 79bf54f136cc2ab9db1208ad6c2b4e5cb12bd950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679531"
---
# <a name="imediadetwritebitmapbits-method"></a><span data-ttu-id="e50e1-104">IMediaDet:: WriteBitmapBits (método)</span><span class="sxs-lookup"><span data-stu-id="e50e1-104">IMediaDet::WriteBitmapBits method</span></span>

> [!Note]  
> <span data-ttu-id="e50e1-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="e50e1-105">\[Deprecated.</span></span> <span data-ttu-id="e50e1-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e50e1-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e50e1-107">El `WriteBitmapBits` método recupera un fotograma de vídeo en el tiempo medio especificado y lo escribe en un archivo.</span><span class="sxs-lookup"><span data-stu-id="e50e1-107">The `WriteBitmapBits` method retrieves a video frame at the specified media time and writes it to a file.</span></span> <span data-ttu-id="e50e1-108">El fotograma de vídeo siempre tiene el formato RGB de 24 bits.</span><span class="sxs-lookup"><span data-stu-id="e50e1-108">The video frame is always in 24-bit RGB format.</span></span>

## <a name="syntax"></a><span data-ttu-id="e50e1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e50e1-109">Syntax</span></span>


```C++
HRESULT WriteBitmapBits(
   double StreamTime,
   long   Width,
   long   Height,
   BSTR   Filename
);
```



## <a name="parameters"></a><span data-ttu-id="e50e1-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e50e1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e50e1-111">*StreamTime*</span><span class="sxs-lookup"><span data-stu-id="e50e1-111">*StreamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="e50e1-112">Hora a la que se va a recuperar el fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e50e1-112">Time at which to retrieve the video frame.</span></span>

</dd> <dt>

<span data-ttu-id="e50e1-113">*Width*</span><span class="sxs-lookup"><span data-stu-id="e50e1-113">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="e50e1-114">Ancho de la imagen, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="e50e1-114">Width of the image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="e50e1-115">*Height*</span><span class="sxs-lookup"><span data-stu-id="e50e1-115">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="e50e1-116">Alto de la imagen, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="e50e1-116">Height of the image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="e50e1-117">*Nombre de archivo*</span><span class="sxs-lookup"><span data-stu-id="e50e1-117">*Filename*</span></span> 
</dt> <dd>

<span data-ttu-id="e50e1-118">Ruta de acceso del archivo en el que se va a guardar el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="e50e1-118">Path of the file in which to save the bitmap.</span></span> <span data-ttu-id="e50e1-119">Si el archivo ya existe, este método lo sobrescribe.</span><span class="sxs-lookup"><span data-stu-id="e50e1-119">If the file already exists, this method overwrites it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e50e1-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e50e1-120">Return value</span></span>

<span data-ttu-id="e50e1-121">Devuelve S correcto \_ .</span><span class="sxs-lookup"><span data-stu-id="e50e1-121">Returns S\_OK it successful.</span></span> <span data-ttu-id="e50e1-122">De lo contrario, devuelve un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="e50e1-122">Otherwise, returns an **HRESULT** value that indicates the cause of the error.</span></span> <span data-ttu-id="e50e1-123">Entre los posibles códigos de error se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e50e1-123">Possible error codes include the following:</span></span>



| <span data-ttu-id="e50e1-124">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e50e1-124">Return code</span></span>                                                                                             | <span data-ttu-id="e50e1-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="e50e1-125">Description</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e50e1-126"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="e50e1-126"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="e50e1-127">No se pudo agregar el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) al gráfico.</span><span class="sxs-lookup"><span data-stu-id="e50e1-127">Could not add the [**Sample Grabber**](sample-grabber-filter.md) filter to the graph.</span></span><br/> |
| <dl> <span data-ttu-id="e50e1-128"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="e50e1-128"><dt>**E\_FAIL**</dt></span></span> </dl>                  | <span data-ttu-id="e50e1-129">Error.</span><span class="sxs-lookup"><span data-stu-id="e50e1-129">Failure.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="e50e1-130"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e50e1-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>           | <span data-ttu-id="e50e1-131">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="e50e1-131">Insufficient memory.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="e50e1-132"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="e50e1-132"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>            | <span data-ttu-id="e50e1-133">error inesperado.</span><span class="sxs-lookup"><span data-stu-id="e50e1-133">Unexpected error.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="e50e1-134"><dt>**STG \_ E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="e50e1-134"><dt>**STG\_E\_ACCESSDENIED**</dt></span></span> </dl>     | <span data-ttu-id="e50e1-135">No se puede sobrescribir el archivo.</span><span class="sxs-lookup"><span data-stu-id="e50e1-135">Cannot overwrite file.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="e50e1-136"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="e50e1-136"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="e50e1-137">Tipo de medio no válido.</span><span class="sxs-lookup"><span data-stu-id="e50e1-137">Invalid media type.</span></span><br/>                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="e50e1-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e50e1-138">Remarks</span></span>

<span data-ttu-id="e50e1-139">Antes de llamar a este método, establezca el nombre de archivo y el flujo mediante una llamada a [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) y [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="e50e1-139">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="e50e1-140">Este método coloca el detector de medios en el modo de agarre de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="e50e1-140">This method puts the media detector into bitmap grab mode.</span></span> <span data-ttu-id="e50e1-141">Una vez que se ha llamado a este método, los distintos métodos de información de secuencia de **IMediaDet** no funcionan, a menos que cree una nueva instancia del detector de medios.</span><span class="sxs-lookup"><span data-stu-id="e50e1-141">Once this method has been called, the various stream information methods in **IMediaDet** do not work, unless you create a new instance of the media detector.</span></span>

> [!Note]  
> <span data-ttu-id="e50e1-142">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="e50e1-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e50e1-143">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e50e1-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e50e1-144">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e50e1-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e50e1-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e50e1-145">Requirements</span></span>



| <span data-ttu-id="e50e1-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="e50e1-146">Requirement</span></span> | <span data-ttu-id="e50e1-147">Value</span><span class="sxs-lookup"><span data-stu-id="e50e1-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e50e1-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e50e1-148">Header</span></span><br/>  | <dl> <span data-ttu-id="e50e1-149"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="e50e1-149"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e50e1-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e50e1-150">Library</span></span><br/> | <dl> <span data-ttu-id="e50e1-151"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e50e1-151"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e50e1-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="e50e1-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e50e1-153">**Interfaz IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="e50e1-153">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="e50e1-154">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="e50e1-154">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




