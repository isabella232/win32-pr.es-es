---
description: El método GetDefaultFPS recupera la velocidad de fotogramas predeterminada del objeto de origen. El motor de representación utiliza este valor si no puede determinar la velocidad de fotogramas del origen original.
ms.assetid: c167cd85-e9bb-46ff-9b35-c88898a6c5a3
title: 'IAMTimelineSrc:: GetDefaultFPS (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e48ee38f385ba5ff06b2ede9b27b4558dac65270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689965"
---
# <a name="iamtimelinesrcgetdefaultfps-method"></a><span data-ttu-id="4a715-104">IAMTimelineSrc:: GetDefaultFPS (método)</span><span class="sxs-lookup"><span data-stu-id="4a715-104">IAMTimelineSrc::GetDefaultFPS method</span></span>

> [!Note]  
> <span data-ttu-id="4a715-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="4a715-105">\[Deprecated.</span></span> <span data-ttu-id="4a715-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4a715-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4a715-107">El `GetDefaultFPS` método recupera la velocidad de fotogramas predeterminada del objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="4a715-107">The `GetDefaultFPS` method retrieves the source object's default frame rate.</span></span> <span data-ttu-id="4a715-108">El motor de representación utiliza este valor si no puede determinar la velocidad de fotogramas del origen original.</span><span class="sxs-lookup"><span data-stu-id="4a715-108">The render engine uses this value if it cannot determine the frame rate from the original source.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a715-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a715-109">Syntax</span></span>


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a><span data-ttu-id="4a715-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a715-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a715-111">*pFPS*</span><span class="sxs-lookup"><span data-stu-id="4a715-111">*pFPS*</span></span> 
</dt> <dd>

<span data-ttu-id="4a715-112">Recibe la velocidad de fotogramas predeterminada, en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="4a715-112">Receives the default frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a715-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a715-113">Return value</span></span>

<span data-ttu-id="4a715-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4a715-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4a715-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4a715-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a715-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a715-116">Remarks</span></span>

<span data-ttu-id="4a715-117">La velocidad de fotogramas predeterminada no es necesaria si el formato de archivo especifica la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="4a715-117">The default frame rate is not required if the file format specifies the frame rate.</span></span> <span data-ttu-id="4a715-118">Este es el caso de los formatos de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="4a715-118">This is the case for audio and video formats.</span></span>

<span data-ttu-id="4a715-119">Si el origen es un mapa de bits o una imagen JPEG, el motor de representación lo usa como la primera imagen en una secuencia de mapa de bits independiente del dispositivo (DIB), con una velocidad de fotogramas igual a la velocidad de fotogramas predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4a715-119">If the source is a bitmap or JPEG image, the render engine uses it as the first image in a device-independent bitmap (DIB) sequence, with a frame rate equal to the default frame rate.</span></span> <span data-ttu-id="4a715-120">Para representar una imagen estática, en lugar de una secuencia DIB, establezca la velocidad de fotogramas predeterminada en 0.</span><span class="sxs-lookup"><span data-stu-id="4a715-120">To render a static image, rather than a DIB sequence, set the default frame rate to 0.</span></span>

<span data-ttu-id="4a715-121">Si el origen es un archivo GIF, no establezca la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="4a715-121">If the source is a GIF, do not set the frame rate.</span></span> <span data-ttu-id="4a715-122">En el caso de los GIF animados, el archivo GIF especifica el retraso entre cada imagen.</span><span class="sxs-lookup"><span data-stu-id="4a715-122">For animated GIFs, the GIF file specifies the delay between each image.</span></span>

> [!Note]  
> <span data-ttu-id="4a715-123">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="4a715-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4a715-124">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4a715-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4a715-125">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4a715-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4a715-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a715-126">Requirements</span></span>



| <span data-ttu-id="4a715-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a715-127">Requirement</span></span> | <span data-ttu-id="4a715-128">Value</span><span class="sxs-lookup"><span data-stu-id="4a715-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a715-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a715-129">Header</span></span><br/>  | <dl> <span data-ttu-id="4a715-130"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a715-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4a715-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a715-131">Library</span></span><br/> | <dl> <span data-ttu-id="4a715-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a715-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a715-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a715-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a715-134">**Interfaz IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="4a715-134">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="4a715-135">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="4a715-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




