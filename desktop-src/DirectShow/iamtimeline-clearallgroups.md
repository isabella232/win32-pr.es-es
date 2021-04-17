---
description: El método ClearAllGroups quita todos los grupos de la escala de tiempo, junto con todos los objetos contenidos en esos grupos.
ms.assetid: b0d2a463-bd18-4377-893c-ea4fdf77b1c8
title: 'IAMTimeline:: ClearAllGroups (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.ClearAllGroups
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 05d847bdae9d6f5f5672d555a31505c2739af41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653520"
---
# <a name="iamtimelineclearallgroups-method"></a><span data-ttu-id="72b61-103">IAMTimeline:: ClearAllGroups (método)</span><span class="sxs-lookup"><span data-stu-id="72b61-103">IAMTimeline::ClearAllGroups method</span></span>

> [!Note]  
> <span data-ttu-id="72b61-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="72b61-104">\[Deprecated.</span></span> <span data-ttu-id="72b61-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="72b61-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="72b61-106">El `ClearAllGroups` método quita todos los grupos de la escala de tiempo, junto con todos los objetos contenidos en esos grupos.</span><span class="sxs-lookup"><span data-stu-id="72b61-106">The `ClearAllGroups` method removes all groups from the timeline, along with all objects contained in those groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="72b61-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72b61-107">Syntax</span></span>


```C++
HRESULT ClearAllGroups();
```



## <a name="parameters"></a><span data-ttu-id="72b61-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72b61-108">Parameters</span></span>

<span data-ttu-id="72b61-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="72b61-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="72b61-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72b61-110">Return value</span></span>

<span data-ttu-id="72b61-111">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="72b61-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="72b61-112">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="72b61-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="72b61-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72b61-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="72b61-114">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="72b61-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="72b61-115">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="72b61-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="72b61-116">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="72b61-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="72b61-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72b61-117">Requirements</span></span>



| <span data-ttu-id="72b61-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="72b61-118">Requirement</span></span> | <span data-ttu-id="72b61-119">Value</span><span class="sxs-lookup"><span data-stu-id="72b61-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72b61-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72b61-120">Header</span></span><br/>  | <dl> <span data-ttu-id="72b61-121"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="72b61-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="72b61-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="72b61-122">Library</span></span><br/> | <dl> <span data-ttu-id="72b61-123"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72b61-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72b61-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="72b61-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72b61-125">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="72b61-125">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="72b61-126">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="72b61-126">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




