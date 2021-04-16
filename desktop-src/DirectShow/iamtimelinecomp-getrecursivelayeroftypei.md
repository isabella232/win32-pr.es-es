---
description: 'No se admite. Llame al método IAMTimelineComp:: GetRecursiveLayerOfType en su lugar.'
ms.assetid: 857f57e2-6123-43c3-bb74-62afd0fc0b52
title: 'IAMTimelineComp:: GetRecursiveLayerOfTypeI (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfTypeI
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8aded93aa0753ee8dddf173262c80678e28037a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690228"
---
# <a name="iamtimelinecompgetrecursivelayeroftypei-method"></a><span data-ttu-id="4f9b9-104">IAMTimelineComp:: GetRecursiveLayerOfTypeI (método)</span><span class="sxs-lookup"><span data-stu-id="4f9b9-104">IAMTimelineComp::GetRecursiveLayerOfTypeI method</span></span>

> [!Note]  
> <span data-ttu-id="4f9b9-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-105">\[Deprecated.</span></span> <span data-ttu-id="4f9b9-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4f9b9-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4f9b9-107">No se admite.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-107">Not supported.</span></span> <span data-ttu-id="4f9b9-108">Llame al método [**IAMTimelineComp:: GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-108">Call the [**IAMTimelineComp::GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f9b9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f9b9-109">Syntax</span></span>


```C++
HRESULT GetRecursiveLayerOfTypeI(
   IAMTimelineObj      **ppVirtualTrack,
   long                **pWhichLayer,
   TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a><span data-ttu-id="4f9b9-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f9b9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f9b9-111">*ppVirtualTrack*</span><span class="sxs-lookup"><span data-stu-id="4f9b9-111">*ppVirtualTrack*</span></span> 
</dt> <dd>

<span data-ttu-id="4f9b9-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="4f9b9-113">*pWhichLayer*</span><span class="sxs-lookup"><span data-stu-id="4f9b9-113">*pWhichLayer*</span></span> 
</dt> <dd>

<span data-ttu-id="4f9b9-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="4f9b9-115">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="4f9b9-115">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="4f9b9-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-116">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f9b9-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f9b9-117">Return value</span></span>

<span data-ttu-id="4f9b9-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4f9b9-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4f9b9-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f9b9-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f9b9-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4f9b9-121">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4f9b9-122">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4f9b9-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4f9b9-123">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4f9b9-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f9b9-124">Requirements</span></span>



| <span data-ttu-id="4f9b9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f9b9-125">Requirement</span></span> | <span data-ttu-id="4f9b9-126">Value</span><span class="sxs-lookup"><span data-stu-id="4f9b9-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f9b9-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f9b9-127">Header</span></span><br/>  | <dl> <span data-ttu-id="4f9b9-128"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f9b9-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4f9b9-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4f9b9-129">Library</span></span><br/> | <dl> <span data-ttu-id="4f9b9-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f9b9-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f9b9-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f9b9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f9b9-132">**Interfaz IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="4f9b9-132">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> </dl>

 

 




