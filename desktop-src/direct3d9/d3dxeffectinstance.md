---
description: Tipo de datos para administrar un conjunto de parámetros de efectos predeterminados.
ms.assetid: a3408c0b-b4a6-47b1-b12e-594c13bd3a7d
title: Estructura D3DXEFFECTINSTANCE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTINSTANCE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 6874da0fd04b34036152d58e94b16006e185e117
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362576"
---
# <a name="d3dxeffectinstance-structure"></a><span data-ttu-id="e0bec-103">Estructura D3DXEFFECTINSTANCE</span><span class="sxs-lookup"><span data-stu-id="e0bec-103">D3DXEFFECTINSTANCE structure</span></span>

<span data-ttu-id="e0bec-104">Tipo de datos para administrar un conjunto de parámetros de efectos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="e0bec-104">Data type for managing a set of default effect parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0bec-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0bec-105">Syntax</span></span>


```C++
typedef struct D3DXEFFECTINSTANCE {
  LPSTR               pEffectFilename;
  DWORD               NumDefaults;
  LPD3DXEFFECTDEFAULT pDefaults;
} D3DXEFFECTINSTANCE, *LPD3DXEFFECTINSTANCE;
```



## <a name="members"></a><span data-ttu-id="e0bec-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="e0bec-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e0bec-107">**pEffectFilename**</span><span class="sxs-lookup"><span data-stu-id="e0bec-107">**pEffectFilename**</span></span>
</dt> <dd>

<span data-ttu-id="e0bec-108">Tipo: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="e0bec-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="e0bec-109">Nombre del archivo de efectos.</span><span class="sxs-lookup"><span data-stu-id="e0bec-109">Name of the effect file.</span></span>

</dd> <dt>

<span data-ttu-id="e0bec-110">**NumDefaults**</span><span class="sxs-lookup"><span data-stu-id="e0bec-110">**NumDefaults**</span></span>
</dt> <dd>

<span data-ttu-id="e0bec-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0bec-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e0bec-112">Número de parámetros predeterminados.</span><span class="sxs-lookup"><span data-stu-id="e0bec-112">Number of default parameters.</span></span>

</dd> <dt>

<span data-ttu-id="e0bec-113">**pDefaults**</span><span class="sxs-lookup"><span data-stu-id="e0bec-113">**pDefaults**</span></span>
</dt> <dd>

<span data-ttu-id="e0bec-114">Tipo: **[ **LPD3DXEFFECTDEFAULT**](d3dxeffectdefault.md)**</span><span class="sxs-lookup"><span data-stu-id="e0bec-114">Type: **[**LPD3DXEFFECTDEFAULT**](d3dxeffectdefault.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e0bec-115">Puntero a una matriz de elementos [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md) , cada uno de los cuales contiene un parámetro Effect.</span><span class="sxs-lookup"><span data-stu-id="e0bec-115">Pointer to an array of [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md) elements, each of which contains an effect parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e0bec-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0bec-116">Requirements</span></span>



| <span data-ttu-id="e0bec-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0bec-117">Requirement</span></span> | <span data-ttu-id="e0bec-118">Value</span><span class="sxs-lookup"><span data-stu-id="e0bec-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0bec-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0bec-119">Header</span></span><br/> | <dl> <span data-ttu-id="e0bec-120"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0bec-120"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0bec-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0bec-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0bec-122">Estructuras de efectos</span><span class="sxs-lookup"><span data-stu-id="e0bec-122">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
