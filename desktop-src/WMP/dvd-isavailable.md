---
title: DVD. isAvailable
description: La propiedad isAvailable indica si un tipo especificado de información está disponible o se puede realizar una acción especificada. | DVD. isAvailable
ms.assetid: ed34a943-b9c3-40a8-8845-b83f16951a3e
keywords:
- DVD. isAvailable Windows Media Player
topic_type:
- apiref
api_name:
- DVD.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5088b4b6365dd60d859fda8ec563cc9c8ff8a4c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698074"
---
# <a name="dvdisavailable"></a><span data-ttu-id="4d4c1-105">DVD. isAvailable</span><span class="sxs-lookup"><span data-stu-id="4d4c1-105">DVD.isAvailable</span></span>

<span data-ttu-id="4d4c1-106">La propiedad **isavailable** indica si un tipo especificado de información está disponible o se puede realizar una acción especificada.</span><span class="sxs-lookup"><span data-stu-id="4d4c1-106">The **isAvailable** property indicates whether a specified type of information is available or a specified action can be performed.</span></span>

``` syntax
player.dvd.isAvailable(
        name
        )
```

## <a name="parameters"></a><span data-ttu-id="4d4c1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d4c1-107">Parameters</span></span>

<span data-ttu-id="4d4c1-108">*name*</span><span class="sxs-lookup"><span data-stu-id="4d4c1-108">*name*</span></span>

<span data-ttu-id="4d4c1-109">**Cadena** que contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4d4c1-109">**String** containing one of the following values.</span></span>



| <span data-ttu-id="4d4c1-110">String</span><span class="sxs-lookup"><span data-stu-id="4d4c1-110">String</span></span>     | <span data-ttu-id="4d4c1-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d4c1-111">Description</span></span>                                                                            |
|------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d4c1-112">atrás</span><span class="sxs-lookup"><span data-stu-id="4d4c1-112">back</span></span>       | <span data-ttu-id="4d4c1-113">Determina si el método **back** está disponible.</span><span class="sxs-lookup"><span data-stu-id="4d4c1-113">Determines whether the **back** method is available.</span></span>                                   |
| <span data-ttu-id="4d4c1-114">discos</span><span class="sxs-lookup"><span data-stu-id="4d4c1-114">dvd</span></span>        | <span data-ttu-id="4d4c1-115">Determina si el DVD está cargado.</span><span class="sxs-lookup"><span data-stu-id="4d4c1-115">Determines whether the DVD is loaded.</span></span>                                                  |
| <span data-ttu-id="4d4c1-116">dvdDecoder</span><span class="sxs-lookup"><span data-stu-id="4d4c1-116">dvdDecoder</span></span> | <span data-ttu-id="4d4c1-117">Determina si el descodificador de DVD está instalado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="4d4c1-117">Determines whether the DVD decoder is installed on system.</span></span>                             |
| <span data-ttu-id="4d4c1-118">resume</span><span class="sxs-lookup"><span data-stu-id="4d4c1-118">resume</span></span>     | <span data-ttu-id="4d4c1-119">Determina si el método **resume** está disponible.</span><span class="sxs-lookup"><span data-stu-id="4d4c1-119">Determines whether the **resume** method is available.</span></span>                                 |
| <span data-ttu-id="4d4c1-120">titleMenu</span><span class="sxs-lookup"><span data-stu-id="4d4c1-120">titleMenu</span></span>  | <span data-ttu-id="4d4c1-121">Determina si el método **titleMenu** está disponible.</span><span class="sxs-lookup"><span data-stu-id="4d4c1-121">Determines whether the **titleMenu** method is available.</span></span>                              |
| <span data-ttu-id="4d4c1-122">Menú de menús</span><span class="sxs-lookup"><span data-stu-id="4d4c1-122">topMenu</span></span>    | <span data-ttu-id="4d4c1-123">Determina si el método de **menú de menús** está disponible.</span><span class="sxs-lookup"><span data-stu-id="4d4c1-123">Determines whether the **topMenu** method is available.</span></span> <span data-ttu-id="4d4c1-124">Normalmente denominado menú raíz.</span><span class="sxs-lookup"><span data-stu-id="4d4c1-124">Commonly called the root menu.</span></span> |



 

## <a name="return-values"></a><span data-ttu-id="4d4c1-125">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="4d4c1-125">Return Values</span></span>

<span data-ttu-id="4d4c1-126">Este método devuelve un **valor booleano** de solo lectura que indica si el parámetro especificado está disponible.</span><span class="sxs-lookup"><span data-stu-id="4d4c1-126">This method returns a read-only **Boolean** indicating whether the specified parameter is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d4c1-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d4c1-127">Remarks</span></span>

<span data-ttu-id="4d4c1-128">Las características de DVD de Windows Media Player no funcionarán en equipos que no tengan instalado descodificadores de DVD de terceros.</span><span class="sxs-lookup"><span data-stu-id="4d4c1-128">The DVD features of Windows Media Player will not work on computers that do not have third-party DVD decoders installed.</span></span> <span data-ttu-id="4d4c1-129">Puede determinar si un descodificador está disponible llamando a **isavailable**("dvdDecoder").</span><span class="sxs-lookup"><span data-stu-id="4d4c1-129">You can determine whether a decoder is available by calling **isAvailable**("dvdDecoder").</span></span>

<span data-ttu-id="4d4c1-130">Cada DVD se crea de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="4d4c1-130">Every DVD is authored differently.</span></span> <span data-ttu-id="4d4c1-131">Los métodos disponibles durante la reproducción y la navegación por DVD dependen de cómo se cree el DVD.</span><span class="sxs-lookup"><span data-stu-id="4d4c1-131">The methods available during DVD playback and navigation depend on how the DVD is authored.</span></span>

<span data-ttu-id="4d4c1-132">**Windows Media Player 10 Mobile:** Esta propiedad siempre devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="4d4c1-132">**Windows Media Player 10 Mobile:** This property always returns **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d4c1-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d4c1-133">Requirements</span></span>



| <span data-ttu-id="4d4c1-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d4c1-134">Requirement</span></span> | <span data-ttu-id="4d4c1-135">Value</span><span class="sxs-lookup"><span data-stu-id="4d4c1-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4d4c1-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d4c1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4d4c1-137">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="4d4c1-137">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4d4c1-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d4c1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4d4c1-139">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4d4c1-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4d4c1-140">Versión</span><span class="sxs-lookup"><span data-stu-id="4d4c1-140">Version</span></span><br/>                  | <span data-ttu-id="4d4c1-141">Windows Media Player para Windows XP o posterior</span><span class="sxs-lookup"><span data-stu-id="4d4c1-141">Windows Media Player for Windows XP or later</span></span><br/>                            |
| <span data-ttu-id="4d4c1-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4d4c1-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d4c1-143"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d4c1-143"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d4c1-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d4c1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d4c1-145">**Objeto de DVD**</span><span class="sxs-lookup"><span data-stu-id="4d4c1-145">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





