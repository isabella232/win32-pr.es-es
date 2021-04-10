---
description: configuración regional \_ IDIGITSUBSTITUTION
ms.assetid: f3f7d7ac-8f1e-4bfa-84f0-dfe8cff568c3
title: LOCALE_IDIGITSUBSTITUTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c063ed5b937c3e4c4ae06e40631b9795f6a73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153746"
---
# <a name="locale_idigitsubstitution"></a><span data-ttu-id="ceef4-103">configuración regional \_ IDIGITSUBSTITUTION</span><span class="sxs-lookup"><span data-stu-id="ceef4-103">LOCALE\_IDIGITSUBSTITUTION</span></span>

<span data-ttu-id="ceef4-104">**Windows 2000:** Forma de dígitos.</span><span class="sxs-lookup"><span data-stu-id="ceef4-104">**Windows 2000:** The shape of digits.</span></span> <span data-ttu-id="ceef4-105">Por ejemplo, los dígitos árabe, tailandés y hindú tienen formas clásicas diferentes de los dígitos europeos.</span><span class="sxs-lookup"><span data-stu-id="ceef4-105">For example, Arabic, Thai, and Indic digits have classical shapes different from European digits.</span></span> <span data-ttu-id="ceef4-106">En el caso de las configuraciones regionales con la [configuración regional \_ SNATIVEDIGITS](locale-snative-constants.md) especificada como valores distintos del ASCII 0-9, este valor especifica si se debe dar preferencia a esos otros dígitos para la presentación.</span><span class="sxs-lookup"><span data-stu-id="ceef4-106">For locales with [LOCALE\_SNATIVEDIGITS](locale-snative-constants.md) specified as values other than ASCII 0-9, this value specifies whether preference should be given to those other digits for display purposes.</span></span> <span data-ttu-id="ceef4-107">Por ejemplo, si se elige un valor de 2, siempre se usan los dígitos especificados por SNATIVEDIGITS de configuración regional \_ .</span><span class="sxs-lookup"><span data-stu-id="ceef4-107">For example, if a value of 2 is chosen, the digits specified by LOCALE\_SNATIVEDIGITS are always used.</span></span> <span data-ttu-id="ceef4-108">Si se elige 1, siempre se usan los dígitos ASCII 0-9.</span><span class="sxs-lookup"><span data-stu-id="ceef4-108">If a 1 is chosen, the ASCII 0-9 digits are always used.</span></span> <span data-ttu-id="ceef4-109">Si se elige 0, se utiliza ASCII en algunas circunstancias y los dígitos especificados por la configuración regional \_ SNATIVEDIGITS se usan en otros, dependiendo del contexto.</span><span class="sxs-lookup"><span data-stu-id="ceef4-109">If a 0 is chosen, ASCII is used in some circumstances and the digits specified by LOCALE\_SNATIVEDIGITS are used in others, depending on the context.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ceef4-110">Value</span><span class="sxs-lookup"><span data-stu-id="ceef4-110">Value</span></span></th>
<th><span data-ttu-id="ceef4-111">Significado</span><span class="sxs-lookup"><span data-stu-id="ceef4-111">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ceef4-112">0</span><span class="sxs-lookup"><span data-stu-id="ceef4-112">0</span></span></td>
<td><span data-ttu-id="ceef4-113">Sustitución basada en contexto.</span><span class="sxs-lookup"><span data-stu-id="ceef4-113">Context-based substitution.</span></span> <span data-ttu-id="ceef4-114">Los dígitos se muestran en función del texto anterior en el mismo resultado.</span><span class="sxs-lookup"><span data-stu-id="ceef4-114">Digits are displayed based on the previous text in the same output.</span></span> <span data-ttu-id="ceef4-115">Los dígitos europeos siguen los alfabetos latinos, Arabic-Indic dígitos siguen el texto árabe y otros dígitos nacionales siguen el texto escrito en otros distintos scripts.</span><span class="sxs-lookup"><span data-stu-id="ceef4-115">European digits follow Latin scripts, Arabic-Indic digits follow Arabic text, and other national digits follow text written in various other scripts.</span></span> <span data-ttu-id="ceef4-116">Cuando no hay texto anterior, la configuración regional y el orden de lectura mostrado determinan la sustitución de dígitos, tal como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ceef4-116">When there is no preceding text, the locale and the displayed reading order determine digit substitution, as shown in the following table.</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ceef4-117">Configuración regional</span><span class="sxs-lookup"><span data-stu-id="ceef4-117">Locale</span></span></th>
<th><span data-ttu-id="ceef4-118">Orden de lectura</span><span class="sxs-lookup"><span data-stu-id="ceef4-118">Reading order</span></span></th>
<th><span data-ttu-id="ceef4-119">Dígitos usados</span><span class="sxs-lookup"><span data-stu-id="ceef4-119">Digits used</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ceef4-120">Árabe</span><span class="sxs-lookup"><span data-stu-id="ceef4-120">Arabic</span></span></td>
<td><span data-ttu-id="ceef4-121">De derecha a izquierda</span><span class="sxs-lookup"><span data-stu-id="ceef4-121">Right-to-left</span></span></td>
<td><span data-ttu-id="ceef4-122">Arabic-Indic</span><span class="sxs-lookup"><span data-stu-id="ceef4-122">Arabic-Indic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ceef4-123">Tailandés</span><span class="sxs-lookup"><span data-stu-id="ceef4-123">Thai</span></span></td>
<td><span data-ttu-id="ceef4-124">De izquierda a derecha</span><span class="sxs-lookup"><span data-stu-id="ceef4-124">Left-to-right</span></span></td>
<td><span data-ttu-id="ceef4-125">Dígitos tailandeses</span><span class="sxs-lookup"><span data-stu-id="ceef4-125">Thai digits</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ceef4-126">Todos los demás</span><span class="sxs-lookup"><span data-stu-id="ceef4-126">All others</span></span></td>
<td><span data-ttu-id="ceef4-127">Any</span><span class="sxs-lookup"><span data-stu-id="ceef4-127">Any</span></span></td>
<td><span data-ttu-id="ceef4-128">No se utiliza ninguna sustitución</span><span class="sxs-lookup"><span data-stu-id="ceef4-128">No substitution used</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ceef4-129">1</span><span class="sxs-lookup"><span data-stu-id="ceef4-129">1</span></span></td>
<td><span data-ttu-id="ceef4-130">No se utiliza ninguna sustitución.</span><span class="sxs-lookup"><span data-stu-id="ceef4-130">No substitution used.</span></span> <span data-ttu-id="ceef4-131">Compatibilidad completa con Unicode.</span><span class="sxs-lookup"><span data-stu-id="ceef4-131">Full Unicode compatibility.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ceef4-132">2</span><span class="sxs-lookup"><span data-stu-id="ceef4-132">2</span></span></td>
<td><span data-ttu-id="ceef4-133">Sustitución de dígitos nativa.</span><span class="sxs-lookup"><span data-stu-id="ceef4-133">Native digit substitution.</span></span> <span data-ttu-id="ceef4-134">Las formas nacionales se muestran según LOCALE_SNATIVEDIGITS.</span><span class="sxs-lookup"><span data-stu-id="ceef4-134">National shapes are displayed according to LOCALE_SNATIVEDIGITS.</span></span></td>
</tr>
</tbody>
</table>



 

 

 



