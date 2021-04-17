---
description: El método SetDynamicReconnectLevel establece el nivel de reconexión dinámica durante la representación.
ms.assetid: 092f3464-84a2-48b0-9647-66fe27e9706d
title: 'IRenderEngine:: SetDynamicReconnectLevel (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetDynamicReconnectLevel
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ae02fb6158b58cd5785aa7df539651acfbea5db8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680713"
---
# <a name="irenderenginesetdynamicreconnectlevel-method"></a><span data-ttu-id="41fa3-103">IRenderEngine:: SetDynamicReconnectLevel (método)</span><span class="sxs-lookup"><span data-stu-id="41fa3-103">IRenderEngine::SetDynamicReconnectLevel method</span></span>

> [!Note]  
> <span data-ttu-id="41fa3-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="41fa3-104">\[Deprecated.</span></span> <span data-ttu-id="41fa3-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="41fa3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="41fa3-106">El `SetDynamicReconnectLevel` método establece el nivel de reconexión dinámica durante la representación.</span><span class="sxs-lookup"><span data-stu-id="41fa3-106">The `SetDynamicReconnectLevel` method sets the level of dynamic reconnection during rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="41fa3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41fa3-107">Syntax</span></span>


```C++
HRESULT SetDynamicReconnectLevel(
   DWORD Level
);
```



## <a name="parameters"></a><span data-ttu-id="41fa3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="41fa3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41fa3-109">*Level*</span><span class="sxs-lookup"><span data-stu-id="41fa3-109">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="41fa3-110">Combinación de [**marcas de reconexión dinámica**](dynamic-reconnection-flags.md), que especifica el nivel de reconexión dinámica.</span><span class="sxs-lookup"><span data-stu-id="41fa3-110">Combination of [**Dynamic Reconnection Flags**](dynamic-reconnection-flags.md), specifying the level of dynamic reconnection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41fa3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41fa3-111">Return value</span></span>

<span data-ttu-id="41fa3-112">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="41fa3-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="41fa3-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="41fa3-113">Return code</span></span>                                                                               | <span data-ttu-id="41fa3-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="41fa3-114">Description</span></span>                 |
|-------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="41fa3-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="41fa3-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="41fa3-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="41fa3-116">Success.</span></span><br/>         |
| <dl> <span data-ttu-id="41fa3-117"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="41fa3-117"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="41fa3-118">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="41fa3-118">Not implemented.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="41fa3-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41fa3-119">Remarks</span></span>

<span data-ttu-id="41fa3-120">De forma predeterminada, el motor de representación básico carga todos los orígenes antes de representar un proyecto.</span><span class="sxs-lookup"><span data-stu-id="41fa3-120">By default, the basic render engine loads every source before rendering a project.</span></span> <span data-ttu-id="41fa3-121">Esto puede dar lugar a un tiempo de inicio largo.</span><span class="sxs-lookup"><span data-stu-id="41fa3-121">This can result in a long start-up time.</span></span> <span data-ttu-id="41fa3-122">Con la reconexión dinámica, los orígenes se cargan solo cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="41fa3-122">With dynamic reconnection, sources are loaded only when needed.</span></span> <span data-ttu-id="41fa3-123">Esto puede acortar el tiempo de inicio, pero podría interferir con la reproducción fluida.</span><span class="sxs-lookup"><span data-stu-id="41fa3-123">This can shorten the start-up time, but possibly interfere with smooth playback.</span></span> <span data-ttu-id="41fa3-124">Por lo general, cuanto más clips de origen usa un proyecto, más se puede beneficiar de la reconexión dinámica.</span><span class="sxs-lookup"><span data-stu-id="41fa3-124">Generally, the more source clips that a project uses, the more you might benefit from dynamic reconnection.</span></span>

<span data-ttu-id="41fa3-125">El motor de representación inteligente no implementa este método.</span><span class="sxs-lookup"><span data-stu-id="41fa3-125">The smart render engine does not implement this method.</span></span>

> [!Note]  
> <span data-ttu-id="41fa3-126">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="41fa3-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="41fa3-127">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="41fa3-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="41fa3-128">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="41fa3-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="41fa3-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41fa3-129">Requirements</span></span>



| <span data-ttu-id="41fa3-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="41fa3-130">Requirement</span></span> | <span data-ttu-id="41fa3-131">Value</span><span class="sxs-lookup"><span data-stu-id="41fa3-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41fa3-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41fa3-132">Header</span></span><br/>  | <dl> <span data-ttu-id="41fa3-133"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="41fa3-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="41fa3-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="41fa3-134">Library</span></span><br/> | <dl> <span data-ttu-id="41fa3-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41fa3-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41fa3-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="41fa3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41fa3-137">**Interfaz IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="41fa3-137">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="41fa3-138">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="41fa3-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




