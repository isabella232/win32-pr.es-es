---
description: Define el tipo de modos de bucle set de animación que se usan para la reproducción.
ms.assetid: 2ce26bf0-2b33-4193-a58f-03493a051351
title: Enumeración D3DXPLAYBACK_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLAYBACK_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0ce95b4765ec678c43c8e0ed92008deeb9927298
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914717"
---
# <a name="d3dxplayback_type-enumeration"></a><span data-ttu-id="6c75d-103">\_Enumeración de tipo D3DXPLAYBACK</span><span class="sxs-lookup"><span data-stu-id="6c75d-103">D3DXPLAYBACK\_TYPE enumeration</span></span>

<span data-ttu-id="6c75d-104">Define el tipo de modos de bucle set de animación que se usan para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="6c75d-104">Defines the type of animation set looping modes used for playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c75d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c75d-105">Syntax</span></span>


```C++
typedef enum D3DXPLAYBACK_TYPE { 
  D3DXPLAY_LOOP         = 0,
  D3DXPLAY_ONCE         = 1,
  D3DXPLAY_PINGPONG     = 2,
  D3DXPLAY_FORCE_DWORD  = 0x7fffffff
} D3DXPLAYBACK_TYPE, *LPD3DXPLAYBACK_TYPE;
```



## <a name="constants"></a><span data-ttu-id="6c75d-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="6c75d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6c75d-107"><span id="D3DXPLAY_LOOP"></span><span id="d3dxplay_loop"></span>**\_Bucle D3DXPLAY**</span><span class="sxs-lookup"><span data-stu-id="6c75d-107"><span id="D3DXPLAY_LOOP"></span><span id="d3dxplay_loop"></span>**D3DXPLAY\_LOOP**</span></span>
</dt> <dd>

<span data-ttu-id="6c75d-108">La animación se repite indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="6c75d-108">The animation repeats endlessly.</span></span>

</dd> <dt>

<span data-ttu-id="6c75d-109"><span id="D3DXPLAY_ONCE"></span><span id="d3dxplay_once"></span>**D3DXPLAY \_ una vez**</span><span class="sxs-lookup"><span data-stu-id="6c75d-109"><span id="D3DXPLAY_ONCE"></span><span id="d3dxplay_once"></span>**D3DXPLAY\_ONCE**</span></span>
</dt> <dd>

<span data-ttu-id="6c75d-110">La animación se reproduce una vez y luego se detiene en el último fotograma.</span><span class="sxs-lookup"><span data-stu-id="6c75d-110">The animation plays once, and then it stops on the last frame.</span></span>

</dd> <dt>

<span data-ttu-id="6c75d-111"><span id="D3DXPLAY_PINGPONG"></span><span id="d3dxplay_pingpong"></span>**D3DXPLAY \_ PINGPONG**</span><span class="sxs-lookup"><span data-stu-id="6c75d-111"><span id="D3DXPLAY_PINGPONG"></span><span id="d3dxplay_pingpong"></span>**D3DXPLAY\_PINGPONG**</span></span>
</dt> <dd>

<span data-ttu-id="6c75d-112">La animación alterna infinitamente entre la reproducción hacia delante y la reproducción hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="6c75d-112">The animation alternates endlessly between playing forward and playing backward.</span></span>

</dd> <dt>

<span data-ttu-id="6c75d-113"><span id="D3DXPLAY_FORCE_DWORD"></span><span id="d3dxplay_force_dword"></span>**D3DXPLAY \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6c75d-113"><span id="D3DXPLAY_FORCE_DWORD"></span><span id="d3dxplay_force_dword"></span>**D3DXPLAY\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="6c75d-114">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="6c75d-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="6c75d-115">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6c75d-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="6c75d-116">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="6c75d-116">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c75d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c75d-117">Requirements</span></span>



| <span data-ttu-id="6c75d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c75d-118">Requirement</span></span> | <span data-ttu-id="6c75d-119">Value</span><span class="sxs-lookup"><span data-stu-id="6c75d-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c75d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c75d-120">Header</span></span><br/> | <dl> <span data-ttu-id="6c75d-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c75d-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c75d-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c75d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c75d-123">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="6c75d-123">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




