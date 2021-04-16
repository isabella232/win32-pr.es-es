---
title: IWMPDVD. isAvailable (VB y C)
description: La propiedad isAvailable (el \_ método get isavailable en C \) obtiene un valor que indica si un tipo de información especificado está disponible o se puede realizar una acción especificada.
ms.assetid: 55690783-df2f-473d-a6f2-a4907b7e8a78
keywords:
- IWMPDVD. isAvailable (VB y C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPDVD.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e3409da619f337b61606baaf546cebbb438087c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690688"
---
# <a name="iwmpdvdisavailable-vb-and-c"></a><span data-ttu-id="383f7-104">IWMPDVD. isAvailable (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="383f7-104">IWMPDVD.isAvailable (VB and C#)</span></span>

<span data-ttu-id="383f7-105">La propiedad **isavailable** (el método **Get \_ isavailable** en C#) obtiene un valor que indica si un tipo de información especificado está disponible o se puede realizar una acción especificada.</span><span class="sxs-lookup"><span data-stu-id="383f7-105">The **isAvailable** property (the **get\_isAvailable** method in C#) gets a value that indicates whether a specified type of information is available or a specified action can be performed.</span></span>


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
)
```



## <a name="parameters"></a><span data-ttu-id="383f7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="383f7-106">Parameters</span></span>

<span data-ttu-id="383f7-107">*bstrItem*</span><span class="sxs-lookup"><span data-stu-id="383f7-107">*bstrItem*</span></span>

<span data-ttu-id="383f7-108">System. String que es uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="383f7-108">A System.String that is one of the following values.</span></span>



| <span data-ttu-id="383f7-109">Value</span><span class="sxs-lookup"><span data-stu-id="383f7-109">Value</span></span>      | <span data-ttu-id="383f7-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="383f7-110">Description</span></span>                                                                                   |
|------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="383f7-111">atrás</span><span class="sxs-lookup"><span data-stu-id="383f7-111">back</span></span>       | <span data-ttu-id="383f7-112">Detecta si el método **IWMPDVD. back** está disponible.</span><span class="sxs-lookup"><span data-stu-id="383f7-112">Discovers whether the **IWMPDVD.back** method is available.</span></span>                                   |
| <span data-ttu-id="383f7-113">discos</span><span class="sxs-lookup"><span data-stu-id="383f7-113">dvd</span></span>        | <span data-ttu-id="383f7-114">Detecta si el DVD está cargado.</span><span class="sxs-lookup"><span data-stu-id="383f7-114">Discovers whether the DVD is loaded.</span></span>                                                          |
| <span data-ttu-id="383f7-115">dvdDecoder</span><span class="sxs-lookup"><span data-stu-id="383f7-115">dvdDecoder</span></span> | <span data-ttu-id="383f7-116">Detecta si el descodificador de DVD está instalado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="383f7-116">Discovers whether the DVD decoder is installed on system.</span></span>                                     |
| <span data-ttu-id="383f7-117">resume</span><span class="sxs-lookup"><span data-stu-id="383f7-117">resume</span></span>     | <span data-ttu-id="383f7-118">Detecta si el método **IWMPDVD. resume** está disponible.</span><span class="sxs-lookup"><span data-stu-id="383f7-118">Discovers whether the **IWMPDVD.resume** method is available.</span></span>                                 |
| <span data-ttu-id="383f7-119">titleMenu</span><span class="sxs-lookup"><span data-stu-id="383f7-119">titleMenu</span></span>  | <span data-ttu-id="383f7-120">Detecta si el método **IWMPDVD. titleMenu** está disponible.</span><span class="sxs-lookup"><span data-stu-id="383f7-120">Discovers whether the **IWMPDVD.titleMenu** method is available.</span></span>                              |
| <span data-ttu-id="383f7-121">Menú de menús</span><span class="sxs-lookup"><span data-stu-id="383f7-121">topMenu</span></span>    | <span data-ttu-id="383f7-122">Detecta si el método **IWMPDVD. webmenu** está disponible.</span><span class="sxs-lookup"><span data-stu-id="383f7-122">Discovers whether the **IWMPDVD.topMenu** method is available.</span></span> <span data-ttu-id="383f7-123">Normalmente denominado menú raíz.</span><span class="sxs-lookup"><span data-stu-id="383f7-123">Commonly called the root menu.</span></span> |



 

## <a name="property-value"></a><span data-ttu-id="383f7-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="383f7-124">Property Value</span></span>

<span data-ttu-id="383f7-125">**System.Boolean**</span><span class="sxs-lookup"><span data-stu-id="383f7-125">**System.Boolean**</span></span>

<span data-ttu-id="383f7-126">**System. Boolean** que indica si un tipo de información especificado está disponible o se puede realizar una acción especificada.</span><span class="sxs-lookup"><span data-stu-id="383f7-126">A **System.Boolean** that indicates whether a specified type of information is available or a specified action can be performed.</span></span>

## <a name="remarks"></a><span data-ttu-id="383f7-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="383f7-127">Remarks</span></span>

<span data-ttu-id="383f7-128">Las características de DVD de Windows Media Player no funcionarán en equipos que no tengan instalado un descodificador de DVD.</span><span class="sxs-lookup"><span data-stu-id="383f7-128">The DVD features of Windows Media Player will not work on computers that do not have a DVD decoder installed.</span></span> <span data-ttu-id="383f7-129">Puede determinar si un descodificador está disponible llamando a la propiedad **isavailable** (el método **Get \_ isavailable** en C#) y pasando el valor **System. String** "dvdDecoder".</span><span class="sxs-lookup"><span data-stu-id="383f7-129">You can determine whether a decoder is available by calling the **isAvailable** property (the **get\_isAvailable** method in C#) and passing in the **System.String** value "dvdDecoder".</span></span>

<span data-ttu-id="383f7-130">Cada DVD se crea de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="383f7-130">Every DVD is authored differently.</span></span> <span data-ttu-id="383f7-131">Los métodos disponibles durante la reproducción y la navegación por DVD dependen de cómo se cree el DVD.</span><span class="sxs-lookup"><span data-stu-id="383f7-131">The methods available during DVD playback and navigation depend on how the DVD is authored.</span></span>

## <a name="requirements"></a><span data-ttu-id="383f7-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="383f7-132">Requirements</span></span>



| <span data-ttu-id="383f7-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="383f7-133">Requirement</span></span> | <span data-ttu-id="383f7-134">Value</span><span class="sxs-lookup"><span data-stu-id="383f7-134">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="383f7-135">Versión</span><span class="sxs-lookup"><span data-stu-id="383f7-135">Version</span></span><br/>   | <span data-ttu-id="383f7-136">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="383f7-136">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="383f7-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="383f7-137">Namespace</span></span><br/> | <span data-ttu-id="383f7-138">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="383f7-138">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="383f7-139">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="383f7-139">Assembly</span></span><br/>  | <dl> <span data-ttu-id="383f7-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="383f7-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="383f7-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="383f7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="383f7-142">**Interfaz IWMPDVD (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="383f7-142">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="383f7-143">**IWMPDVD. back (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="383f7-143">**IWMPDVD.back (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-back--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="383f7-144">**IWMPDVD. resume (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="383f7-144">**IWMPDVD.resume (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-resume--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="383f7-145">**IWMPDVD. titleMenu (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="383f7-145">**IWMPDVD.titleMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="383f7-146">**IWMPDVD. webmenu (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="383f7-146">**IWMPDVD.topMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





