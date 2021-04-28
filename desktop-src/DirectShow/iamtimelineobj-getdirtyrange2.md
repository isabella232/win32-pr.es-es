---
description: 'Método IAMTimelineObj::GetDirtyRange2: no compatible.'
ms.assetid: 3acd36f2-52f4-4734-a753-c6a6ce7e9187
title: Método IAMTimelineObj::GetDirtyRange2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetDirtyRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 14c573403bf946b54bbfcc74ae41145a3f1c5c7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119523"
---
# <a name="iamtimelineobjgetdirtyrange2-method"></a><span data-ttu-id="c8743-103">IamTimelineObj::GetDirtyRange2 (método)</span><span class="sxs-lookup"><span data-stu-id="c8743-103">IAMTimelineObj::GetDirtyRange2 method</span></span>

> [!Note]  
> <span data-ttu-id="c8743-104">\[Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="c8743-104">\[Deprecated.</span></span> <span data-ttu-id="c8743-105">Esta API puede quitarse de futuras versiones de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c8743-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c8743-106">No compatible.</span><span class="sxs-lookup"><span data-stu-id="c8743-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8743-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8743-107">Syntax</span></span>


```C++
HRESULT GetDirtyRange2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="c8743-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8743-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8743-109">*Pstart*</span><span class="sxs-lookup"><span data-stu-id="c8743-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="c8743-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c8743-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="c8743-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="c8743-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="c8743-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c8743-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8743-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8743-113">Return value</span></span>

<span data-ttu-id="c8743-114">Si este método se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c8743-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c8743-115">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="c8743-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8743-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c8743-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c8743-117">El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="c8743-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c8743-118">Para obtener Qedit.h, descargue Microsoft Windows SDK [Update para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c8743-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c8743-119">Qedit.h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3.5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c8743-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c8743-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8743-120">Requirements</span></span>



| <span data-ttu-id="c8743-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8743-121">Requirement</span></span> | <span data-ttu-id="c8743-122">Value</span><span class="sxs-lookup"><span data-stu-id="c8743-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8743-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8743-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c8743-124"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="c8743-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c8743-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c8743-125">Library</span></span><br/> | <dl> <span data-ttu-id="c8743-126"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8743-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8743-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c8743-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8743-128">**IamTimelineObj (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="c8743-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




