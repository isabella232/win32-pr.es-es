---
description: 'El método GetCutPoint2 recupera el punto de corte. Este método es equivalente a IAMTimelineTrans:: GetCutPoint, pero toma un valor REFTIME.'
ms.assetid: bf2b7cac-6740-44d8-a889-8c745a23db19
title: 'IAMTimelineTrans:: GetCutPoint2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 68712da95da2f5c21d5e370c688002aa14a8a166
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691026"
---
# <a name="iamtimelinetransgetcutpoint2-method"></a><span data-ttu-id="4c71c-104">IAMTimelineTrans:: GetCutPoint2 (método)</span><span class="sxs-lookup"><span data-stu-id="4c71c-104">IAMTimelineTrans::GetCutPoint2 method</span></span>

> [!Note]  
> <span data-ttu-id="4c71c-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="4c71c-105">\[Deprecated.</span></span> <span data-ttu-id="4c71c-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4c71c-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4c71c-107">El `GetCutPoint2` método recupera el punto de corte.</span><span class="sxs-lookup"><span data-stu-id="4c71c-107">The `GetCutPoint2` method retrieves the cut point.</span></span> <span data-ttu-id="4c71c-108">Este método es equivalente a [**IAMTimelineTrans:: GetCutPoint**](iamtimelinetrans-getcutpoint.md), pero toma un valor [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="4c71c-108">This method is equivalent to [**IAMTimelineTrans::GetCutPoint**](iamtimelinetrans-getcutpoint.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c71c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c71c-109">Syntax</span></span>


```C++
HRESULT GetCutPoint2(
   REFTIME *pTLTime
);
```



## <a name="parameters"></a><span data-ttu-id="4c71c-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c71c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c71c-111">*pTLTime*</span><span class="sxs-lookup"><span data-stu-id="4c71c-111">*pTLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="4c71c-112">Recibe el punto de corte, en segundos, con respecto a la hora de inicio de la transición.</span><span class="sxs-lookup"><span data-stu-id="4c71c-112">Receives the cut point, relative to the start time of the transition, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c71c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c71c-113">Return value</span></span>

<span data-ttu-id="4c71c-114">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="4c71c-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="4c71c-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4c71c-115">Return code</span></span>                                                                               | <span data-ttu-id="4c71c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c71c-116">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4c71c-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="4c71c-117"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="4c71c-118">No se estableció el punto de corte.</span><span class="sxs-lookup"><span data-stu-id="4c71c-118">The cut point was not set.</span></span> <span data-ttu-id="4c71c-119">El valor devuelto es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4c71c-119">The value returned is the default value.</span></span><br/> |
| <dl> <span data-ttu-id="4c71c-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="4c71c-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="4c71c-121">El punto de corte se estableció en un valor distinto del predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4c71c-121">The cut point was set to a value other than the default.</span></span><br/>            |
| <dl> <span data-ttu-id="4c71c-122"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="4c71c-122"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="4c71c-123">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="4c71c-123">**NULL** pointer argument.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="4c71c-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c71c-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4c71c-125">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="4c71c-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4c71c-126">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4c71c-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4c71c-127">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4c71c-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4c71c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c71c-128">Requirements</span></span>



| <span data-ttu-id="4c71c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c71c-129">Requirement</span></span> | <span data-ttu-id="4c71c-130">Value</span><span class="sxs-lookup"><span data-stu-id="4c71c-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c71c-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c71c-131">Header</span></span><br/>  | <dl> <span data-ttu-id="4c71c-132"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c71c-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4c71c-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4c71c-133">Library</span></span><br/> | <dl> <span data-ttu-id="4c71c-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c71c-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c71c-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c71c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c71c-136">**Interfaz IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="4c71c-136">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="4c71c-137">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="4c71c-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




