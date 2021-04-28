---
description: 'Método IAMTimelineObj::SetDirtyRange: no implementado.'
ms.assetid: f3be3b5a-7ab9-44ca-8a03-33fb905d3aea
title: Método IAMTimelineObj::SetDirtyRange (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetDirtyRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7e3f70e5ba9d01733df154911c4f40d2b9d33776
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119493"
---
# <a name="iamtimelineobjsetdirtyrange-method"></a><span data-ttu-id="03fdd-103">IamTimelineObj::SetDirtyRange (método)</span><span class="sxs-lookup"><span data-stu-id="03fdd-103">IAMTimelineObj::SetDirtyRange method</span></span>

> [!Note]  
> <span data-ttu-id="03fdd-104">\[Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="03fdd-104">\[Deprecated.</span></span> <span data-ttu-id="03fdd-105">Esta API puede quitarse de futuras versiones de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="03fdd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="03fdd-106">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="03fdd-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="03fdd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03fdd-107">Syntax</span></span>


```C++
HRESULT SetDirtyRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="03fdd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03fdd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03fdd-109">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="03fdd-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="03fdd-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="03fdd-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="03fdd-111">*Detención*</span><span class="sxs-lookup"><span data-stu-id="03fdd-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="03fdd-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="03fdd-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03fdd-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03fdd-113">Return value</span></span>

<span data-ttu-id="03fdd-114">Si este método se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="03fdd-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="03fdd-115">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="03fdd-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="03fdd-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="03fdd-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="03fdd-117">El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="03fdd-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="03fdd-118">Para obtener Qedit.h, descargue la Microsoft Windows SDK [update para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="03fdd-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="03fdd-119">Qedit.h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3.5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="03fdd-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="03fdd-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03fdd-120">Requirements</span></span>



| <span data-ttu-id="03fdd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="03fdd-121">Requirement</span></span> | <span data-ttu-id="03fdd-122">Value</span><span class="sxs-lookup"><span data-stu-id="03fdd-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03fdd-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03fdd-123">Header</span></span><br/>  | <dl> <span data-ttu-id="03fdd-124"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="03fdd-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="03fdd-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="03fdd-125">Library</span></span><br/> | <dl> <span data-ttu-id="03fdd-126"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="03fdd-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03fdd-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="03fdd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03fdd-128">**IamTimelineObj (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="03fdd-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




