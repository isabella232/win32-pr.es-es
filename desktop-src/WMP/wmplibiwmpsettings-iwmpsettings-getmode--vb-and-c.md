---
title: IWMPSettings getMode, método
description: El método getMode devuelve un valor que indica si el modo de bucle o el modo de orden aleatorio está activo.
ms.assetid: a2e4bf74-017f-4c54-a3a1-a03b75a87a59
keywords:
- método getMode de Windows Media Player
- método getMode Windows Media Player, interfaz IWMPSettings
- Interfaz IWMPSettings Windows Media Player, método getMode
topic_type:
- apiref
api_name:
- IWMPSettings.getMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229cacf629410f958a062615cd5feb22be2ab0d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718757"
---
# <a name="iwmpsettingsgetmode-method"></a><span data-ttu-id="d99a2-106">IWMPSettings:: getMode (método)</span><span class="sxs-lookup"><span data-stu-id="d99a2-106">IWMPSettings::getMode method</span></span>

<span data-ttu-id="d99a2-107">El método **getMode** devuelve un valor que indica si el modo de bucle o el modo de orden aleatorio está activo.</span><span class="sxs-lookup"><span data-stu-id="d99a2-107">The **getMode** method returns a value indicating whether loop mode or shuffle mode is active.</span></span>

## <a name="syntax"></a><span data-ttu-id="d99a2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d99a2-108">Syntax</span></span>


```CSharp
public System.Boolean getMode(
  System.String bstrMode
);
```


```VB

Public Function getMode( _
  ByVal bstrMode As System.String _
) As System.Boolean
Implements IWMPSettings.getMode
```





## <a name="parameters"></a><span data-ttu-id="d99a2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d99a2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d99a2-110">*bstrMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d99a2-110">*bstrMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d99a2-111">**System. String** que es uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d99a2-111">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="d99a2-112">Value</span><span class="sxs-lookup"><span data-stu-id="d99a2-112">Value</span></span>      | <span data-ttu-id="d99a2-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="d99a2-113">Description</span></span>                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d99a2-114">autoRewind</span><span class="sxs-lookup"><span data-stu-id="d99a2-114">autoRewind</span></span> | <span data-ttu-id="d99a2-115">Las pistas se reinician desde el principio después de la reproducción hasta el final.</span><span class="sxs-lookup"><span data-stu-id="d99a2-115">Tracks are restarted from the beginning after playing to the end.</span></span>                                |
| <span data-ttu-id="d99a2-116">bucle</span><span class="sxs-lookup"><span data-stu-id="d99a2-116">loop</span></span>       | <span data-ttu-id="d99a2-117">La secuencia de pistas se repite.</span><span class="sxs-lookup"><span data-stu-id="d99a2-117">The sequence of tracks repeats itself.</span></span>                                                           |
| <span data-ttu-id="d99a2-118">showFrame</span><span class="sxs-lookup"><span data-stu-id="d99a2-118">showFrame</span></span>  | <span data-ttu-id="d99a2-119">El fotograma clave más cercano se muestra cuando no se reproduce.</span><span class="sxs-lookup"><span data-stu-id="d99a2-119">The nearest key frame is displayed when not playing.</span></span> <span data-ttu-id="d99a2-120">Este modo no es relevante para las pistas de audio.</span><span class="sxs-lookup"><span data-stu-id="d99a2-120">This mode is not relevant for audio tracks.</span></span> |
| <span data-ttu-id="d99a2-121">shuffle</span><span class="sxs-lookup"><span data-stu-id="d99a2-121">shuffle</span></span>    | <span data-ttu-id="d99a2-122">Las pistas se reproducen en orden aleatorio.</span><span class="sxs-lookup"><span data-stu-id="d99a2-122">Tracks are played in random order.</span></span>                                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d99a2-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d99a2-123">Return value</span></span>

<span data-ttu-id="d99a2-124">Un valor **System. Boolean** que indica si el modo especificado está activo.</span><span class="sxs-lookup"><span data-stu-id="d99a2-124">A **System.Boolean** value indicating whether the specified mode is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="d99a2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d99a2-125">Requirements</span></span>



| <span data-ttu-id="d99a2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d99a2-126">Requirement</span></span> | <span data-ttu-id="d99a2-127">Value</span><span class="sxs-lookup"><span data-stu-id="d99a2-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d99a2-128">Versión</span><span class="sxs-lookup"><span data-stu-id="d99a2-128">Version</span></span><br/>   | <span data-ttu-id="d99a2-129">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="d99a2-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d99a2-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d99a2-130">Namespace</span></span><br/> | <span data-ttu-id="d99a2-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d99a2-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d99a2-132">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="d99a2-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d99a2-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d99a2-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d99a2-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="d99a2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d99a2-135">**Interfaz IWMPSettings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d99a2-135">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d99a2-136">**IWMPSettings. setMode (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d99a2-136">**IWMPSettings.setMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





