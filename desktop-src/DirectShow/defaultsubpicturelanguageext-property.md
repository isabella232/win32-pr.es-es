---
description: La propiedad DefaultSubpictureLanguageExt recupera la extensión de idioma de subimagen de DVD predeterminada.
ms.assetid: bd437844-6e5c-4237-a968-700a53e18635
title: Propiedad DefaultSubpictureLanguageExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37bba455a26df4eaa6676b77447c3faed408609
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536712"
---
# <a name="defaultsubpicturelanguageext-property"></a><span data-ttu-id="3b988-103">Propiedad DefaultSubpictureLanguageExt</span><span class="sxs-lookup"><span data-stu-id="3b988-103">DefaultSubpictureLanguageExt Property</span></span>

> [!Note]  
> <span data-ttu-id="3b988-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3b988-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="3b988-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="3b988-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="3b988-106">La `DefaultSubpictureLanguageExt` propiedad recupera la extensión de idioma de subimagen de DVD predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3b988-106">The `DefaultSubpictureLanguageExt` property retrieves the default DVD subpicture language extension.</span></span>

``` syntax
[ iLangExt = ] MSWebDVD.DefaultSubpictureLanguageExt
```

## <a name="return-value"></a><span data-ttu-id="3b988-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b988-107">Return Value</span></span>

<span data-ttu-id="3b988-108">Devuelve un valor entero que indica la extensión de idioma de subimagen de DVD predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3b988-108">Returns an Integer value indicating the default DVD subpicture language extension.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b988-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b988-109">Remarks</span></span>

<span data-ttu-id="3b988-110">Esta propiedad es de solo lectura y no tiene ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3b988-110">This property is read-only with no default value.</span></span> <span data-ttu-id="3b988-111">En la siguiente tabla se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="3b988-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="3b988-112">Valor</span><span class="sxs-lookup"><span data-stu-id="3b988-112">Value</span></span> | <span data-ttu-id="3b988-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b988-113">Description</span></span>                    |
|-------|--------------------------------|
| <span data-ttu-id="3b988-114">0</span><span class="sxs-lookup"><span data-stu-id="3b988-114">0</span></span>     | <span data-ttu-id="3b988-115">No se ha especificado la extensión</span><span class="sxs-lookup"><span data-stu-id="3b988-115">Extension Not Specified</span></span>        |
| <span data-ttu-id="3b988-116">1</span><span class="sxs-lookup"><span data-stu-id="3b988-116">1</span></span>     | <span data-ttu-id="3b988-117">Leyendas normales</span><span class="sxs-lookup"><span data-stu-id="3b988-117">Normal Captions</span></span>                |
| <span data-ttu-id="3b988-118">2</span><span class="sxs-lookup"><span data-stu-id="3b988-118">2</span></span>     | <span data-ttu-id="3b988-119">Leyendas grandes</span><span class="sxs-lookup"><span data-stu-id="3b988-119">Big Captions</span></span>                   |
| <span data-ttu-id="3b988-120">3</span><span class="sxs-lookup"><span data-stu-id="3b988-120">3</span></span>     | <span data-ttu-id="3b988-121">Títulos de los elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3b988-121">Children's Captions</span></span>            |
| <span data-ttu-id="3b988-122">5</span><span class="sxs-lookup"><span data-stu-id="3b988-122">5</span></span>     | <span data-ttu-id="3b988-123">Subtítulos normales cerrados</span><span class="sxs-lookup"><span data-stu-id="3b988-123">Normal Closed Captions</span></span>         |
| <span data-ttu-id="3b988-124">6</span><span class="sxs-lookup"><span data-stu-id="3b988-124">6</span></span>     | <span data-ttu-id="3b988-125">Subtítulos Big Closed</span><span class="sxs-lookup"><span data-stu-id="3b988-125">Big Closed Captions</span></span>            |
| <span data-ttu-id="3b988-126">7</span><span class="sxs-lookup"><span data-stu-id="3b988-126">7</span></span>     | <span data-ttu-id="3b988-127">Subtítulos (CC) de los niños</span><span class="sxs-lookup"><span data-stu-id="3b988-127">Children's Closed Captions</span></span>     |
| <span data-ttu-id="3b988-128">9</span><span class="sxs-lookup"><span data-stu-id="3b988-128">9</span></span>     | <span data-ttu-id="3b988-129">Forzado</span><span class="sxs-lookup"><span data-stu-id="3b988-129">Forced</span></span>                         |
| <span data-ttu-id="3b988-130">13</span><span class="sxs-lookup"><span data-stu-id="3b988-130">13</span></span>    | <span data-ttu-id="3b988-131">Comentarios del Director normal</span><span class="sxs-lookup"><span data-stu-id="3b988-131">Normal Director's Comments</span></span>     |
| <span data-ttu-id="3b988-132">14</span><span class="sxs-lookup"><span data-stu-id="3b988-132">14</span></span>    | <span data-ttu-id="3b988-133">Comentarios del Big Director</span><span class="sxs-lookup"><span data-stu-id="3b988-133">Big Director's Comments</span></span>        |
| <span data-ttu-id="3b988-134">15</span><span class="sxs-lookup"><span data-stu-id="3b988-134">15</span></span>    | <span data-ttu-id="3b988-135">Comentarios de Director's de los niños</span><span class="sxs-lookup"><span data-stu-id="3b988-135">Children's Director's Comments</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="3b988-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b988-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b988-137">**SelectDefaultSubpictureLanguage**</span><span class="sxs-lookup"><span data-stu-id="3b988-137">**SelectDefaultSubpictureLanguage**</span></span>](selectdefaultsubpicturelanguage-method.md)
</dt> </dl>

 

 



