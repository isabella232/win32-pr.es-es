---
description: Marcas usadas para obtener información de devolución de llamada.
ms.assetid: e8126ff0-db23-4da6-a999-0efb8c2647da
title: Enumeración D3DXCALLBACK_SEARCH_FLAGS (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCALLBACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: d3302b79734557a5c1f2082ec2a4e95c03790f4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083742"
---
# <a name="d3dxcallback_search_flags-enumeration"></a><span data-ttu-id="447ae-103">\_Enumeración de marcas de búsqueda de D3DXCALLBACK \_</span><span class="sxs-lookup"><span data-stu-id="447ae-103">D3DXCALLBACK\_SEARCH\_FLAGS enumeration</span></span>

<span data-ttu-id="447ae-104">Marcas usadas para obtener información de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="447ae-104">Flags used to obtain callback information.</span></span>

## <a name="syntax"></a><span data-ttu-id="447ae-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="447ae-105">Syntax</span></span>


```C++
typedef enum D3DXCALLBACK_SEARCH_FLAGS { 
  D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION  = 1,
  D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION     = 2,
  D3DXCALLBACK_SEARCH_FORCE_DWORD                 = 0x7fffffff
} D3DXCALLBACK_SEARCH_FLAGS, *LPD3DXCALLBACK_SEARCH_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="447ae-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="447ae-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="447ae-107"><span id="D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION"></span><span id="d3dxcallback_search_excluding_initial_position"></span>**D3DXCALLBACK \_ búsqueda \_ excluyendo la \_ \_ posición inicial**</span><span class="sxs-lookup"><span data-stu-id="447ae-107"><span id="D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION"></span><span id="d3dxcallback_search_excluding_initial_position"></span>**D3DXCALLBACK\_SEARCH\_EXCLUDING\_INITIAL\_POSITION**</span></span>
</dt> <dd>

<span data-ttu-id="447ae-108">Excluya las devoluciones de llamada ubicadas en la posición inicial de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="447ae-108">Exclude callbacks located at the initial position from the search.</span></span>

</dd> <dt>

<span data-ttu-id="447ae-109"><span id="D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION"></span><span id="d3dxcallback_search_behind_initial_position"></span>**D3DXCALLBACK \_ Buscar \_ detrás de la \_ \_ posición inicial**</span><span class="sxs-lookup"><span data-stu-id="447ae-109"><span id="D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION"></span><span id="d3dxcallback_search_behind_initial_position"></span>**D3DXCALLBACK\_SEARCH\_BEHIND\_INITIAL\_POSITION**</span></span>
</dt> <dd>

<span data-ttu-id="447ae-110">Invertir la dirección de búsqueda de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="447ae-110">Reverse the callback search direction.</span></span>

</dd> <dt>

<span data-ttu-id="447ae-111"><span id="D3DXCALLBACK_SEARCH_FORCE_DWORD"></span><span id="d3dxcallback_search_force_dword"></span>**D3DXCALLBACK \_ de \_ forzar búsqueda en \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="447ae-111"><span id="D3DXCALLBACK_SEARCH_FORCE_DWORD"></span><span id="d3dxcallback_search_force_dword"></span>**D3DXCALLBACK\_SEARCH\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="447ae-112">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="447ae-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="447ae-113">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="447ae-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="447ae-114">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="447ae-114">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="447ae-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="447ae-115">Requirements</span></span>



| <span data-ttu-id="447ae-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="447ae-116">Requirement</span></span> | <span data-ttu-id="447ae-117">Value</span><span class="sxs-lookup"><span data-stu-id="447ae-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="447ae-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="447ae-118">Header</span></span><br/> | <dl> <span data-ttu-id="447ae-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="447ae-119"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="447ae-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="447ae-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="447ae-121">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="447ae-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




