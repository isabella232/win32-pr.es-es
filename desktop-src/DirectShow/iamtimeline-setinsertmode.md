---
description: 'Método IAMTimeline::SetInsertMode: no implementado.'
ms.assetid: 31ff6e32-e8e7-45b4-af62-b6a84e061c94
title: Método IAMTimeline::SetInsertMode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetInsertMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c3d89e779d1941b23e30c3f96314dd99058c4cf8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098673"
---
# <a name="iamtimelinesetinsertmode-method"></a><span data-ttu-id="1c59d-103">IamTimeline::SetInsertMode (método)</span><span class="sxs-lookup"><span data-stu-id="1c59d-103">IAMTimeline::SetInsertMode method</span></span>

> [!Note]  
> <span data-ttu-id="1c59d-104">\[Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="1c59d-104">\[Deprecated.</span></span> <span data-ttu-id="1c59d-105">Esta API puede quitarse de futuras versiones de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1c59d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1c59d-106">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="1c59d-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c59d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c59d-107">Syntax</span></span>


```C++
HRESULT SetInsertMode(
   long Mode
);
```



## <a name="parameters"></a><span data-ttu-id="1c59d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c59d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c59d-109">*Modo*</span><span class="sxs-lookup"><span data-stu-id="1c59d-109">*Mode*</span></span> 
</dt> <dd>

<span data-ttu-id="1c59d-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="1c59d-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c59d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c59d-111">Return value</span></span>

<span data-ttu-id="1c59d-112">Si este método se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1c59d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1c59d-113">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="1c59d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c59d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1c59d-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1c59d-115">El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="1c59d-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1c59d-116">Para obtener Qedit.h, descargue la Microsoft Windows SDK [update para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1c59d-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1c59d-117">Qedit.h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3.5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1c59d-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1c59d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c59d-118">Requirements</span></span>



| <span data-ttu-id="1c59d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c59d-119">Requirement</span></span> | <span data-ttu-id="1c59d-120">Value</span><span class="sxs-lookup"><span data-stu-id="1c59d-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c59d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c59d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1c59d-122"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="1c59d-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1c59d-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1c59d-123">Library</span></span><br/> | <dl> <span data-ttu-id="1c59d-124"><dt>Strmiids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c59d-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c59d-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1c59d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c59d-126">**IamTimeline (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="1c59d-126">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




