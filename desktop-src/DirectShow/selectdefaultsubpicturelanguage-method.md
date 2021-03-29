---
description: El método SelectDefaultSubpictureLanguage establece el idioma de subimagen predeterminado actual en el objeto MSWebDVD.
ms.assetid: e83980d1-c7cd-4755-9a27-3b0c2548009e
title: Método SelectDefaultSubpictureLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d7dd4d66ae9d0580bf863ede9fff1e51d373e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805834"
---
# <a name="selectdefaultsubpicturelanguage-method"></a><span data-ttu-id="b008c-103">Método SelectDefaultSubpictureLanguage</span><span class="sxs-lookup"><span data-stu-id="b008c-103">SelectDefaultSubpictureLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="b008c-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b008c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b008c-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="b008c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="b008c-106">El `SelectDefaultSubpictureLanguage` método establece el idioma de subimagen predeterminado actual en el objeto **MSWebDVD** .</span><span class="sxs-lookup"><span data-stu-id="b008c-106">The `SelectDefaultSubpictureLanguage` method sets the current default subpicture language in the **MSWebDVD** object.</span></span>

``` syntax
MSWebDVD.SelectDefaultSubpictureLanguage(iLang,iExt)
```

## <a name="parameters"></a><span data-ttu-id="b008c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b008c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b008c-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span><span class="sxs-lookup"><span data-stu-id="b008c-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span></span>
</dt> <dd>

<span data-ttu-id="b008c-109">Especifica el idioma como un entero.</span><span class="sxs-lookup"><span data-stu-id="b008c-109">Specifies the language as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="b008c-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span><span class="sxs-lookup"><span data-stu-id="b008c-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span></span>
</dt> <dd>

<span data-ttu-id="b008c-111">Especifica la extensión del lenguaje de subimagen como un entero.</span><span class="sxs-lookup"><span data-stu-id="b008c-111">Specifies the subpicture language extension as an Integer.</span></span>



| <span data-ttu-id="b008c-112">Value</span><span class="sxs-lookup"><span data-stu-id="b008c-112">Value</span></span> | <span data-ttu-id="b008c-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="b008c-113">Description</span></span>                    |
|-------|--------------------------------|
| <span data-ttu-id="b008c-114">0</span><span class="sxs-lookup"><span data-stu-id="b008c-114">0</span></span>     | <span data-ttu-id="b008c-115">No se ha especificado la extensión</span><span class="sxs-lookup"><span data-stu-id="b008c-115">Extension Not Specified</span></span>        |
| <span data-ttu-id="b008c-116">1</span><span class="sxs-lookup"><span data-stu-id="b008c-116">1</span></span>     | <span data-ttu-id="b008c-117">Leyendas normales</span><span class="sxs-lookup"><span data-stu-id="b008c-117">Normal Captions</span></span>                |
| <span data-ttu-id="b008c-118">2</span><span class="sxs-lookup"><span data-stu-id="b008c-118">2</span></span>     | <span data-ttu-id="b008c-119">Leyendas grandes</span><span class="sxs-lookup"><span data-stu-id="b008c-119">Big Captions</span></span>                   |
| <span data-ttu-id="b008c-120">3</span><span class="sxs-lookup"><span data-stu-id="b008c-120">3</span></span>     | <span data-ttu-id="b008c-121">Títulos de los elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b008c-121">Children's Captions</span></span>            |
| <span data-ttu-id="b008c-122">5</span><span class="sxs-lookup"><span data-stu-id="b008c-122">5</span></span>     | <span data-ttu-id="b008c-123">Subtítulos normales cerrados</span><span class="sxs-lookup"><span data-stu-id="b008c-123">Normal Closed Captions</span></span>         |
| <span data-ttu-id="b008c-124">6</span><span class="sxs-lookup"><span data-stu-id="b008c-124">6</span></span>     | <span data-ttu-id="b008c-125">Subtítulos Big Closed</span><span class="sxs-lookup"><span data-stu-id="b008c-125">Big Closed Captions</span></span>            |
| <span data-ttu-id="b008c-126">7</span><span class="sxs-lookup"><span data-stu-id="b008c-126">7</span></span>     | <span data-ttu-id="b008c-127">Subtítulos (CC) de los niños</span><span class="sxs-lookup"><span data-stu-id="b008c-127">Children's Closed Captions</span></span>     |
| <span data-ttu-id="b008c-128">9</span><span class="sxs-lookup"><span data-stu-id="b008c-128">9</span></span>     | <span data-ttu-id="b008c-129">Forzado</span><span class="sxs-lookup"><span data-stu-id="b008c-129">Forced</span></span>                         |
| <span data-ttu-id="b008c-130">13</span><span class="sxs-lookup"><span data-stu-id="b008c-130">13</span></span>    | <span data-ttu-id="b008c-131">Comentarios del Director normal</span><span class="sxs-lookup"><span data-stu-id="b008c-131">Normal Director's Comments</span></span>     |
| <span data-ttu-id="b008c-132">14</span><span class="sxs-lookup"><span data-stu-id="b008c-132">14</span></span>    | <span data-ttu-id="b008c-133">Comentarios del Big Director</span><span class="sxs-lookup"><span data-stu-id="b008c-133">Big Director's Comments</span></span>        |
| <span data-ttu-id="b008c-134">15</span><span class="sxs-lookup"><span data-stu-id="b008c-134">15</span></span>    | <span data-ttu-id="b008c-135">Comentarios de Director's de los niños</span><span class="sxs-lookup"><span data-stu-id="b008c-135">Children's Director's Comments</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b008c-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b008c-136">Return Value</span></span>

<span data-ttu-id="b008c-137">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b008c-137">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b008c-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b008c-138">Remarks</span></span>

<span data-ttu-id="b008c-139">La extensión del lenguaje de subimagen proporciona más información acerca de la subimagen.</span><span class="sxs-lookup"><span data-stu-id="b008c-139">The subpicture language extension provides further information about the subpicture.</span></span>

 

 



