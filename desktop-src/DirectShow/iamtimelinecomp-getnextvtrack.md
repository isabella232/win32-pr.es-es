---
description: El método GetNextVTrack recupera la siguiente pista virtual después de una pista virtual especificada.
ms.assetid: c43e6b16-a3e4-4407-b48d-b04c4bb66688
title: 'IAMTimelineComp:: GetNextVTrack (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetNextVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0e5a4500c2b53703a13b509f112453e65c954f96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680974"
---
# <a name="iamtimelinecompgetnextvtrack-method"></a><span data-ttu-id="71367-103">IAMTimelineComp:: GetNextVTrack (método)</span><span class="sxs-lookup"><span data-stu-id="71367-103">IAMTimelineComp::GetNextVTrack method</span></span>

> [!Note]  
> <span data-ttu-id="71367-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="71367-104">\[Deprecated.</span></span> <span data-ttu-id="71367-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="71367-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="71367-106">El `GetNextVTrack` método recupera la siguiente pista virtual después de una pista virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="71367-106">The `GetNextVTrack` method retrieves the next virtual track after a specified virtual track.</span></span>

## <a name="syntax"></a><span data-ttu-id="71367-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71367-107">Syntax</span></span>


```C++
HRESULT GetNextVTrack(
        IAMTimelineObj *pVirtualTrack,
  [out] IAMTimelineObj **ppNextVirtualTrack
);
```



## <a name="parameters"></a><span data-ttu-id="71367-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71367-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71367-109">*pVirtualTrack*</span><span class="sxs-lookup"><span data-stu-id="71367-109">*pVirtualTrack*</span></span> 
</dt> <dd>

<span data-ttu-id="71367-110">Puntero a la pista virtual anterior o **null** para recuperar la primera pista virtual de la composición.</span><span class="sxs-lookup"><span data-stu-id="71367-110">Pointer to the previous virtual track, or **NULL** to retrieve the first virtual track in the composition.</span></span>

</dd> <dt>

<span data-ttu-id="71367-111">*ppNextVirtualTrack* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="71367-111">*ppNextVirtualTrack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71367-112">Recibe un puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) de la siguiente pista virtual, en orden de prioridad.</span><span class="sxs-lookup"><span data-stu-id="71367-112">Receives a pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the next virtual track, in order of priority.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71367-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71367-113">Return value</span></span>

<span data-ttu-id="71367-114">Devuelve S \_ OK si el método recupera una pista virtual o s \_ false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="71367-114">Returns S\_OK if the method retrieves a virtual track, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="71367-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71367-115">Remarks</span></span>

<span data-ttu-id="71367-116">Si el método se ejecuta correctamente, la interfaz **IAMTimelineObj** que devuelve tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="71367-116">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="71367-117">Asegúrese de liberar la interfaz cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="71367-117">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="71367-118">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="71367-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="71367-119">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="71367-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="71367-120">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="71367-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="71367-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71367-121">Requirements</span></span>



| <span data-ttu-id="71367-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="71367-122">Requirement</span></span> | <span data-ttu-id="71367-123">Value</span><span class="sxs-lookup"><span data-stu-id="71367-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71367-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71367-124">Header</span></span><br/>  | <dl> <span data-ttu-id="71367-125"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="71367-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="71367-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="71367-126">Library</span></span><br/> | <dl> <span data-ttu-id="71367-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71367-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71367-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="71367-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71367-129">**Interfaz IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="71367-129">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="71367-130">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="71367-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




