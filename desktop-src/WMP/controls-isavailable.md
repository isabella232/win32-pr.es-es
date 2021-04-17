---
title: Controls. isAvailable
description: La propiedad isAvailable indica si un tipo especificado de información está disponible o se puede realizar una acción especificada. | Controls. isAvailable
ms.assetid: d2bfaa67-eac9-4fc4-9424-636ddb4b35d6
keywords:
- Windows Media Player Controls. isAvailable
topic_type:
- apiref
api_name:
- Controls.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61afa07596a55208be63bd29759fd5f9f3e10170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699901"
---
# <a name="controlsisavailable"></a><span data-ttu-id="3288b-105">Controls. isAvailable</span><span class="sxs-lookup"><span data-stu-id="3288b-105">Controls.isAvailable</span></span>

<span data-ttu-id="3288b-106">La propiedad **isavailable** indica si un tipo especificado de información está disponible o se puede realizar una acción especificada.</span><span class="sxs-lookup"><span data-stu-id="3288b-106">The **isAvailable** property indicates whether a specified type of information is available or a specified action can be performed.</span></span>

``` syntax
player.controls.isAvailable(
        name
        )
```

## <a name="parameters"></a><span data-ttu-id="3288b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3288b-107">Parameters</span></span>

<span data-ttu-id="3288b-108">*name*</span><span class="sxs-lookup"><span data-stu-id="3288b-108">*name*</span></span>

<span data-ttu-id="3288b-109">**Cadena** que contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3288b-109">**String** containing one of the following values.</span></span>



| <span data-ttu-id="3288b-110">String</span><span class="sxs-lookup"><span data-stu-id="3288b-110">String</span></span>          | <span data-ttu-id="3288b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3288b-111">Description</span></span>                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3288b-112">currentItem</span><span class="sxs-lookup"><span data-stu-id="3288b-112">currentItem</span></span>     | <span data-ttu-id="3288b-113">Determina si el usuario puede establecer la propiedad **CurrentItem** .</span><span class="sxs-lookup"><span data-stu-id="3288b-113">Determines whether the user can set the **currentItem** property.</span></span>                                                                                                 |
| <span data-ttu-id="3288b-114">currentMarker</span><span class="sxs-lookup"><span data-stu-id="3288b-114">currentMarker</span></span>   | <span data-ttu-id="3288b-115">Determina si el usuario puede buscar un marcador específico.</span><span class="sxs-lookup"><span data-stu-id="3288b-115">Determines whether the user can seek to a specific marker.</span></span>                                                                                                        |
| <span data-ttu-id="3288b-116">currentPosition</span><span class="sxs-lookup"><span data-stu-id="3288b-116">currentPosition</span></span> | <span data-ttu-id="3288b-117">Determina si el usuario puede buscar una posición específica en el archivo.</span><span class="sxs-lookup"><span data-stu-id="3288b-117">Determines whether the user can seek to a specific position in the file.</span></span> <span data-ttu-id="3288b-118">Algunos archivos no admiten búsquedas.</span><span class="sxs-lookup"><span data-stu-id="3288b-118">Some files do not support seeking.</span></span>                                                       |
| <span data-ttu-id="3288b-119">fastForward</span><span class="sxs-lookup"><span data-stu-id="3288b-119">fastForward</span></span>     | <span data-ttu-id="3288b-120">Determina si el archivo admite el reenvío rápido y si se puede invocar la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="3288b-120">Determines whether the file supports fast forwarding and whether that functionality can be invoked.</span></span> <span data-ttu-id="3288b-121">Muchos tipos de archivo (o secuencias en directo) no admiten fastForward.</span><span class="sxs-lookup"><span data-stu-id="3288b-121">Many file types (or live streams) do not support fastForward.</span></span> |
| <span data-ttu-id="3288b-122">fastReverse</span><span class="sxs-lookup"><span data-stu-id="3288b-122">fastReverse</span></span>     | <span data-ttu-id="3288b-123">Determina si el archivo admite fastReverse y si se puede invocar esa funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="3288b-123">Determines whether the file supports fastReverse and whether that functionality can be invoked.</span></span> <span data-ttu-id="3288b-124">Muchos tipos de archivo (o secuencias en directo) no admiten fastReverse.</span><span class="sxs-lookup"><span data-stu-id="3288b-124">Many file types (or live streams) do not support fastReverse.</span></span>     |
| <span data-ttu-id="3288b-125">Siguiente</span><span class="sxs-lookup"><span data-stu-id="3288b-125">next</span></span>            | <span data-ttu-id="3288b-126">Determina si el usuario puede buscar la siguiente entrada en una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="3288b-126">Determines whether the user can seek to the next entry in a playlist.</span></span>                                                                                             |
| <span data-ttu-id="3288b-127">pause</span><span class="sxs-lookup"><span data-stu-id="3288b-127">pause</span></span>           | <span data-ttu-id="3288b-128">Determina si el método **PAUSE** está disponible.</span><span class="sxs-lookup"><span data-stu-id="3288b-128">Determines whether the **pause** method is available.</span></span>                                                                                                             |
| <span data-ttu-id="3288b-129">reproducción</span><span class="sxs-lookup"><span data-stu-id="3288b-129">play</span></span>            | <span data-ttu-id="3288b-130">Determina si el método **Play** está disponible.</span><span class="sxs-lookup"><span data-stu-id="3288b-130">Determines whether the **play** method is available.</span></span>                                                                                                              |
| <span data-ttu-id="3288b-131">previous</span><span class="sxs-lookup"><span data-stu-id="3288b-131">previous</span></span>        | <span data-ttu-id="3288b-132">Determina si el usuario puede buscar la entrada anterior en una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="3288b-132">Determines whether the user can seek to the previous entry in a playlist.</span></span>                                                                                         |
| <span data-ttu-id="3288b-133">paso</span><span class="sxs-lookup"><span data-stu-id="3288b-133">step</span></span>            | <span data-ttu-id="3288b-134">Determina si el método **Step** está disponible durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="3288b-134">Determines whether the **step** method is available during playback.</span></span>                                                                                              |
| <span data-ttu-id="3288b-135">stop</span><span class="sxs-lookup"><span data-stu-id="3288b-135">stop</span></span>            | <span data-ttu-id="3288b-136">Determina si el método de **detención** está disponible.</span><span class="sxs-lookup"><span data-stu-id="3288b-136">Determines whether the **stop** method is available.</span></span>                                                                                                              |



 

## <a name="return-values"></a><span data-ttu-id="3288b-137">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="3288b-137">Return Values</span></span>

<span data-ttu-id="3288b-138">Este método devuelve un valor **booleano** .</span><span class="sxs-lookup"><span data-stu-id="3288b-138">This method returns a **Boolean** value.</span></span>

## <a name="examples"></a><span data-ttu-id="3288b-139">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3288b-139">Examples</span></span>

<span data-ttu-id="3288b-140">En el ejemplo siguiente se crea un elemento de botón HTML que busca la posición inicial del elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="3288b-140">The following example creates an HTML BUTTON element that seeks to the starting position of the current media item.</span></span> <span data-ttu-id="3288b-141">El código JScript usa **isavailable** para comprobar que el archivo admite la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3288b-141">The JScript code uses **isAvailable** to verify that the file supports the seek operation.</span></span> <span data-ttu-id="3288b-142">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="3288b-142">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "START"  NAME = "START"  VALUE = "Seek To Zero"

    /* If supported, seek to position zero. */
    onClick = "if (Player.controls.isAvailable('CurrentPosition'))
        Player.controls.currentPosition = 0;
">
```



## <a name="requirements"></a><span data-ttu-id="3288b-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3288b-143">Requirements</span></span>



| <span data-ttu-id="3288b-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="3288b-144">Requirement</span></span> | <span data-ttu-id="3288b-145">Value</span><span class="sxs-lookup"><span data-stu-id="3288b-145">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3288b-146">Versión</span><span class="sxs-lookup"><span data-stu-id="3288b-146">Version</span></span><br/> | <span data-ttu-id="3288b-147">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="3288b-147">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="3288b-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3288b-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="3288b-149"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3288b-149"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3288b-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="3288b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3288b-151">**Controls (objeto)**</span><span class="sxs-lookup"><span data-stu-id="3288b-151">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





