---
description: 'El método GetDuration2 recupera la duración de la escala de tiempo. Este método es equivalente a IAMTimeline:: GetDuration, pero toma un parámetro de tipo Double.'
ms.assetid: 49f5eed3-7fab-4f08-b65c-300349b197cb
title: 'IAMTimeline:: GetDuration2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDuration2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bc840e642f6c08825f6f53869229e9cc27e87b38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653723"
---
# <a name="iamtimelinegetduration2-method"></a><span data-ttu-id="a0803-104">IAMTimeline:: GetDuration2 (método)</span><span class="sxs-lookup"><span data-stu-id="a0803-104">IAMTimeline::GetDuration2 method</span></span>

> [!Note]  
> <span data-ttu-id="a0803-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="a0803-105">\[Deprecated.</span></span> <span data-ttu-id="a0803-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a0803-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a0803-107">El `GetDuration2` método recupera la duración de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="a0803-107">The `GetDuration2` method retrieves the duration of the timeline.</span></span> <span data-ttu-id="a0803-108">Este método es equivalente a [**IAMTimeline:: GetDuration**](iamtimeline-getduration.md), pero toma un parámetro de tipo **Double**.</span><span class="sxs-lookup"><span data-stu-id="a0803-108">This method is equivalent to [**IAMTimeline::GetDuration**](iamtimeline-getduration.md), but takes a parameter of type **double**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0803-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0803-109">Syntax</span></span>


```C++
HRESULT GetDuration2(
   double *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="a0803-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a0803-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0803-111">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="a0803-111">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="a0803-112">Recibe la duración de la escala de tiempo, en segundos fraccionarios.</span><span class="sxs-lookup"><span data-stu-id="a0803-112">Receives the duration of the timeline, in fractional seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0803-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0803-113">Return value</span></span>

<span data-ttu-id="a0803-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a0803-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a0803-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a0803-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0803-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0803-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a0803-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="a0803-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a0803-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a0803-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a0803-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a0803-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a0803-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0803-120">Requirements</span></span>



| <span data-ttu-id="a0803-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0803-121">Requirement</span></span> | <span data-ttu-id="a0803-122">Value</span><span class="sxs-lookup"><span data-stu-id="a0803-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0803-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0803-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a0803-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0803-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a0803-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a0803-125">Library</span></span><br/> | <dl> <span data-ttu-id="a0803-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0803-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0803-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0803-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0803-128">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="a0803-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="a0803-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="a0803-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




