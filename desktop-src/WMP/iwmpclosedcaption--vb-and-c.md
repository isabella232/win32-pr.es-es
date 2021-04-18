---
title: Interfaz IWMPClosedCaption (VB y C) (WMP. h)
description: Proporciona una manera de incluir leyendas con un archivo multimedia digital. El texto de la leyenda se encuentra en un archivo de intercambio de medios accesibles (SAMI) sincronizado.
ms.assetid: 927f6fe4-5847-439e-9df0-19cc910d887d
keywords:
- IWMPClosedCaption (VB y C) interfaz de Windows Media Player
- IWMPClosedCaption (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPClosedCaption (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ce3f697fc5c651a47f257a61bd9841987f54478
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690429"
---
# <a name="iwmpclosedcaption-vb-and-c-interface"></a><span data-ttu-id="659a9-106">Interfaz IWMPClosedCaption (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="659a9-106">IWMPClosedCaption (VB and C#) interface</span></span>

<span data-ttu-id="659a9-107">Proporciona una manera de incluir leyendas con un archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="659a9-107">Provides a way to include captions with a digital media file.</span></span> <span data-ttu-id="659a9-108">El texto de la leyenda se encuentra en un archivo de intercambio de medios accesibles (SAMI) sincronizado.</span><span class="sxs-lookup"><span data-stu-id="659a9-108">The captioning text is in a Synchronized Accessible Media Interchange (SAMI) file.</span></span>

## <a name="members"></a><span data-ttu-id="659a9-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="659a9-109">Members</span></span>

<span data-ttu-id="659a9-110">La interfaz **IWMPClosedCaption (VB y C#)** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="659a9-110">The **IWMPClosedCaption (VB and C#)** interface does not define any members.</span></span>

<span data-ttu-id="659a9-111">La interfaz **IWMPClosedCaption** expone las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="659a9-111">The **IWMPClosedCaption** interface exposes the following properties.</span></span>



| <span data-ttu-id="659a9-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="659a9-112">Property</span></span>                                                                             | <span data-ttu-id="659a9-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="659a9-113">Description</span></span>                                                                                |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="659a9-114">captioningId</span><span class="sxs-lookup"><span data-stu-id="659a9-114">captioningId</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md) | <span data-ttu-id="659a9-115">Obtiene o establece el nombre del elemento HTML que muestra los subtítulos.</span><span class="sxs-lookup"><span data-stu-id="659a9-115">Gets or sets the name of the HTML element displaying the captioning.</span></span>                       |
| [<span data-ttu-id="659a9-116">SAMIFileName</span><span class="sxs-lookup"><span data-stu-id="659a9-116">SAMIFileName</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samifilename--vb-and-c.md) | <span data-ttu-id="659a9-117">Obtiene o establece el nombre del archivo que contiene la información necesaria para los subtítulos (CC).</span><span class="sxs-lookup"><span data-stu-id="659a9-117">Gets or sets the name of the file containing the information needed for closed captioning.</span></span> |
| [<span data-ttu-id="659a9-118">SAMILang</span><span class="sxs-lookup"><span data-stu-id="659a9-118">SAMILang</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)         | <span data-ttu-id="659a9-119">Obtiene o establece el idioma que se muestra para los subtítulos (CC).</span><span class="sxs-lookup"><span data-stu-id="659a9-119">Gets or sets the language displayed for closed captioning.</span></span>                                 |
| [<span data-ttu-id="659a9-120">SAMIStyle</span><span class="sxs-lookup"><span data-stu-id="659a9-120">SAMIStyle</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)       | <span data-ttu-id="659a9-121">Obtiene o establece el estilo de subtítulos (CC).</span><span class="sxs-lookup"><span data-stu-id="659a9-121">Gets or sets the closed captioning style.</span></span>                                                  |



 

<span data-ttu-id="659a9-122">Obtenga una interfaz **IWMPClosedCaption** con la siguiente propiedad.</span><span class="sxs-lookup"><span data-stu-id="659a9-122">Get an **IWMPClosedCaption** interface by using the following property.</span></span>



| <span data-ttu-id="659a9-123">Object</span><span class="sxs-lookup"><span data-stu-id="659a9-123">Object</span></span>                                                            | <span data-ttu-id="659a9-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="659a9-124">Property</span></span>                                                                   |
|-------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="659a9-125">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="659a9-125">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="659a9-126">closedCaption</span><span class="sxs-lookup"><span data-stu-id="659a9-126">closedCaption</span></span>](axwmplib-axwindowsmediaplayer-closedcaption--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="659a9-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="659a9-127">Requirements</span></span>



| <span data-ttu-id="659a9-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="659a9-128">Requirement</span></span> | <span data-ttu-id="659a9-129">Value</span><span class="sxs-lookup"><span data-stu-id="659a9-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="659a9-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="659a9-130">Header</span></span><br/> | <dl> <span data-ttu-id="659a9-131"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="659a9-131"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="659a9-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="659a9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="659a9-133">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="659a9-133">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="659a9-134">**Interfaces para Visual Basic .NET y C #**</span><span class="sxs-lookup"><span data-stu-id="659a9-134">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="659a9-135">**Interfaz IWMPClosedCaption2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="659a9-135">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





