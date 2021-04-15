---
description: Contiene datos de rampa rojo, verde y azul.
ms.assetid: c596f47a-6c09-4b97-ab2f-b1da3d851aa4
title: Estructura D3DGAMMARAMP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DGAMMARAMP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 496885b8267d339c7617ec24b884fa193f8d9945
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707939"
---
# <a name="d3dgammaramp-structure"></a><span data-ttu-id="d607d-103">Estructura D3DGAMMARAMP</span><span class="sxs-lookup"><span data-stu-id="d607d-103">D3DGAMMARAMP structure</span></span>

<span data-ttu-id="d607d-104">Contiene datos de rampa rojo, verde y azul.</span><span class="sxs-lookup"><span data-stu-id="d607d-104">Contains red, green, and blue ramp data.</span></span>

## <a name="syntax"></a><span data-ttu-id="d607d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d607d-105">Syntax</span></span>


```C++
typedef struct D3DGAMMARAMP {
  WORD red[256];
  WORD green[256];
  WORD blue[256];
} D3DGAMMARAMP, *LPD3DGAMMARAMP;
```



## <a name="members"></a><span data-ttu-id="d607d-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d607d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d607d-107">**alerta**</span><span class="sxs-lookup"><span data-stu-id="d607d-107">**red**</span></span>
</dt> <dd>

<span data-ttu-id="d607d-108">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d607d-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d607d-109">Matriz de 256 elemento de WORD que describe la rampa gamma roja.</span><span class="sxs-lookup"><span data-stu-id="d607d-109">Array of 256 WORD element that describes the red gamma ramp.</span></span>

</dd> <dt>

<span data-ttu-id="d607d-110">**verde**</span><span class="sxs-lookup"><span data-stu-id="d607d-110">**green**</span></span>
</dt> <dd>

<span data-ttu-id="d607d-111">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d607d-111">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d607d-112">Matriz de 256 elemento de WORD que describe la rampa gamma verde.</span><span class="sxs-lookup"><span data-stu-id="d607d-112">Array of 256 WORD element that describes the green gamma ramp.</span></span>

</dd> <dt>

<span data-ttu-id="d607d-113">**azul**</span><span class="sxs-lookup"><span data-stu-id="d607d-113">**blue**</span></span>
</dt> <dd>

<span data-ttu-id="d607d-114">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d607d-114">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d607d-115">Matriz de 256 elemento de WORD que describe la rampa gamma azul.</span><span class="sxs-lookup"><span data-stu-id="d607d-115">Array of 256 WORD element that describes the blue gamma ramp.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d607d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d607d-116">Requirements</span></span>



| <span data-ttu-id="d607d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d607d-117">Requirement</span></span> | <span data-ttu-id="d607d-118">Value</span><span class="sxs-lookup"><span data-stu-id="d607d-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d607d-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d607d-119">Header</span></span><br/> | <dl> <span data-ttu-id="d607d-120"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d607d-120"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d607d-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="d607d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d607d-122">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="d607d-122">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="d607d-123">**GetGammaRamp**</span><span class="sxs-lookup"><span data-stu-id="d607d-123">**GetGammaRamp**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
</dt> <dt>

[<span data-ttu-id="d607d-124">**SetGammaRamp**</span><span class="sxs-lookup"><span data-stu-id="d607d-124">**SetGammaRamp**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
</dt> </dl>

 

 
