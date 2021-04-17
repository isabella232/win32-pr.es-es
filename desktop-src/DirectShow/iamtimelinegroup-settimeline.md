---
description: 'No se admite. Llame al método IAMTimeline:: AddGroup en su lugar.'
ms.assetid: dd671fa5-ed5a-46e2-b4bd-a37f0e7458ca
title: 'IAMTimelineGroup:: SetTimeline (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 166d65f5ae9a14f58ed7b20763ab5e4a136df598
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680872"
---
# <a name="iamtimelinegroupsettimeline-method"></a><span data-ttu-id="a1df4-104">IAMTimelineGroup:: SetTimeline (método)</span><span class="sxs-lookup"><span data-stu-id="a1df4-104">IAMTimelineGroup::SetTimeline method</span></span>

> [!Note]  
> <span data-ttu-id="a1df4-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="a1df4-105">\[Deprecated.</span></span> <span data-ttu-id="a1df4-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a1df4-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a1df4-107">No se admite.</span><span class="sxs-lookup"><span data-stu-id="a1df4-107">Not supported.</span></span> <span data-ttu-id="a1df4-108">Llame al método [**IAMTimeline:: addgroup**](iamtimeline-addgroup.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a1df4-108">Call the [**IAMTimeline::AddGroup**](iamtimeline-addgroup.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1df4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1df4-109">Syntax</span></span>


```C++
HRESULT SetTimeline(
   IAMTimeline *pTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="a1df4-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1df4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1df4-111">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="a1df4-111">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="a1df4-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a1df4-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1df4-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1df4-113">Return value</span></span>

<span data-ttu-id="a1df4-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a1df4-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a1df4-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a1df4-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1df4-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1df4-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a1df4-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="a1df4-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a1df4-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a1df4-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a1df4-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a1df4-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a1df4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1df4-120">Requirements</span></span>



| <span data-ttu-id="a1df4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1df4-121">Requirement</span></span> | <span data-ttu-id="a1df4-122">Value</span><span class="sxs-lookup"><span data-stu-id="a1df4-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1df4-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1df4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a1df4-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1df4-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a1df4-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1df4-125">Library</span></span><br/> | <dl> <span data-ttu-id="a1df4-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1df4-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1df4-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1df4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1df4-128">**Interfaz IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="a1df4-128">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> </dl>

 

 




