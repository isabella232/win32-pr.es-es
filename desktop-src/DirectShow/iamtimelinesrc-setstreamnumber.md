---
description: El método SetStreamNumber especifica la secuencia que se va a leer del archivo de código fuente asociado a este objeto de origen.
ms.assetid: d40d0889-3b28-4114-9dd2-529e380eaeb8
title: 'IAMTimelineSrc:: SetStreamNumber (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStreamNumber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 32deec91d4ae0fe55b4574344dd357932856db81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690612"
---
# <a name="iamtimelinesrcsetstreamnumber-method"></a><span data-ttu-id="f5a78-103">IAMTimelineSrc:: SetStreamNumber (método)</span><span class="sxs-lookup"><span data-stu-id="f5a78-103">IAMTimelineSrc::SetStreamNumber method</span></span>

> [!Note]  
> <span data-ttu-id="f5a78-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="f5a78-104">\[Deprecated.</span></span> <span data-ttu-id="f5a78-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f5a78-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f5a78-106">El `SetStreamNumber` método especifica la secuencia que se va a leer del archivo de código fuente asociado a este objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="f5a78-106">The `SetStreamNumber` method specifies which stream to read from the source file associated with this source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5a78-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5a78-107">Syntax</span></span>


```C++
HRESULT SetStreamNumber(
   long Val
);
```



## <a name="parameters"></a><span data-ttu-id="f5a78-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5a78-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5a78-109">*Val*</span><span class="sxs-lookup"><span data-stu-id="f5a78-109">*Val*</span></span> 
</dt> <dd>

<span data-ttu-id="f5a78-110">El número de secuencia, desde el conjunto de secuencias que coinciden con el tipo de medio del grupo primario.</span><span class="sxs-lookup"><span data-stu-id="f5a78-110">The stream number, from the set of streams matching the media type of the parent group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5a78-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5a78-111">Return value</span></span>

<span data-ttu-id="f5a78-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f5a78-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f5a78-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f5a78-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5a78-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5a78-114">Remarks</span></span>

<span data-ttu-id="f5a78-115">El parámetro *Val* especifica un número de secuencia del conjunto de secuencias que coincide con el tipo de medio del grupo primario, no del conjunto completo de secuencias del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="f5a78-115">The *Val* parameter specifies a stream number from the set of streams that matches the parent group's media type, not from the entire set of streams in the source file.</span></span> <span data-ttu-id="f5a78-116">Por ejemplo, supongamos que un archivo contiene dos secuencias de vídeo y dos secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="f5a78-116">For example, For example, suppose that a file contains two video streams and two audio streams.</span></span> <span data-ttu-id="f5a78-117">Si el objeto de origen está dentro de un grupo de vídeos, al establecer *Val* en 0, se selecciona la primera secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f5a78-117">If the source object is inside a video group, setting *Val* to 0 selects the first video stream.</span></span> <span data-ttu-id="f5a78-118">El autor de la llamada es responsable de especificar un número de secuencia válido.</span><span class="sxs-lookup"><span data-stu-id="f5a78-118">The caller is responsible for specifying a valid stream number.</span></span>

<span data-ttu-id="f5a78-119">El valor predeterminado del número de secuencia es cero.</span><span class="sxs-lookup"><span data-stu-id="f5a78-119">The stream number defaults to zero.</span></span>

> [!Note]  
> <span data-ttu-id="f5a78-120">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="f5a78-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f5a78-121">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5a78-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f5a78-122">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f5a78-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f5a78-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5a78-123">Requirements</span></span>



| <span data-ttu-id="f5a78-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5a78-124">Requirement</span></span> | <span data-ttu-id="f5a78-125">Value</span><span class="sxs-lookup"><span data-stu-id="f5a78-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5a78-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5a78-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f5a78-127"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5a78-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f5a78-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f5a78-128">Library</span></span><br/> | <dl> <span data-ttu-id="f5a78-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5a78-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5a78-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5a78-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5a78-131">**Interfaz IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="f5a78-131">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="f5a78-132">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="f5a78-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




