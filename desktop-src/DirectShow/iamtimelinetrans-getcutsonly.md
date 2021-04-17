---
description: El método GetCutsOnly determina si la transición se representa como un corte. Si es así, la transición se produce de forma instantánea en el punto de corte.
ms.assetid: d7959816-1152-4bc4-b3f8-bed69b450530
title: 'IAMTimelineTrans:: GetCutsOnly (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d3bbec55ddfe77c053135054fde9b64efce516a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691025"
---
# <a name="iamtimelinetransgetcutsonly-method"></a><span data-ttu-id="98e14-104">IAMTimelineTrans:: GetCutsOnly (método)</span><span class="sxs-lookup"><span data-stu-id="98e14-104">IAMTimelineTrans::GetCutsOnly method</span></span>

> [!Note]  
> <span data-ttu-id="98e14-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="98e14-105">\[Deprecated.</span></span> <span data-ttu-id="98e14-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="98e14-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="98e14-107">El `GetCutsOnly` método determina si la transición se representa como un corte.</span><span class="sxs-lookup"><span data-stu-id="98e14-107">The `GetCutsOnly` method determines whether the transition is rendered as a cut.</span></span> <span data-ttu-id="98e14-108">Si es así, la transición se produce de forma instantánea en el punto de corte.</span><span class="sxs-lookup"><span data-stu-id="98e14-108">If so, the transition occurs instantaneously at the cut point.</span></span>

## <a name="syntax"></a><span data-ttu-id="98e14-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98e14-109">Syntax</span></span>


```C++
HRESULT GetCutsOnly(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="98e14-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98e14-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98e14-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="98e14-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="98e14-112">Recibe un valor booleano que especifica si la transición se representa como un corte.</span><span class="sxs-lookup"><span data-stu-id="98e14-112">Receives a Boolean value specifying whether the transition is rendered as a cut.</span></span> <span data-ttu-id="98e14-113">Si es **true**, la transición es un corte instantáneo.</span><span class="sxs-lookup"><span data-stu-id="98e14-113">If **TRUE**, the transition is an instantaneous cut.</span></span> <span data-ttu-id="98e14-114">Si **es false**, la transición se produce a lo largo de su duración normal.</span><span class="sxs-lookup"><span data-stu-id="98e14-114">If **FALSE**, the transition occurs over its normal duration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98e14-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98e14-115">Return value</span></span>

<span data-ttu-id="98e14-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="98e14-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="98e14-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="98e14-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="98e14-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98e14-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="98e14-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="98e14-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="98e14-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="98e14-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="98e14-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="98e14-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="98e14-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98e14-122">Requirements</span></span>



| <span data-ttu-id="98e14-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="98e14-123">Requirement</span></span> | <span data-ttu-id="98e14-124">Value</span><span class="sxs-lookup"><span data-stu-id="98e14-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98e14-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98e14-125">Header</span></span><br/>  | <dl> <span data-ttu-id="98e14-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="98e14-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="98e14-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98e14-127">Library</span></span><br/> | <dl> <span data-ttu-id="98e14-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98e14-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98e14-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="98e14-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98e14-130">**Interfaz IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="98e14-130">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="98e14-131">**IAMTimelineTrans::SetCutsOnly**</span><span class="sxs-lookup"><span data-stu-id="98e14-131">**IAMTimelineTrans::SetCutsOnly**</span></span>](iamtimelinetrans-setcutsonly.md)
</dt> <dt>

[<span data-ttu-id="98e14-132">**IAMTimelineTrans::GetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="98e14-132">**IAMTimelineTrans::GetCutPoint**</span></span>](iamtimelinetrans-getcutpoint.md)
</dt> <dt>

[<span data-ttu-id="98e14-133">**IAMTimeline::TransitionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="98e14-133">**IAMTimeline::TransitionsEnabled**</span></span>](iamtimeline-transitionsenabled.md)
</dt> <dt>

[<span data-ttu-id="98e14-134">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="98e14-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




