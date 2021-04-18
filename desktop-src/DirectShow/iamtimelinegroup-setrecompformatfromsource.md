---
description: El método SetRecompFormatFromSource establece el formato de recompresión de vídeo con el formato de compresión de un archivo de código fuente.
ms.assetid: 2d42876a-524b-454d-b4f1-353afe3a4d28
title: 'IAMTimelineGroup:: SetRecompFormatFromSource (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetRecompFormatFromSource
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: adf4bfcf9d76ed40092eba7c612f4213c7aacb0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680918"
---
# <a name="iamtimelinegroupsetrecompformatfromsource-method"></a><span data-ttu-id="17b1e-103">IAMTimelineGroup:: SetRecompFormatFromSource (método)</span><span class="sxs-lookup"><span data-stu-id="17b1e-103">IAMTimelineGroup::SetRecompFormatFromSource method</span></span>

> [!Note]  
> <span data-ttu-id="17b1e-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="17b1e-104">\[Deprecated.</span></span> <span data-ttu-id="17b1e-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="17b1e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="17b1e-106">El `SetRecompFormatFromSource` método establece el formato de recompresión de vídeo con el formato de compresión de un archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="17b1e-106">The `SetRecompFormatFromSource` method sets the video recompression format using the compression format from a source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="17b1e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17b1e-107">Syntax</span></span>


```C++
HRESULT SetRecompFormatFromSource(
   IAMTimelineSrc *pSource
);
```



## <a name="parameters"></a><span data-ttu-id="17b1e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17b1e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17b1e-109">*pSource*</span><span class="sxs-lookup"><span data-stu-id="17b1e-109">*pSource*</span></span> 
</dt> <dd>

<span data-ttu-id="17b1e-110">Puntero a la interfaz [**IAMTimelineSrc**](iamtimelinesrc.md) del objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="17b1e-110">Pointer to the [**IAMTimelineSrc**](iamtimelinesrc.md) interface of the source object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17b1e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17b1e-111">Return value</span></span>

<span data-ttu-id="17b1e-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="17b1e-112">Returns an **HRESULT** values.</span></span> <span data-ttu-id="17b1e-113">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="17b1e-113">Possible values include the following.</span></span>



| <span data-ttu-id="17b1e-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="17b1e-114">Return code</span></span>                                                                                             | <span data-ttu-id="17b1e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="17b1e-115">Description</span></span>                                                                                            |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="17b1e-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="17b1e-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="17b1e-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="17b1e-117">Success.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="17b1e-118"><dt>**E \_ sin \_ escala de tiempo**</dt></span><span class="sxs-lookup"><span data-stu-id="17b1e-118"><dt>**E\_NO\_TIMELINE**</dt></span></span> </dl>          | <span data-ttu-id="17b1e-119">El grupo no está dentro de una escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="17b1e-119">The group is not within a timeline.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="17b1e-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="17b1e-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>           | <span data-ttu-id="17b1e-121">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="17b1e-121">Insufficient memory.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="17b1e-122"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="17b1e-122"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="17b1e-123">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="17b1e-123">**NULL** pointer argument.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="17b1e-124"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="17b1e-124"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="17b1e-125">Tipo de medio no válido.</span><span class="sxs-lookup"><span data-stu-id="17b1e-125">Invalid media type.</span></span> <span data-ttu-id="17b1e-126">El grupo no es un grupo de vídeos o el archivo de origen no tiene ningún flujo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="17b1e-126">The group is not a video group, or the source file has no video stream.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="17b1e-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17b1e-127">Remarks</span></span>

<span data-ttu-id="17b1e-128">Este método busca el archivo de código fuente asociado a *pSource*, recupera el tipo de medio de la primera secuencia de vídeo en el archivo y establece el formato de compresión de grupo mediante ese tipo.</span><span class="sxs-lookup"><span data-stu-id="17b1e-128">This method finds the source file associated with *pSource*, retrieves the media type of the first video stream in the file, and sets the group compression format using that type.</span></span> <span data-ttu-id="17b1e-129">Para obtener más información sobre los formatos de compresión, vea [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md).</span><span class="sxs-lookup"><span data-stu-id="17b1e-129">For more information about compression formats, see [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md).</span></span>

> [!Note]  
> <span data-ttu-id="17b1e-130">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="17b1e-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="17b1e-131">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="17b1e-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="17b1e-132">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="17b1e-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="17b1e-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17b1e-133">Requirements</span></span>



| <span data-ttu-id="17b1e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="17b1e-134">Requirement</span></span> | <span data-ttu-id="17b1e-135">Value</span><span class="sxs-lookup"><span data-stu-id="17b1e-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17b1e-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17b1e-136">Header</span></span><br/>  | <dl> <span data-ttu-id="17b1e-137"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="17b1e-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="17b1e-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="17b1e-138">Library</span></span><br/> | <dl> <span data-ttu-id="17b1e-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17b1e-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17b1e-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="17b1e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17b1e-141">**Interfaz IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="17b1e-141">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="17b1e-142">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="17b1e-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




