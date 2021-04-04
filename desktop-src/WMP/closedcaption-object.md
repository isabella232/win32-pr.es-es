---
title: Objeto ClosedCaption
description: El objeto ClosedCaption proporciona una manera de incluir leyendas con un clip multimedia. El texto de la leyenda se encuentra en un archivo de intercambio de medios accesibles (SAMI) sincronizado.
ms.assetid: 5e192aa4-0ecd-4bda-8dad-1750039c7898
keywords:
- Objeto ClosedCaption Media Player de Windows
topic_type:
- apiref
api_name:
- ClosedCaption Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85e53468e8d5cc2694555b9a05d8b207d1660618
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104076967"
---
# <a name="closedcaption-object"></a><span data-ttu-id="87582-105">Objeto ClosedCaption</span><span class="sxs-lookup"><span data-stu-id="87582-105">ClosedCaption Object</span></span>

<span data-ttu-id="87582-106">El objeto **ClosedCaption** proporciona una manera de incluir leyendas con un clip multimedia.</span><span class="sxs-lookup"><span data-stu-id="87582-106">The **ClosedCaption** object provides a way to include captions with a media clip.</span></span> <span data-ttu-id="87582-107">El texto de la leyenda se encuentra en un archivo de intercambio de medios accesibles (SAMI) sincronizado.</span><span class="sxs-lookup"><span data-stu-id="87582-107">The captioning text is in a Synchronized Accessible Media Interchange (SAMI) file.</span></span>

<span data-ttu-id="87582-108">El objeto **ClosedCaption** admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="87582-108">The **ClosedCaption** object supports the following properties.</span></span>



| <span data-ttu-id="87582-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="87582-109">Property</span></span>                                           | <span data-ttu-id="87582-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="87582-110">Description</span></span>                                                                                          |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="87582-111">captioningID</span><span class="sxs-lookup"><span data-stu-id="87582-111">captioningID</span></span>](closedcaption-captioningid.md)     | <span data-ttu-id="87582-112">Especifica o recupera el nombre del marco o control que muestra los subtítulos.</span><span class="sxs-lookup"><span data-stu-id="87582-112">Specifies or retrieves the name of the frame or control displaying the captioning.</span></span>                   |
| [<span data-ttu-id="87582-113">SAMIFileName</span><span class="sxs-lookup"><span data-stu-id="87582-113">SAMIFileName</span></span>](closedcaption-samifilename.md)     | <span data-ttu-id="87582-114">Especifica o recupera el nombre del archivo que contiene la información necesaria para los subtítulos (CC).</span><span class="sxs-lookup"><span data-stu-id="87582-114">Specifies or retrieves the name of the file containing the information needed for closed captioning.</span></span> |
| [<span data-ttu-id="87582-115">SAMILang</span><span class="sxs-lookup"><span data-stu-id="87582-115">SAMILang</span></span>](closedcaption-samilang.md)             | <span data-ttu-id="87582-116">Especifica o recupera el idioma que se muestra para los subtítulos (CC).</span><span class="sxs-lookup"><span data-stu-id="87582-116">Specifies or retrieves the language displayed for closed captioning.</span></span>                                 |
| [<span data-ttu-id="87582-117">SAMILangCount</span><span class="sxs-lookup"><span data-stu-id="87582-117">SAMILangCount</span></span>](closedcaption-samilangcount.md)   | <span data-ttu-id="87582-118">Recupera el número de idiomas admitidos por el archivo SAMI actual.</span><span class="sxs-lookup"><span data-stu-id="87582-118">Retrieves the number of languages supported by the current SAMI file.</span></span>                                |
| [<span data-ttu-id="87582-119">SAMIStyle</span><span class="sxs-lookup"><span data-stu-id="87582-119">SAMIStyle</span></span>](closedcaption-samistyle.md)           | <span data-ttu-id="87582-120">Especifica o recupera el estilo de subtítulos (CC).</span><span class="sxs-lookup"><span data-stu-id="87582-120">Specifies or retrieves the closed captioning style.</span></span>                                                  |
| [<span data-ttu-id="87582-121">SAMIStyleCount</span><span class="sxs-lookup"><span data-stu-id="87582-121">SAMIStyleCount</span></span>](closedcaption-samistylecount.md) | <span data-ttu-id="87582-122">Recupera el número de estilos admitidos por el archivo SAMI actual.</span><span class="sxs-lookup"><span data-stu-id="87582-122">Retrieves the number of styles supported by the current SAMI file.</span></span>                                   |



 

<span data-ttu-id="87582-123">El objeto **ClosedCaption** admite los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="87582-123">The **ClosedCaption** object supports the following methods.</span></span>



| <span data-ttu-id="87582-124">Método</span><span class="sxs-lookup"><span data-stu-id="87582-124">Method</span></span>                                                 | <span data-ttu-id="87582-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="87582-125">Description</span></span>                                                                              |
|--------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="87582-126">getSAMILangID</span><span class="sxs-lookup"><span data-stu-id="87582-126">getSAMILangID</span></span>](closedcaption-getsamilangid.md)       | <span data-ttu-id="87582-127">Recupera el identificador de configuración regional (LCID) de un idioma admitido por el archivo SAMI actual.</span><span class="sxs-lookup"><span data-stu-id="87582-127">Retrieves the locale identifier (LCID) of a language supported by the current SAMI file.</span></span> |
| [<span data-ttu-id="87582-128">getSAMILangName</span><span class="sxs-lookup"><span data-stu-id="87582-128">getSAMILangName</span></span>](closedcaption-getsamilangname.md)   | <span data-ttu-id="87582-129">Recupera el nombre de un idioma admitido por el archivo SAMI actual.</span><span class="sxs-lookup"><span data-stu-id="87582-129">Retrieves the name of a language supported by the current SAMI file.</span></span>                     |
| [<span data-ttu-id="87582-130">getSAMIStyleName</span><span class="sxs-lookup"><span data-stu-id="87582-130">getSAMIStyleName</span></span>](closedcaption-getsamistylename.md) | <span data-ttu-id="87582-131">Recupera el nombre de un estilo compatible con el archivo SAMI actual.</span><span class="sxs-lookup"><span data-stu-id="87582-131">Retrieves the name of a style supported by the current SAMI file.</span></span>                        |



 

<span data-ttu-id="87582-132">Se tiene acceso al objeto **ClosedCaption** a través de la propiedad siguiente.</span><span class="sxs-lookup"><span data-stu-id="87582-132">The **ClosedCaption** object is accessed through the following property.</span></span>



| <span data-ttu-id="87582-133">Object</span><span class="sxs-lookup"><span data-stu-id="87582-133">Object</span></span>                      | <span data-ttu-id="87582-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="87582-134">Property</span></span>                                  |
|-----------------------------|-------------------------------------------|
| [<span data-ttu-id="87582-135">Reproductor</span><span class="sxs-lookup"><span data-stu-id="87582-135">Player</span></span>](player-object.md) | [<span data-ttu-id="87582-136">closedCaption</span><span class="sxs-lookup"><span data-stu-id="87582-136">closedCaption</span></span>](player-closedcaption.md) |



 

## <a name="see-also"></a><span data-ttu-id="87582-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="87582-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87582-138">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="87582-138">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="87582-139">**Referencia del modelo de objetos para scripting**</span><span class="sxs-lookup"><span data-stu-id="87582-139">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




