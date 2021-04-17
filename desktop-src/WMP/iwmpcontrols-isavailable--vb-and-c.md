---
title: IWMPControls. isAvailable (VB y C)
description: La propiedad isAvailable (el \_ método get isavailable en C \) obtiene un valor que indica si un tipo de información especificado está disponible o se puede realizar una acción especificada.
ms.assetid: 00812d5c-513e-49d5-93ba-750b81a852dd
keywords:
- IWMPControls. isAvailable (VB y C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPControls.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0d5d9ffcd6cad6eefb7cdff25fd2cf34b76ccc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690425"
---
# <a name="iwmpcontrolsisavailable-vb-and-c"></a><span data-ttu-id="cce23-104">IWMPControls. isAvailable (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="cce23-104">IWMPControls.isAvailable (VB and C#)</span></span>

<span data-ttu-id="cce23-105">La propiedad **isavailable** (el método **Get \_ isavailable** en C#) obtiene un valor que indica si un tipo de información especificado está disponible o se puede realizar una acción especificada.</span><span class="sxs-lookup"><span data-stu-id="cce23-105">The **isAvailable** property (the **get\_isAvailable** method in C#) gets a value indicating whether a specified type of information is available or a specified action can be performed.</span></span>


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
bool get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a><span data-ttu-id="cce23-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cce23-106">Parameters</span></span>

<span data-ttu-id="cce23-107">*bstrItem*</span><span class="sxs-lookup"><span data-stu-id="cce23-107">*bstrItem*</span></span>

<span data-ttu-id="cce23-108">System. String que es uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="cce23-108">A System.String that is one of the following values.</span></span>



| <span data-ttu-id="cce23-109">Value</span><span class="sxs-lookup"><span data-stu-id="cce23-109">Value</span></span>           | <span data-ttu-id="cce23-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="cce23-110">Description</span></span>                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cce23-111">currentItem</span><span class="sxs-lookup"><span data-stu-id="cce23-111">currentItem</span></span>     | <span data-ttu-id="cce23-112">Detecta si el usuario puede establecer la propiedad **IWMPControls. CurrentItem** .</span><span class="sxs-lookup"><span data-stu-id="cce23-112">Discovers whether the user can set the **IWMPControls.currentItem** property.</span></span>                                                                                     |
| <span data-ttu-id="cce23-113">currentMarker</span><span class="sxs-lookup"><span data-stu-id="cce23-113">currentMarker</span></span>   | <span data-ttu-id="cce23-114">Detecta si el usuario puede buscar un marcador específico.</span><span class="sxs-lookup"><span data-stu-id="cce23-114">Discovers whether the user can seek to a specific marker.</span></span>                                                                                                         |
| <span data-ttu-id="cce23-115">currentPosition</span><span class="sxs-lookup"><span data-stu-id="cce23-115">currentPosition</span></span> | <span data-ttu-id="cce23-116">Detecta si el usuario puede buscar una posición específica en el archivo.</span><span class="sxs-lookup"><span data-stu-id="cce23-116">Discovers whether the user can seek to a specific position in the file.</span></span> <span data-ttu-id="cce23-117">Algunos archivos no admiten búsquedas.</span><span class="sxs-lookup"><span data-stu-id="cce23-117">Some files do not support seeking.</span></span>                                                        |
| <span data-ttu-id="cce23-118">fastForward</span><span class="sxs-lookup"><span data-stu-id="cce23-118">fastForward</span></span>     | <span data-ttu-id="cce23-119">Detecta si el archivo admite el reenvío rápido y si se puede invocar la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="cce23-119">Discovers whether the file supports fast forwarding and whether that functionality can be invoked.</span></span> <span data-ttu-id="cce23-120">Muchos tipos de archivo (y secuencias en directo) no admiten fastForward.</span><span class="sxs-lookup"><span data-stu-id="cce23-120">Many file types (and live streams) do not support fastForward.</span></span> |
| <span data-ttu-id="cce23-121">fastReverse</span><span class="sxs-lookup"><span data-stu-id="cce23-121">fastReverse</span></span>     | <span data-ttu-id="cce23-122">Detecta si el archivo admite fastReverse y si se puede invocar esa funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="cce23-122">Discovers whether the file supports fastReverse and whether that functionality can be invoked.</span></span> <span data-ttu-id="cce23-123">Muchos tipos de archivo (y secuencias en directo) no admiten fastReverse.</span><span class="sxs-lookup"><span data-stu-id="cce23-123">Many file types (and live streams) do not support fastReverse.</span></span>     |
| <span data-ttu-id="cce23-124">Siguiente</span><span class="sxs-lookup"><span data-stu-id="cce23-124">next</span></span>            | <span data-ttu-id="cce23-125">Detecta si el usuario puede buscar la siguiente entrada en una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="cce23-125">Discovers whether the user can seek to the next entry in a playlist.</span></span>                                                                                              |
| <span data-ttu-id="cce23-126">pause</span><span class="sxs-lookup"><span data-stu-id="cce23-126">pause</span></span>           | <span data-ttu-id="cce23-127">Detecta si el método **IWMPControls. PAUSE** está disponible.</span><span class="sxs-lookup"><span data-stu-id="cce23-127">Discovers whether the **IWMPControls.pause** method is available.</span></span>                                                                                                 |
| <span data-ttu-id="cce23-128">reproducción</span><span class="sxs-lookup"><span data-stu-id="cce23-128">play</span></span>            | <span data-ttu-id="cce23-129">Detecta si el método **IWMPControls. Play** está disponible.</span><span class="sxs-lookup"><span data-stu-id="cce23-129">Discovers whether the **IWMPControls.play** method is available.</span></span>                                                                                                  |
| <span data-ttu-id="cce23-130">previous</span><span class="sxs-lookup"><span data-stu-id="cce23-130">previous</span></span>        | <span data-ttu-id="cce23-131">Detecta si el usuario puede buscar la entrada anterior en una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="cce23-131">Discovers whether the user can seek to the previous entry in a playlist.</span></span>                                                                                          |
| <span data-ttu-id="cce23-132">paso</span><span class="sxs-lookup"><span data-stu-id="cce23-132">step</span></span>            | <span data-ttu-id="cce23-133">Detecta si el método **IWMPControls2. Step** está disponible durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="cce23-133">Discovers whether the **IWMPControls2.step** method is available during playback.</span></span>                                                                                 |
| <span data-ttu-id="cce23-134">stop</span><span class="sxs-lookup"><span data-stu-id="cce23-134">stop</span></span>            | <span data-ttu-id="cce23-135">Detecta si el método **IWMPControls. Stop** está disponible.</span><span class="sxs-lookup"><span data-stu-id="cce23-135">Discovers whether the **IWMPControls.stop** method is available.</span></span>                                                                                                  |



 

## <a name="property-value"></a><span data-ttu-id="cce23-136">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="cce23-136">Property Value</span></span>

<span data-ttu-id="cce23-137">**System.Boolean**</span><span class="sxs-lookup"><span data-stu-id="cce23-137">**System.Boolean**</span></span>

<span data-ttu-id="cce23-138">**System. Boolean** que indica si un tipo de información especificado está disponible o se puede realizar una acción especificada.</span><span class="sxs-lookup"><span data-stu-id="cce23-138">A **System.Boolean** that indicates whether a specified type of information is available or a specified action can be performed.</span></span>

## <a name="remarks"></a><span data-ttu-id="cce23-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cce23-139">Remarks</span></span>

<span data-ttu-id="cce23-140">**IWMPControls. isavailable** es una propiedad de Visual Basic que toma un parámetro.</span><span class="sxs-lookup"><span data-stu-id="cce23-140">**IWMPControls.isAvailable** is a property in Visual Basic that takes a parameter.</span></span> <span data-ttu-id="cce23-141">En C#, se hace referencia a él como el método **IWMPControls. Get \_ isavailable** .</span><span class="sxs-lookup"><span data-stu-id="cce23-141">In C# it is referred to as the **IWMPControls.get\_isAvailable** method.</span></span>

## <a name="examples"></a><span data-ttu-id="cce23-142">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cce23-142">Examples</span></span>

<span data-ttu-id="cce23-143">En el ejemplo siguiente se usa la propiedad **isavailable** (el método **Get \_ isavailable** en C#) para comprobar que el elemento multimedia actual admite la propiedad **currentPosition** .</span><span class="sxs-lookup"><span data-stu-id="cce23-143">The following example uses the **isAvailable** property (the **get\_isAvailable** method in C#) to verify that the current media item supports the **currentPosition** property.</span></span> <span data-ttu-id="cce23-144">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="cce23-144">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// If the currentPosition property is supported, seek to position 0.
if (player.Ctlcontrols.get_isAvailable("currentPosition"))
{
    player.Ctlcontrols.currentPosition = 0;
}
```


```VB

' If the currentPosition property is supported, seek to position 0.
If (player.Ctlcontrols.isAvailable(&quot;currentPosition&quot;)) Then

    player.Ctlcontrols.currentPosition = 0

End If
```





## <a name="requirements"></a><span data-ttu-id="cce23-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cce23-145">Requirements</span></span>



| <span data-ttu-id="cce23-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="cce23-146">Requirement</span></span> | <span data-ttu-id="cce23-147">Value</span><span class="sxs-lookup"><span data-stu-id="cce23-147">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cce23-148">Versión</span><span class="sxs-lookup"><span data-stu-id="cce23-148">Version</span></span><br/>   | <span data-ttu-id="cce23-149">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="cce23-149">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="cce23-150">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cce23-150">Namespace</span></span><br/> | <span data-ttu-id="cce23-151">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="cce23-151">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="cce23-152">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="cce23-152">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cce23-153"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cce23-153"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cce23-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="cce23-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cce23-155">**Interfaz IWMPControls (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="cce23-155">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cce23-156">**IWMPControls. currentItem (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="cce23-156">**IWMPControls.currentItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cce23-157">**IWMPControls. PAUSE (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="cce23-157">**IWMPControls.pause (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cce23-158">**IWMPControls. Play (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="cce23-158">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cce23-159">**IWMPControls. STOP (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="cce23-159">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cce23-160">**IWMPControls2. Step (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="cce23-160">**IWMPControls2.step (VB and C#)**</span></span>](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md)
</dt> </dl>

 

 





