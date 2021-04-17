---
description: No se admite.
ms.assetid: 6e45b542-be3f-4da8-808a-6aa8b4299519
title: 'IAMTimeline:: GetDirtyRange (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDirtyRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2eb0c830e7bdf441432130785e1e5397d1d4267e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653848"
---
# <a name="iamtimelinegetdirtyrange-method"></a><span data-ttu-id="49f3a-103">IAMTimeline:: GetDirtyRange (método)</span><span class="sxs-lookup"><span data-stu-id="49f3a-103">IAMTimeline::GetDirtyRange method</span></span>

> [!Note]  
> <span data-ttu-id="49f3a-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="49f3a-104">\[Deprecated.</span></span> <span data-ttu-id="49f3a-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="49f3a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="49f3a-106">No se admite.</span><span class="sxs-lookup"><span data-stu-id="49f3a-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="49f3a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49f3a-107">Syntax</span></span>


```C++
HRESULT GetDirtyRange(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="49f3a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49f3a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49f3a-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="49f3a-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="49f3a-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="49f3a-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="49f3a-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="49f3a-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="49f3a-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="49f3a-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49f3a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49f3a-113">Return value</span></span>

<span data-ttu-id="49f3a-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="49f3a-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="49f3a-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="49f3a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="49f3a-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49f3a-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="49f3a-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="49f3a-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="49f3a-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="49f3a-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="49f3a-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="49f3a-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="49f3a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49f3a-120">Requirements</span></span>



| <span data-ttu-id="49f3a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="49f3a-121">Requirement</span></span> | <span data-ttu-id="49f3a-122">Value</span><span class="sxs-lookup"><span data-stu-id="49f3a-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49f3a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49f3a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="49f3a-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="49f3a-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="49f3a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="49f3a-125">Library</span></span><br/> | <dl> <span data-ttu-id="49f3a-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49f3a-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49f3a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="49f3a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49f3a-128">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="49f3a-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




