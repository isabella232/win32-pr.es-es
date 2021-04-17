---
description: Sin implementar.
ms.assetid: b803ba33-d698-449f-a540-3981c4f0826a
title: 'IAMTimeline:: SetInterestRange (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetInterestRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0a3c92848380bb71bcdca0e6f6de1069d6eb998a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653632"
---
# <a name="iamtimelinesetinterestrange-method"></a><span data-ttu-id="21355-103">IAMTimeline:: SetInterestRange (método)</span><span class="sxs-lookup"><span data-stu-id="21355-103">IAMTimeline::SetInterestRange method</span></span>

> [!Note]  
> <span data-ttu-id="21355-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="21355-104">\[Deprecated.</span></span> <span data-ttu-id="21355-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="21355-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="21355-106">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="21355-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="21355-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21355-107">Syntax</span></span>


```C++
HRESULT SetInterestRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="21355-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21355-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21355-109">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="21355-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="21355-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="21355-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="21355-111">*Detención*</span><span class="sxs-lookup"><span data-stu-id="21355-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="21355-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="21355-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21355-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21355-113">Return value</span></span>

<span data-ttu-id="21355-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="21355-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="21355-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="21355-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="21355-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21355-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="21355-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="21355-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="21355-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="21355-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="21355-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="21355-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="21355-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21355-120">Requirements</span></span>



| <span data-ttu-id="21355-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="21355-121">Requirement</span></span> | <span data-ttu-id="21355-122">Value</span><span class="sxs-lookup"><span data-stu-id="21355-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21355-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21355-123">Header</span></span><br/>  | <dl> <span data-ttu-id="21355-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="21355-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="21355-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="21355-125">Library</span></span><br/> | <dl> <span data-ttu-id="21355-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21355-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21355-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="21355-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21355-128">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="21355-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




