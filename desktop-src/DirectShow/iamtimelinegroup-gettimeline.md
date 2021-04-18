---
description: El método GetTimeline recupera la escala de tiempo a la que pertenece este grupo.
ms.assetid: a57d75c9-6e2e-426f-9403-ad32188b2211
title: 'IAMTimelineGroup:: GetTimeline (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b85b0c6f1730c2946134a36d33537f311b6603f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680305"
---
# <a name="iamtimelinegroupgettimeline-method"></a><span data-ttu-id="4c9b1-103">IAMTimelineGroup:: GetTimeline (método)</span><span class="sxs-lookup"><span data-stu-id="4c9b1-103">IAMTimelineGroup::GetTimeline method</span></span>

> [!Note]  
> <span data-ttu-id="4c9b1-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="4c9b1-104">\[Deprecated.</span></span> <span data-ttu-id="4c9b1-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4c9b1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4c9b1-106">El `GetTimeline` método recupera la escala de tiempo a la que pertenece este grupo.</span><span class="sxs-lookup"><span data-stu-id="4c9b1-106">The `GetTimeline` method retrieves the timeline to which this group belongs.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c9b1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c9b1-107">Syntax</span></span>


```C++
HRESULT GetTimeline(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="4c9b1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c9b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c9b1-109">*ppTimeline* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4c9b1-109">*ppTimeline* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c9b1-110">Recibe la interfaz [**IAMTimeline**](iamtimeline.md) de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="4c9b1-110">Receives the timeline's [**IAMTimeline**](iamtimeline.md) interface.</span></span> <span data-ttu-id="4c9b1-111">Si el grupo no es parte de una escala de tiempo, el valor se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="4c9b1-111">If the group is not part of a timeline, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c9b1-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c9b1-112">Return value</span></span>

<span data-ttu-id="4c9b1-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4c9b1-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4c9b1-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4c9b1-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c9b1-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c9b1-115">Remarks</span></span>

<span data-ttu-id="4c9b1-116">Si el valor devuelto en *ppTimeline* no es **null**, la interfaz **IAMTimeline** tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="4c9b1-116">If the value returned in *ppTimeline* is not **NULL**, the **IAMTimeline** interface has an outstanding reference count.</span></span> <span data-ttu-id="4c9b1-117">Asegúrese de liberar la interfaz cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="4c9b1-117">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="4c9b1-118">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="4c9b1-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4c9b1-119">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4c9b1-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4c9b1-120">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4c9b1-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4c9b1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c9b1-121">Requirements</span></span>



| <span data-ttu-id="4c9b1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c9b1-122">Requirement</span></span> | <span data-ttu-id="4c9b1-123">Value</span><span class="sxs-lookup"><span data-stu-id="4c9b1-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c9b1-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c9b1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4c9b1-125"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c9b1-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4c9b1-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4c9b1-126">Library</span></span><br/> | <dl> <span data-ttu-id="4c9b1-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c9b1-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c9b1-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c9b1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c9b1-129">**Interfaz IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="4c9b1-129">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="4c9b1-130">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="4c9b1-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




