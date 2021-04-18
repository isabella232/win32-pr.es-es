---
description: El método RemoveAll quita permanentemente este objeto de la escala de tiempo, incluidos los subobjetos y secundarios.
ms.assetid: 9596cf47-63fe-4839-a6d5-3685fc91a935
title: 'IAMTimelineObj:: RemoveAll (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.RemoveAll
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1888b89773253285036c89e20332d92555b6db2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680730"
---
# <a name="iamtimelineobjremoveall-method"></a><span data-ttu-id="96054-103">IAMTimelineObj:: RemoveAll (método)</span><span class="sxs-lookup"><span data-stu-id="96054-103">IAMTimelineObj::RemoveAll method</span></span>

> [!Note]  
> <span data-ttu-id="96054-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="96054-104">\[Deprecated.</span></span> <span data-ttu-id="96054-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="96054-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="96054-106">El `RemoveAll` método quita permanentemente este objeto de la escala de tiempo, incluidos los subobjetos y secundarios.</span><span class="sxs-lookup"><span data-stu-id="96054-106">The `RemoveAll` method permanently removes this object from the timeline, including subobjects and children.</span></span>

## <a name="syntax"></a><span data-ttu-id="96054-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96054-107">Syntax</span></span>


```C++
HRESULT RemoveAll();
```



## <a name="parameters"></a><span data-ttu-id="96054-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96054-108">Parameters</span></span>

<span data-ttu-id="96054-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="96054-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="96054-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96054-110">Return value</span></span>

<span data-ttu-id="96054-111">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="96054-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="96054-112">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="96054-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="96054-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96054-113">Remarks</span></span>

<span data-ttu-id="96054-114">Para quitar un objeto con el fin de volver a insertarlo en otra parte de la escala de tiempo, llame a [**IAMTimelineObj:: Remove**](iamtimelineobj-remove.md).</span><span class="sxs-lookup"><span data-stu-id="96054-114">To remove an object for the purpose of reinserting it elsewhere in the timeline, call [**IAMTimelineObj::Remove**](iamtimelineobj-remove.md).</span></span>

> [!Note]  
> <span data-ttu-id="96054-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="96054-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="96054-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="96054-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="96054-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="96054-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="96054-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96054-118">Requirements</span></span>



| <span data-ttu-id="96054-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="96054-119">Requirement</span></span> | <span data-ttu-id="96054-120">Value</span><span class="sxs-lookup"><span data-stu-id="96054-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96054-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96054-121">Header</span></span><br/>  | <dl> <span data-ttu-id="96054-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="96054-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="96054-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="96054-123">Library</span></span><br/> | <dl> <span data-ttu-id="96054-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96054-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96054-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="96054-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96054-126">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="96054-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="96054-127">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="96054-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




