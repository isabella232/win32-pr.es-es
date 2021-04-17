---
description: No se admite.
ms.assetid: 7f97b1c4-0508-45a5-a6fd-5dae17f0fa60
title: 'IAMTimelineObj:: GetDirtyRange (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetDirtyRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d4f82b34c70cafd49bf21d662cf8b397b8d6316d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691060"
---
# <a name="iamtimelineobjgetdirtyrange-method"></a><span data-ttu-id="fc052-103">IAMTimelineObj:: GetDirtyRange (método)</span><span class="sxs-lookup"><span data-stu-id="fc052-103">IAMTimelineObj::GetDirtyRange method</span></span>

> [!Note]  
> <span data-ttu-id="fc052-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="fc052-104">\[Deprecated.</span></span> <span data-ttu-id="fc052-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fc052-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fc052-106">No se admite.</span><span class="sxs-lookup"><span data-stu-id="fc052-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc052-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc052-107">Syntax</span></span>


```C++
HRESULT GetDirtyRange(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="fc052-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc052-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc052-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="fc052-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="fc052-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="fc052-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="fc052-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="fc052-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="fc052-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="fc052-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc052-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc052-113">Return value</span></span>

<span data-ttu-id="fc052-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="fc052-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fc052-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fc052-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc052-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc052-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fc052-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="fc052-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fc052-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fc052-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fc052-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="fc052-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fc052-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc052-120">Requirements</span></span>



| <span data-ttu-id="fc052-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc052-121">Requirement</span></span> | <span data-ttu-id="fc052-122">Value</span><span class="sxs-lookup"><span data-stu-id="fc052-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc052-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc052-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fc052-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc052-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fc052-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc052-125">Library</span></span><br/> | <dl> <span data-ttu-id="fc052-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc052-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc052-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc052-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc052-128">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="fc052-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




