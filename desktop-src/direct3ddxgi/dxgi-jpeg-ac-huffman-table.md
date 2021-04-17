---
description: Describe una tabla de formato de CA JPEG.
ms.assetid: E1923FFA-E7E5-4158-9793-3E7F5A6EA7FA
title: DXGI_JPEG_AC_HUFFMAN_TABLE estructura (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_AC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 760840822eb6b9411983c72324bc1e86a3208195
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717717"
---
# <a name="dxgi_jpeg_ac_huffman_table-structure"></a><span data-ttu-id="0b30c-103">Estructura de tabla de gráfico de CA de DXGI \_ JPEG \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="0b30c-103">DXGI\_JPEG\_AC\_HUFFMAN\_TABLE structure</span></span>

<span data-ttu-id="0b30c-104">Describe una tabla de formato de CA JPEG.</span><span class="sxs-lookup"><span data-stu-id="0b30c-104">Describes a JPEG AC huffman table.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b30c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b30c-105">Syntax</span></span>


```C++
typedef struct DXGI_JPEG_AC_HUFFMAN_TABLE {
  BYTE CodeCounts[16];
  BYTE CodeValues[162];
} DXGI_JPEG_AC_HUFFMAN_TABLE;
```



## <a name="members"></a><span data-ttu-id="0b30c-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="0b30c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0b30c-107">**CodeCounts**</span><span class="sxs-lookup"><span data-stu-id="0b30c-107">**CodeCounts**</span></span>
</dt> <dd>

<span data-ttu-id="0b30c-108">El número de códigos para cada longitud de código.</span><span class="sxs-lookup"><span data-stu-id="0b30c-108">The number of codes for each code length.</span></span>

</dd> <dt>

<span data-ttu-id="0b30c-109">**CodeValues**</span><span class="sxs-lookup"><span data-stu-id="0b30c-109">**CodeValues**</span></span>
</dt> <dd>

<span data-ttu-id="0b30c-110">Valores de código de Huffman, en orden de aumento de la longitud del código.</span><span class="sxs-lookup"><span data-stu-id="0b30c-110">The Huffman code values, in order of increasing code length.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b30c-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b30c-111">Requirements</span></span>



| <span data-ttu-id="0b30c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b30c-112">Requirement</span></span> | <span data-ttu-id="0b30c-113">Value</span><span class="sxs-lookup"><span data-stu-id="0b30c-113">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b30c-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b30c-114">Header</span></span><br/> | <dl> <span data-ttu-id="0b30c-115"><dt>Dxgitype. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b30c-115"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b30c-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b30c-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b30c-117">Estructuras de DXGI</span><span class="sxs-lookup"><span data-stu-id="0b30c-117">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




