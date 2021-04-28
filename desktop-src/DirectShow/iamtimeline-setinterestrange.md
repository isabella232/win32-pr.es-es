---
description: 'Método IAMTimeline::SetInterestRange: no implementado.'
ms.assetid: b803ba33-d698-449f-a540-3981c4f0826a
title: Método IAMTimeline::SetInterestRange (Qedit.h)
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
ms.openlocfilehash: 23485bbdc2292e0d341e3fef0646fb68616698c4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119573"
---
# <a name="iamtimelinesetinterestrange-method"></a><span data-ttu-id="9b695-103">IamTimeline::SetInterestRange (método)</span><span class="sxs-lookup"><span data-stu-id="9b695-103">IAMTimeline::SetInterestRange method</span></span>

> [!Note]  
> <span data-ttu-id="9b695-104">\[Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="9b695-104">\[Deprecated.</span></span> <span data-ttu-id="9b695-105">Esta API puede quitarse de futuras versiones de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9b695-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9b695-106">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="9b695-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b695-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b695-107">Syntax</span></span>


```C++
HRESULT SetInterestRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="9b695-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b695-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b695-109">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="9b695-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="9b695-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="9b695-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="9b695-111">*Detención*</span><span class="sxs-lookup"><span data-stu-id="9b695-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="9b695-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="9b695-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b695-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b695-113">Return value</span></span>

<span data-ttu-id="9b695-114">Si este método se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9b695-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9b695-115">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="9b695-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b695-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9b695-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9b695-117">El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="9b695-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9b695-118">Para obtener Qedit.h, descargue la Microsoft Windows SDK [update para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9b695-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9b695-119">Qedit.h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3.5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9b695-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9b695-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b695-120">Requirements</span></span>



| <span data-ttu-id="9b695-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b695-121">Requirement</span></span> | <span data-ttu-id="9b695-122">Value</span><span class="sxs-lookup"><span data-stu-id="9b695-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b695-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b695-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9b695-124"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="9b695-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9b695-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b695-125">Library</span></span><br/> | <dl> <span data-ttu-id="9b695-126"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b695-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b695-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9b695-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b695-128">**IAMTimeline (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="9b695-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




