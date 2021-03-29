---
title: Enumeraciones de DWRITE_RENDERING_MODE
description: A partir de Windows 8, la \_ enumeración del modo de representación DWRITE \_ ha agregado nuevos valores de enumeración y ha dejado de usar otros.
ms.assetid: 3EA568B4-310D-4F70-9530-5916419282E5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fa79cf34a03960ddb42a8a80221e99d47be847
ms.sourcegitcommit: d1b8f5ed3d6e35e93cb254efc49428a072d7ef9a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/12/2019
ms.locfileid: "103993796"
---
# <a name="dwrite_rendering_mode-enumerations"></a><span data-ttu-id="1251b-103">\_Enumeraciones del modo de representación DWRITE \_</span><span class="sxs-lookup"><span data-stu-id="1251b-103">DWRITE\_RENDERING\_MODE enumerations</span></span>

<span data-ttu-id="1251b-104">A partir de Windows 8, la enumeración del **\_ \_ modo de representación DWRITE** ha agregado nuevos valores de enumeración y ha dejado de usar otros.</span><span class="sxs-lookup"><span data-stu-id="1251b-104">Starting in Windows 8, the **DWRITE\_RENDERING\_MODE** enumeration added new enumeration values and deprecated others.</span></span>

<span data-ttu-id="1251b-105">A partir de Windows 8, la enumeración de [**\_ \_ \_ modo de suavizado de texto DWRITE**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode) determina si el texto se representa con ClearType.</span><span class="sxs-lookup"><span data-stu-id="1251b-105">Starting in Windows 8, the [**DWRITE\_TEXT\_ANTIALIAS\_MODE**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode) enumeration determines whether text is rendered using ClearType.</span></span> <span data-ttu-id="1251b-106">Como resultado, todos los modos de representación de ClearType en la enumeración de **\_ \_ modo de representación DWRITE** están desusados.</span><span class="sxs-lookup"><span data-stu-id="1251b-106">As a result, all the ClearType rendering modes in the **DWRITE\_RENDERING\_MODE** enumeration are deprecated.</span></span> <span data-ttu-id="1251b-107">Estos valores de enumeración se asignan ahora a los nuevos modos de representación.</span><span class="sxs-lookup"><span data-stu-id="1251b-107">These enumeration values now map to new rendering modes.</span></span>

<span data-ttu-id="1251b-108">En la tabla siguiente se muestran los valores de enumeración antiguos y los nuevos valores a los que están asignados.</span><span class="sxs-lookup"><span data-stu-id="1251b-108">The table here shows the old enumeration values and the new values they are mapped to.</span></span> <span data-ttu-id="1251b-109">Para obtener descripciones de los nuevos valores, consulte [**\_ \_ modo de representación de DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode).</span><span class="sxs-lookup"><span data-stu-id="1251b-109">For descriptions of the new values, see [**DWRITE\_RENDERING\_MODE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode).</span></span>



| <span data-ttu-id="1251b-110">Modo anterior</span><span class="sxs-lookup"><span data-stu-id="1251b-110">Old mode</span></span>                                                                                | <span data-ttu-id="1251b-111">Nuevo modo</span><span class="sxs-lookup"><span data-stu-id="1251b-111">New mode</span></span>                                                                                |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="1251b-112">**\_modo de representación \_ DWRITE \_ CLEARTYPE \_ GDI \_ clásico**</span><span class="sxs-lookup"><span data-stu-id="1251b-112">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_GDI\_CLASSIC**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)       | [<span data-ttu-id="1251b-113">**\_modo de representación \_ DWRITE \_ GDI \_ clásico**</span><span class="sxs-lookup"><span data-stu-id="1251b-113">**DWRITE\_RENDERING\_MODE\_GDI\_CLASSIC**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)                  |
| [<span data-ttu-id="1251b-114">**\_modo de representación \_ DWRITE \_ CLEARTYPE \_ GDI \_ natural**</span><span class="sxs-lookup"><span data-stu-id="1251b-114">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_GDI\_NATURAL**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)       | [<span data-ttu-id="1251b-115">**\_modo de representación \_ DWRITE \_ GDI \_ natural**</span><span class="sxs-lookup"><span data-stu-id="1251b-115">**DWRITE\_RENDERING\_MODE\_GDI\_NATURAL**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)                  |
| [<span data-ttu-id="1251b-116">**\_modo de representación \_ DWRITE \_ CLEARTYPE \_ natural**</span><span class="sxs-lookup"><span data-stu-id="1251b-116">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_NATURAL**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)            | [<span data-ttu-id="1251b-117">**\_modo de representación \_ DWRITE \_ CLEARTYPE \_ natural**</span><span class="sxs-lookup"><span data-stu-id="1251b-117">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_NATURAL**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)            |
| [<span data-ttu-id="1251b-118">**\_modo de representación \_ DWRITE \_ CLEARTYPE \_ natural \_ simétrico**</span><span class="sxs-lookup"><span data-stu-id="1251b-118">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_NATURAL\_SYMMETRIC**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode) | [<span data-ttu-id="1251b-119">**\_modo de representación \_ DWRITE \_ CLEARTYPE \_ natural \_ simétrico**</span><span class="sxs-lookup"><span data-stu-id="1251b-119">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_NATURAL\_SYMMETRIC**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode) |



 

## <a name="in-this-section"></a><span data-ttu-id="1251b-120">En esta sección</span><span class="sxs-lookup"><span data-stu-id="1251b-120">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1251b-121">Tema</span><span class="sxs-lookup"><span data-stu-id="1251b-121">Topic</span></span></th>
<th><span data-ttu-id="1251b-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="1251b-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1251b-123"><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE (Windows 8 y versiones posteriores)</strong></a></span><span class="sxs-lookup"><span data-stu-id="1251b-123"><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE (Windows 8 and later)</strong></a></span></span><br/></td>
<td><span data-ttu-id="1251b-124">Representa un método de representación de glifos.</span><span class="sxs-lookup"><span data-stu-id="1251b-124">Represents a method of rendering glyphs.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1251b-125">En este tema se trata <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> en Windows 8 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="1251b-125">This topic is about <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> in Windows 8 and later.</span></span> <span data-ttu-id="1251b-126">Para obtener información sobre la versión anterior, consulte <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>este tema</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1251b-126">For info on the previous version see <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>this topic</strong></a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1251b-127"><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1251b-127"><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="1251b-128">Representa un método de representación de glifos.</span><span class="sxs-lookup"><span data-stu-id="1251b-128">Represents a method of rendering glyphs.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1251b-129">En este tema se trata <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> anterior a Windows 8 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="1251b-129">This topic is about <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> previous to Windows 8 and later.</span></span> <span data-ttu-id="1251b-130">Para obtener información sobre la versión más reciente, consulte <strong>este tema</strong>.</span><span class="sxs-lookup"><span data-stu-id="1251b-130">For info on the newer version see <strong>this topic</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 





