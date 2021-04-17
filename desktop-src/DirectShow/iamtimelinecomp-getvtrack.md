---
description: El método GetVTrack recupera la pista virtual con la prioridad especificada.
ms.assetid: e866064b-a511-4f0c-8cb1-62e4f1c42347
title: 'IAMTimelineComp:: GetVTrack (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 06c205f700cbdb98fdc5f45bdd2ca7727e2456f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680971"
---
# <a name="iamtimelinecompgetvtrack-method"></a><span data-ttu-id="96eaa-103">IAMTimelineComp:: GetVTrack (método)</span><span class="sxs-lookup"><span data-stu-id="96eaa-103">IAMTimelineComp::GetVTrack method</span></span>

> [!Note]  
> <span data-ttu-id="96eaa-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="96eaa-104">\[Deprecated.</span></span> <span data-ttu-id="96eaa-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="96eaa-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="96eaa-106">El `GetVTrack` método recupera la pista virtual con la prioridad especificada.</span><span class="sxs-lookup"><span data-stu-id="96eaa-106">The `GetVTrack` method retrieves the virtual track at the specified priority.</span></span>

## <a name="syntax"></a><span data-ttu-id="96eaa-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96eaa-107">Syntax</span></span>


```C++
HRESULT GetVTrack(
  [out] IAMTimelineObj **ppVirtualTrack,
        long           Which
);
```



## <a name="parameters"></a><span data-ttu-id="96eaa-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96eaa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96eaa-109">*ppVirtualTrack* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="96eaa-109">*ppVirtualTrack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96eaa-110">Recibe la interfaz [**IAMTimelineObj**](iamtimelineobj.md) de la pista virtual.</span><span class="sxs-lookup"><span data-stu-id="96eaa-110">Receives the virtual track's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="96eaa-111">*Cuales*</span><span class="sxs-lookup"><span data-stu-id="96eaa-111">*Which*</span></span> 
</dt> <dd>

<span data-ttu-id="96eaa-112">Prioridad de la pista virtual que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="96eaa-112">Priority of the virtual track to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96eaa-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96eaa-113">Return value</span></span>

<span data-ttu-id="96eaa-114">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="96eaa-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="96eaa-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="96eaa-115">Return code</span></span>                                                                                  | <span data-ttu-id="96eaa-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="96eaa-116">Description</span></span>                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="96eaa-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="96eaa-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="96eaa-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="96eaa-118">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="96eaa-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="96eaa-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="96eaa-120">No hay ninguna pista virtual con la prioridad especificada.</span><span class="sxs-lookup"><span data-stu-id="96eaa-120">No virtual track with the specified priority.</span></span><br/> |
| <dl> <span data-ttu-id="96eaa-121"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="96eaa-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="96eaa-122">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="96eaa-122">**NULL** pointer argument.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="96eaa-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96eaa-123">Remarks</span></span>

<span data-ttu-id="96eaa-124">Si el método se ejecuta correctamente, la interfaz **IAMTimelineObj** que devuelve tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="96eaa-124">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="96eaa-125">Asegúrese de liberar la interfaz cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="96eaa-125">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="96eaa-126">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="96eaa-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="96eaa-127">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="96eaa-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="96eaa-128">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="96eaa-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="96eaa-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96eaa-129">Requirements</span></span>



| <span data-ttu-id="96eaa-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="96eaa-130">Requirement</span></span> | <span data-ttu-id="96eaa-131">Value</span><span class="sxs-lookup"><span data-stu-id="96eaa-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96eaa-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96eaa-132">Header</span></span><br/>  | <dl> <span data-ttu-id="96eaa-133"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="96eaa-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="96eaa-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="96eaa-134">Library</span></span><br/> | <dl> <span data-ttu-id="96eaa-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96eaa-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96eaa-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="96eaa-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96eaa-137">**Interfaz IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="96eaa-137">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="96eaa-138">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="96eaa-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




