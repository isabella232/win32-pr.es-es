---
description: Describe una tabla Huffman de DC JPEG.
ms.assetid: 9D6C18C3-F75C-41E0-9EFA-E882E89DE713
title: DXGI_JPEG_DC_HUFFMAN_TABLE estructura (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_DC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: b2f5f73f7c6def745b987818b9ec30fb3e2752e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280293"
---
# <a name="dxgi_jpeg_dc_huffman_table-structure"></a><span data-ttu-id="ae410-103">\_Estructura de \_ \_ tabla HUFFMAN de DC JPEG de DXGI \_</span><span class="sxs-lookup"><span data-stu-id="ae410-103">DXGI\_JPEG\_DC\_HUFFMAN\_TABLE structure</span></span>

<span data-ttu-id="ae410-104">Describe una tabla Huffman de DC JPEG.</span><span class="sxs-lookup"><span data-stu-id="ae410-104">Describes a JPEG DC huffman table.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae410-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae410-105">Syntax</span></span>


```C++
typedef struct DXGI_JPEG_DC_HUFFMAN_TABLE {
  BYTE CodeCounts[12];
  BYTE CodeValues[12];
} DXGI_JPEG_DC_HUFFMAN_TABLE;
```



## <a name="members"></a><span data-ttu-id="ae410-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ae410-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ae410-107">**CodeCounts**</span><span class="sxs-lookup"><span data-stu-id="ae410-107">**CodeCounts**</span></span>
</dt> <dd>

<span data-ttu-id="ae410-108">El número de códigos para cada longitud de código.</span><span class="sxs-lookup"><span data-stu-id="ae410-108">The number of codes for each code length.</span></span>

</dd> <dt>

<span data-ttu-id="ae410-109">**CodeValues**</span><span class="sxs-lookup"><span data-stu-id="ae410-109">**CodeValues**</span></span>
</dt> <dd>

<span data-ttu-id="ae410-110">Valores de código de Huffman, en orden de aumento de la longitud del código.</span><span class="sxs-lookup"><span data-stu-id="ae410-110">The Huffman code values, in order of increasing code length.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae410-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae410-111">Requirements</span></span>



| <span data-ttu-id="ae410-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae410-112">Requirement</span></span> | <span data-ttu-id="ae410-113">Value</span><span class="sxs-lookup"><span data-stu-id="ae410-113">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae410-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae410-114">Header</span></span><br/> | <dl> <span data-ttu-id="ae410-115"><dt>Dxgitype. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae410-115"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae410-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae410-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae410-117">Estructuras de DXGI</span><span class="sxs-lookup"><span data-stu-id="ae410-117">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




