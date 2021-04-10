---
description: Especifica los datos de la malla menos los datos de la posición.
ms.assetid: 30a95ca3-84ab-475d-9654-a3853263056b
title: FVFData
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52af6096357c4855d2dc34442c6cd4814b6713b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152114"
---
# <a name="fvfdata"></a><span data-ttu-id="827c1-103">FVFData</span><span class="sxs-lookup"><span data-stu-id="827c1-103">FVFData</span></span>

<span data-ttu-id="827c1-104">Especifica los datos de la malla menos los datos de la posición.</span><span class="sxs-lookup"><span data-stu-id="827c1-104">Specifies the mesh data minus the position data.</span></span>

``` syntax
template FVFData
{
    < B6E70A0E-8EF9-4e83-94AD-ECC8B0C04897 >
    DWORD dwFVF;
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

<span data-ttu-id="827c1-105">Donde:</span><span class="sxs-lookup"><span data-stu-id="827c1-105">Where:</span></span>

-   <span data-ttu-id="827c1-106">dwFVF: código FVF.</span><span class="sxs-lookup"><span data-stu-id="827c1-106">dwFVF - A FVF code.</span></span>
-   <span data-ttu-id="827c1-107">nDWords: datos binarios.</span><span class="sxs-lookup"><span data-stu-id="827c1-107">nDWords - Binary data.</span></span> <span data-ttu-id="827c1-108">Número de DWORDs.</span><span class="sxs-lookup"><span data-stu-id="827c1-108">The number of DWORDS.</span></span>
-   <span data-ttu-id="827c1-109">\[nDWords \] de datos: matriz de DWords que contienen los datos de cada elemento de vértice.</span><span class="sxs-lookup"><span data-stu-id="827c1-109">data\[nDWords\] - Array of DWORDS that contain the data in each vertex element.</span></span>

## <a name="see-also"></a><span data-ttu-id="827c1-110">Vea también</span><span class="sxs-lookup"><span data-stu-id="827c1-110">See also</span></span>

<dl> <dt>

<span data-ttu-id="827c1-111">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="827c1-111">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



