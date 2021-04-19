---
description: 'El método SetCutPoint2 establece la hora a la que la transición corta de un origen al siguiente, si la transición se representa como un corte. Este método es equivalente a IAMTimelineTrans:: SetCutPoint, pero toma un valor REFTIME.'
ms.assetid: d06d3ee7-04a2-4266-9995-bfabea24aef9
title: 'IAMTimelineTrans:: SetCutPoint2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 117ec522416f0d5722c8ef7aa17cd6e81720b4c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690043"
---
# <a name="iamtimelinetranssetcutpoint2-method"></a><span data-ttu-id="7824b-104">IAMTimelineTrans:: SetCutPoint2 (método)</span><span class="sxs-lookup"><span data-stu-id="7824b-104">IAMTimelineTrans::SetCutPoint2 method</span></span>

> [!Note]  
> <span data-ttu-id="7824b-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="7824b-105">\[Deprecated.</span></span> <span data-ttu-id="7824b-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7824b-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7824b-107">El `SetCutPoint2` método establece la hora a la que la transición corta de un origen al siguiente, si la transición se representa como un corte.</span><span class="sxs-lookup"><span data-stu-id="7824b-107">The `SetCutPoint2` method sets the time at which the transition cuts from one source to the next, if the transition is rendered as a cut.</span></span> <span data-ttu-id="7824b-108">Este método es equivalente a [**IAMTimelineTrans:: SetCutPoint**](iamtimelinetrans-setcutpoint.md), pero toma un valor [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="7824b-108">This method is equivalent to [**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7824b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7824b-109">Syntax</span></span>


```C++
HRESULT SetCutPoint2(
   REFTIME TLTime
);
```



## <a name="parameters"></a><span data-ttu-id="7824b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7824b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7824b-111">*TLTime*</span><span class="sxs-lookup"><span data-stu-id="7824b-111">*TLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="7824b-112">Punto de corte relativo al inicio de la transición, en segundos.</span><span class="sxs-lookup"><span data-stu-id="7824b-112">Cut point relative to the start of the transition, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7824b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7824b-113">Return value</span></span>

<span data-ttu-id="7824b-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="7824b-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7824b-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7824b-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7824b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7824b-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7824b-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="7824b-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7824b-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7824b-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7824b-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7824b-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7824b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7824b-120">Requirements</span></span>



| <span data-ttu-id="7824b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7824b-121">Requirement</span></span> | <span data-ttu-id="7824b-122">Value</span><span class="sxs-lookup"><span data-stu-id="7824b-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7824b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7824b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7824b-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="7824b-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7824b-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7824b-125">Library</span></span><br/> | <dl> <span data-ttu-id="7824b-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7824b-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7824b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="7824b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7824b-128">**Interfaz IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="7824b-128">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="7824b-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="7824b-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




