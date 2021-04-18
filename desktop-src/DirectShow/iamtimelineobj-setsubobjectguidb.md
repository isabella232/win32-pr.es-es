---
description: 'El método SetSubObjectGUIDB especifica el GUID del subobjeto asociado a este objeto. Este método es equivalente a IAMTimelineObj:: SetSubObjectGUID, pero toma un valor BSTR.'
ms.assetid: b2523b17-1df3-4be5-8bbb-6b67815f9349
title: 'IAMTimelineObj:: SetSubObjectGUIDB (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetSubObjectGUIDB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8df74249f061321ccd710822b8c2e0b76d5c3582
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679508"
---
# <a name="iamtimelineobjsetsubobjectguidb-method"></a><span data-ttu-id="ebb3e-104">IAMTimelineObj:: SetSubObjectGUIDB (método)</span><span class="sxs-lookup"><span data-stu-id="ebb3e-104">IAMTimelineObj::SetSubObjectGUIDB method</span></span>

> [!Note]  
> <span data-ttu-id="ebb3e-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="ebb3e-105">\[Deprecated.</span></span> <span data-ttu-id="ebb3e-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ebb3e-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ebb3e-107">El `SetSubObjectGUIDB` método especifica el GUID del subobjeto asociado a este objeto.</span><span class="sxs-lookup"><span data-stu-id="ebb3e-107">The `SetSubObjectGUIDB` method specifies the GUID of the subobject associated with this object.</span></span> <span data-ttu-id="ebb3e-108">Este método es equivalente a [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) , pero toma un valor **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="ebb3e-108">This method is equivalent to [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) but takes a **BSTR** value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebb3e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ebb3e-109">Syntax</span></span>


```C++
HRESULT SetSubObjectGUIDB(
   BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="ebb3e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ebb3e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebb3e-111">*newVal*</span><span class="sxs-lookup"><span data-stu-id="ebb3e-111">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="ebb3e-112">**BSTR** que representa el GUID del subobjeto.</span><span class="sxs-lookup"><span data-stu-id="ebb3e-112">**BSTR** representing the GUID of the subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebb3e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ebb3e-113">Return value</span></span>

<span data-ttu-id="ebb3e-114">Devuelve S \_ correcto si es correcto o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="ebb3e-114">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebb3e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ebb3e-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ebb3e-116">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="ebb3e-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ebb3e-117">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ebb3e-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ebb3e-118">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ebb3e-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ebb3e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebb3e-119">Requirements</span></span>



| <span data-ttu-id="ebb3e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebb3e-120">Requirement</span></span> | <span data-ttu-id="ebb3e-121">Value</span><span class="sxs-lookup"><span data-stu-id="ebb3e-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebb3e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ebb3e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ebb3e-123"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebb3e-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ebb3e-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ebb3e-124">Library</span></span><br/> | <dl> <span data-ttu-id="ebb3e-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ebb3e-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebb3e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ebb3e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebb3e-127">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="ebb3e-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="ebb3e-128">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="ebb3e-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




