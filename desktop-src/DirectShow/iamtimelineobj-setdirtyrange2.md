---
description: 'Método IAMTimelineObj::SetDirtyRange2: no implementado.'
ms.assetid: 14ff2979-134f-45e4-98e1-1a119e1ffee2
title: Método IAMTimelineObj::SetDirtyRange2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetDirtyRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 149274a7dcb185f362ae8f58915b81af07a2bf5e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098543"
---
# <a name="iamtimelineobjsetdirtyrange2-method"></a><span data-ttu-id="9aca6-103">Método IAMTimelineObj::SetDirtyRange2</span><span class="sxs-lookup"><span data-stu-id="9aca6-103">IAMTimelineObj::SetDirtyRange2 method</span></span>

> [!Note]  
> <span data-ttu-id="9aca6-104">\[Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="9aca6-104">\[Deprecated.</span></span> <span data-ttu-id="9aca6-105">Esta API puede quitarse de futuras versiones de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9aca6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9aca6-106">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="9aca6-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aca6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9aca6-107">Syntax</span></span>


```C++
HRESULT SetDirtyRange2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="9aca6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9aca6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aca6-109">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="9aca6-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="9aca6-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="9aca6-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="9aca6-111">*Detención*</span><span class="sxs-lookup"><span data-stu-id="9aca6-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="9aca6-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="9aca6-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aca6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9aca6-113">Return value</span></span>

<span data-ttu-id="9aca6-114">Si este método se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9aca6-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9aca6-115">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="9aca6-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aca6-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9aca6-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9aca6-117">El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="9aca6-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9aca6-118">Para obtener Qedit.h, descargue la Microsoft Windows SDK [update para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9aca6-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9aca6-119">Qedit.h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3.5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9aca6-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9aca6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9aca6-120">Requirements</span></span>



| <span data-ttu-id="9aca6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9aca6-121">Requirement</span></span> | <span data-ttu-id="9aca6-122">Value</span><span class="sxs-lookup"><span data-stu-id="9aca6-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9aca6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9aca6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9aca6-124"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="9aca6-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9aca6-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9aca6-125">Library</span></span><br/> | <dl> <span data-ttu-id="9aca6-126"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9aca6-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aca6-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9aca6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aca6-128">**IAMTimelineObj (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="9aca6-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




