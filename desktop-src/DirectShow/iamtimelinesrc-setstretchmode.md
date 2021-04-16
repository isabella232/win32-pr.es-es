---
description: El método SetStretchMode establece el modo Stretch. El modo Stretch determina cómo se representa un origen de vídeo si su tamaño no coincide con las dimensiones de salida.
ms.assetid: 4f720975-5035-4539-895f-3eb3c3b31719
title: 'IAMTimelineSrc:: SetStretchMode (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2fae71362f6e09d2eae6c2cdf574a2fbda43930b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690080"
---
# <a name="iamtimelinesrcsetstretchmode-method"></a><span data-ttu-id="aabea-104">IAMTimelineSrc:: SetStretchMode (método)</span><span class="sxs-lookup"><span data-stu-id="aabea-104">IAMTimelineSrc::SetStretchMode method</span></span>

> [!Note]  
> <span data-ttu-id="aabea-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="aabea-105">\[Deprecated.</span></span> <span data-ttu-id="aabea-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="aabea-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="aabea-107">El `SetStretchMode` método establece el modo Stretch.</span><span class="sxs-lookup"><span data-stu-id="aabea-107">The `SetStretchMode` method sets the stretch mode.</span></span> <span data-ttu-id="aabea-108">El modo Stretch determina cómo se representa un origen de vídeo si su tamaño no coincide con las dimensiones de salida.</span><span class="sxs-lookup"><span data-stu-id="aabea-108">The stretch mode determines how a video source is rendered if its size does not match the output dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="aabea-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aabea-109">Syntax</span></span>


```C++
HRESULT SetStretchMode(
   int nStretchMode
);
```



## <a name="parameters"></a><span data-ttu-id="aabea-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aabea-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aabea-111">*nStretchMode*</span><span class="sxs-lookup"><span data-stu-id="aabea-111">*nStretchMode*</span></span> 
</dt> <dd>

<span data-ttu-id="aabea-112">Marca que indica el modo de ajuste actual.</span><span class="sxs-lookup"><span data-stu-id="aabea-112">Flag indicating the current stretch mode.</span></span> <span data-ttu-id="aabea-113">Para obtener una lista de los valores posibles, vea [**cambiar el tamaño**](resize-flags.md)de las marcas.</span><span class="sxs-lookup"><span data-stu-id="aabea-113">For a list of possible values, see [**Resize Flags**](resize-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aabea-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aabea-114">Return value</span></span>

<span data-ttu-id="aabea-115">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="aabea-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="aabea-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aabea-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="aabea-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="aabea-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="aabea-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="aabea-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="aabea-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="aabea-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="aabea-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aabea-120">Requirements</span></span>



| <span data-ttu-id="aabea-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="aabea-121">Requirement</span></span> | <span data-ttu-id="aabea-122">Value</span><span class="sxs-lookup"><span data-stu-id="aabea-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aabea-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aabea-123">Header</span></span><br/>  | <dl> <span data-ttu-id="aabea-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="aabea-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="aabea-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aabea-125">Library</span></span><br/> | <dl> <span data-ttu-id="aabea-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aabea-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aabea-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="aabea-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aabea-128">**Interfaz IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="aabea-128">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="aabea-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="aabea-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




