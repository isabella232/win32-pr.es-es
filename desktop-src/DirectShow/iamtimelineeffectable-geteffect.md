---
description: El método GetEffect recupera el efecto en el nivel de prioridad especificado.
ms.assetid: 8606c457-1c4d-4a20-b674-aaf82abeb451
title: 'IAMTimelineEffectable:: GetEffect (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.GetEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b7a769fca28ea1f8f698b23de7df6b7c15f05234
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681253"
---
# <a name="iamtimelineeffectablegeteffect-method"></a><span data-ttu-id="a9af5-103">IAMTimelineEffectable:: GetEffect (método)</span><span class="sxs-lookup"><span data-stu-id="a9af5-103">IAMTimelineEffectable::GetEffect method</span></span>

> [!Note]  
> <span data-ttu-id="a9af5-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="a9af5-104">\[Deprecated.</span></span> <span data-ttu-id="a9af5-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a9af5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a9af5-106">El método **GetEffect** recupera el efecto en el nivel de prioridad especificado.</span><span class="sxs-lookup"><span data-stu-id="a9af5-106">The **GetEffect** method retrieves the effect at the specified priority level.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9af5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9af5-107">Syntax</span></span>


```C++
HRESULT GetEffect(
  [out] IAMTimelineObj **ppFX,
        long           Which
);
```



## <a name="parameters"></a><span data-ttu-id="a9af5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a9af5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9af5-109">*ppFX* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a9af5-109">*ppFX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9af5-110">Recibe la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del efecto.</span><span class="sxs-lookup"><span data-stu-id="a9af5-110">Receives the effect's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="a9af5-111">*Cuales*</span><span class="sxs-lookup"><span data-stu-id="a9af5-111">*Which*</span></span> 
</dt> <dd>

<span data-ttu-id="a9af5-112">Nivel de prioridad del efecto que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="a9af5-112">Priority level of the effect to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9af5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a9af5-113">Return value</span></span>

<span data-ttu-id="a9af5-114">Devuelve un valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="a9af5-114">Returns an HRESULT value.</span></span> <span data-ttu-id="a9af5-115">Entre los valores posibles figuran los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a9af5-115">Possible values include the following:</span></span>



| <span data-ttu-id="a9af5-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a9af5-116">Return code</span></span>                                                                               | <span data-ttu-id="a9af5-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9af5-117">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="a9af5-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="a9af5-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="a9af5-119">Ningún efecto con la prioridad especificada.</span><span class="sxs-lookup"><span data-stu-id="a9af5-119">No effect at the specified priority,</span></span><br/> |
| <dl> <span data-ttu-id="a9af5-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a9af5-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="a9af5-121">Correcto.</span><span class="sxs-lookup"><span data-stu-id="a9af5-121">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="a9af5-122"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="a9af5-122"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="a9af5-123">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="a9af5-123">**NULL** pointer argument.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="a9af5-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9af5-124">Remarks</span></span>

<span data-ttu-id="a9af5-125">Si el método devuelve S \_ correcto, la interfaz **IAMTimelineObj** que devuelve tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="a9af5-125">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="a9af5-126">Asegúrese de liberar la interfaz cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="a9af5-126">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="a9af5-127">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="a9af5-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a9af5-128">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a9af5-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a9af5-129">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a9af5-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a9af5-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9af5-130">Requirements</span></span>



| <span data-ttu-id="a9af5-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9af5-131">Requirement</span></span> | <span data-ttu-id="a9af5-132">Value</span><span class="sxs-lookup"><span data-stu-id="a9af5-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9af5-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9af5-133">Header</span></span><br/>  | <dl> <span data-ttu-id="a9af5-134"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9af5-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a9af5-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a9af5-135">Library</span></span><br/> | <dl> <span data-ttu-id="a9af5-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9af5-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9af5-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9af5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9af5-138">**Interfaz IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="a9af5-138">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="a9af5-139">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="a9af5-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




