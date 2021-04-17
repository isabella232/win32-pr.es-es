---
description: El método VTrackSwapPriorities cambia los niveles de prioridad de dos pistas.
ms.assetid: 87085060-5165-4c32-b5b0-895ae487e7ef
title: 'IAMTimelineComp:: VTrackSwapPriorities (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: df90fe3f4c481f454c6cc743f09de9538a2c892d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691082"
---
# <a name="iamtimelinecompvtrackswappriorities-method"></a><span data-ttu-id="4722a-103">IAMTimelineComp:: VTrackSwapPriorities (método)</span><span class="sxs-lookup"><span data-stu-id="4722a-103">IAMTimelineComp::VTrackSwapPriorities method</span></span>

> [!Note]  
> <span data-ttu-id="4722a-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="4722a-104">\[Deprecated.</span></span> <span data-ttu-id="4722a-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4722a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4722a-106">El `VTrackSwapPriorities` método cambia los niveles de prioridad de dos pistas.</span><span class="sxs-lookup"><span data-stu-id="4722a-106">The `VTrackSwapPriorities` method switches the priority levels of two tracks.</span></span>

<span data-ttu-id="4722a-107">Dado dos niveles de prioridad, este método cambia las pistas virtuales en esas prioridades.</span><span class="sxs-lookup"><span data-stu-id="4722a-107">Given two priority levels, this method switches the virtual tracks at those priorities.</span></span> <span data-ttu-id="4722a-108">Cuando el método devuelve, la pista que estaba en el primer nivel de prioridad ahora está en el segundo nivel de prioridad y viceversa.</span><span class="sxs-lookup"><span data-stu-id="4722a-108">When the method returns, the track that was at the first priority level is now at the second priority level, and vice versa.</span></span>

## <a name="syntax"></a><span data-ttu-id="4722a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4722a-109">Syntax</span></span>


```C++
HRESULT VTrackSwapPriorities(
   long VirtualTrackA,
   long VirtualTrackB
);
```



## <a name="parameters"></a><span data-ttu-id="4722a-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4722a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4722a-111">*VirtualTrackA*</span><span class="sxs-lookup"><span data-stu-id="4722a-111">*VirtualTrackA*</span></span> 
</dt> <dd>

<span data-ttu-id="4722a-112">Primer nivel de prioridad en el que se van a intercambiar las pistas virtuales.</span><span class="sxs-lookup"><span data-stu-id="4722a-112">First priority level at which to swap virtual tracks.</span></span>

</dd> <dt>

<span data-ttu-id="4722a-113">*VirtualTrackB*</span><span class="sxs-lookup"><span data-stu-id="4722a-113">*VirtualTrackB*</span></span> 
</dt> <dd>

<span data-ttu-id="4722a-114">Segundo nivel de prioridad en el que se van a intercambiar las pistas virtuales.</span><span class="sxs-lookup"><span data-stu-id="4722a-114">Second priority level at which to swap virtual tracks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4722a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4722a-115">Return value</span></span>

<span data-ttu-id="4722a-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4722a-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4722a-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4722a-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4722a-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4722a-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4722a-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="4722a-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4722a-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4722a-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4722a-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4722a-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4722a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4722a-122">Requirements</span></span>



| <span data-ttu-id="4722a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4722a-123">Requirement</span></span> | <span data-ttu-id="4722a-124">Value</span><span class="sxs-lookup"><span data-stu-id="4722a-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4722a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4722a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4722a-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="4722a-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4722a-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4722a-127">Library</span></span><br/> | <dl> <span data-ttu-id="4722a-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4722a-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4722a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="4722a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4722a-130">**Interfaz IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="4722a-130">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="4722a-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="4722a-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




