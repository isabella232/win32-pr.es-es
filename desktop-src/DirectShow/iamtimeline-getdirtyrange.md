---
description: 'Método IAMTimeline::GetDirtyRange: no compatible.'
ms.assetid: 6e45b542-be3f-4da8-808a-6aa8b4299519
title: Método IAMTimeline::GetDirtyRange (Qedit.h)
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
ms.openlocfilehash: cb0ecbd8a93698d36354c251f0381c35acf288a2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119603"
---
# <a name="iamtimelinegetdirtyrange-method"></a><span data-ttu-id="eed3b-103">IamTimeline::GetDirtyRange (método)</span><span class="sxs-lookup"><span data-stu-id="eed3b-103">IAMTimeline::GetDirtyRange method</span></span>

> [!Note]  
> <span data-ttu-id="eed3b-104">\[Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="eed3b-104">\[Deprecated.</span></span> <span data-ttu-id="eed3b-105">Esta API puede quitarse de futuras versiones de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="eed3b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="eed3b-106">No compatible.</span><span class="sxs-lookup"><span data-stu-id="eed3b-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="eed3b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eed3b-107">Syntax</span></span>


```C++
HRESULT GetDirtyRange(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="eed3b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eed3b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eed3b-109">*Pstart*</span><span class="sxs-lookup"><span data-stu-id="eed3b-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="eed3b-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="eed3b-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="eed3b-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="eed3b-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="eed3b-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="eed3b-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eed3b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eed3b-113">Return value</span></span>

<span data-ttu-id="eed3b-114">Si este método se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="eed3b-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eed3b-115">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="eed3b-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="eed3b-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eed3b-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="eed3b-117">El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="eed3b-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="eed3b-118">Para obtener Qedit.h, descargue la Microsoft Windows SDK [update para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="eed3b-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="eed3b-119">Qedit.h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3.5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="eed3b-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eed3b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eed3b-120">Requirements</span></span>



| <span data-ttu-id="eed3b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="eed3b-121">Requirement</span></span> | <span data-ttu-id="eed3b-122">Value</span><span class="sxs-lookup"><span data-stu-id="eed3b-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eed3b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eed3b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="eed3b-124"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="eed3b-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="eed3b-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eed3b-125">Library</span></span><br/> | <dl> <span data-ttu-id="eed3b-126"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="eed3b-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eed3b-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="eed3b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eed3b-128">**IAMTimeline (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="eed3b-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




