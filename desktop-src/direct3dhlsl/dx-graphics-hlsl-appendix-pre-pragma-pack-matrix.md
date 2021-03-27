---
title: pack_matrix Directiva pragma
description: Directiva pragma que especifica la alineación de empaquetado para matrices.
ms.assetid: e77dc007-d915-4d78-9fff-d44d4999e4da
keywords:
- pack_matrix pragma Directive HLSL
topic_type:
- apiref
api_name:
- pack_matrix pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4bb5474702a1caba3f772002c34677601715caff
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076747"
---
# <a name="pack_matrix-pragma-directive"></a><span data-ttu-id="2e62c-104">\_instrucción pragma Matrix (Directiva)</span><span class="sxs-lookup"><span data-stu-id="2e62c-104">pack\_matrix pragma Directive</span></span>

<span data-ttu-id="2e62c-105">Directiva pragma que especifica la alineación de empaquetado para matrices.</span><span class="sxs-lookup"><span data-stu-id="2e62c-105">Pragma directive that specifies packing alignment for matrices.</span></span>



| <span data-ttu-id="2e62c-106">\#matriz de pragma Pack \_ ( *alignment* )</span><span class="sxs-lookup"><span data-stu-id="2e62c-106">\#pragma pack\_matrix( *alignment* )</span></span> |
|--------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="2e62c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e62c-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2e62c-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="2e62c-108">Item</span></span></th>
<th><span data-ttu-id="2e62c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e62c-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2e62c-110"><span id="alignment"></span><span id="ALIGNMENT"></span><em>ecuación</em></span><span class="sxs-lookup"><span data-stu-id="2e62c-110"><span id="alignment"></span><span id="ALIGNMENT"></span><em>alignment</em></span></span><br/></td>
<td><span data-ttu-id="2e62c-111">Alineación que se va a establecer para las matrices.</span><span class="sxs-lookup"><span data-stu-id="2e62c-111">Alignment to set for matrices.</span></span> <span data-ttu-id="2e62c-112">Este parámetro puede tomar uno de los valores enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2e62c-112">This parameter can take one of the values listed in the following table.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2e62c-113">Value</span><span class="sxs-lookup"><span data-stu-id="2e62c-113">Value</span></span></th>
<th><span data-ttu-id="2e62c-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e62c-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2e62c-115">column_major</span><span class="sxs-lookup"><span data-stu-id="2e62c-115">column_major</span></span></td>
<td><span data-ttu-id="2e62c-116">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2e62c-116">Default.</span></span> <span data-ttu-id="2e62c-117">Establece la alineación de empaquetado de la matriz en la columna principal.</span><span class="sxs-lookup"><span data-stu-id="2e62c-117">Sets the matrix packing alignment to column major.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2e62c-118">row_major</span><span class="sxs-lookup"><span data-stu-id="2e62c-118">row_major</span></span></td>
<td><span data-ttu-id="2e62c-119">Establece la alineación de empaquetado de matriz en la fila principal.</span><span class="sxs-lookup"><span data-stu-id="2e62c-119">Sets the matrix packing alignment to row major.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="2e62c-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2e62c-120">Examples</span></span>

<span data-ttu-id="2e62c-121">En el ejemplo siguiente se establece la alineación de empaquetado de matriz en la fila principal.</span><span class="sxs-lookup"><span data-stu-id="2e62c-121">The following example sets the matrix packing alignment to row major.</span></span>


```
#pragma pack_matrix( row_major )
```



## <a name="see-also"></a><span data-ttu-id="2e62c-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e62c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e62c-123">Directivas de preprocesador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2e62c-123">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="2e62c-124">\#pragma (Directiva) (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2e62c-124">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





