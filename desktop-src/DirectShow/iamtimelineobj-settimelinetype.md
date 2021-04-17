---
description: 'No se admite. Llame al método IAMTimeline:: CreateEmptyNode para crear un nuevo objeto Timeline. Una vez creado un objeto, no se puede cambiar su tipo.'
ms.assetid: 127b7435-84b0-46c4-b072-bb8eb54b6a4f
title: 'IAMTimelineObj:: SetTimelineType (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetTimelineType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a63031968a2dfb43d98f9b7f59bd2d9051042732
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690716"
---
# <a name="iamtimelineobjsettimelinetype-method"></a><span data-ttu-id="3791c-105">IAMTimelineObj:: SetTimelineType (método)</span><span class="sxs-lookup"><span data-stu-id="3791c-105">IAMTimelineObj::SetTimelineType method</span></span>

> [!Note]  
> <span data-ttu-id="3791c-106">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="3791c-106">\[Deprecated.</span></span> <span data-ttu-id="3791c-107">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3791c-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3791c-108">No se admite.</span><span class="sxs-lookup"><span data-stu-id="3791c-108">Not supported.</span></span> <span data-ttu-id="3791c-109">Llame al método [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) para crear un nuevo objeto Timeline.</span><span class="sxs-lookup"><span data-stu-id="3791c-109">Call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method to create a new timeline object.</span></span> <span data-ttu-id="3791c-110">Una vez creado un objeto, no se puede cambiar su tipo.</span><span class="sxs-lookup"><span data-stu-id="3791c-110">Once an object is created, you cannot change its type.</span></span>

## <a name="syntax"></a><span data-ttu-id="3791c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3791c-111">Syntax</span></span>


```C++
HRESULT SetTimelineType(
   TIMELINE_MAJOR_TYPE newVal
);
```



## <a name="parameters"></a><span data-ttu-id="3791c-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3791c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3791c-113">*newVal*</span><span class="sxs-lookup"><span data-stu-id="3791c-113">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="3791c-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="3791c-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3791c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3791c-115">Return value</span></span>

<span data-ttu-id="3791c-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="3791c-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3791c-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3791c-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3791c-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3791c-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3791c-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="3791c-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3791c-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3791c-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3791c-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3791c-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3791c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3791c-122">Requirements</span></span>



| <span data-ttu-id="3791c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3791c-123">Requirement</span></span> | <span data-ttu-id="3791c-124">Value</span><span class="sxs-lookup"><span data-stu-id="3791c-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3791c-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3791c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3791c-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="3791c-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3791c-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3791c-127">Library</span></span><br/> | <dl> <span data-ttu-id="3791c-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3791c-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3791c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="3791c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3791c-130">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="3791c-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




