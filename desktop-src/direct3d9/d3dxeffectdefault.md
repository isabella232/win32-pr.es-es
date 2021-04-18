---
description: Parámetros predeterminados de efecto.
ms.assetid: a8a24cf2-0ecd-4429-97d3-086ff49540a1
title: Estructura D3DXEFFECTDEFAULT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: fee415cbd7d8ec28daa079dd2f224949402a813b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698254"
---
# <a name="d3dxeffectdefault-structure"></a><span data-ttu-id="80aae-103">Estructura D3DXEFFECTDEFAULT</span><span class="sxs-lookup"><span data-stu-id="80aae-103">D3DXEFFECTDEFAULT structure</span></span>

<span data-ttu-id="80aae-104">Parámetros predeterminados de efecto.</span><span class="sxs-lookup"><span data-stu-id="80aae-104">Effect default parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="80aae-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80aae-105">Syntax</span></span>


```C++
typedef struct D3DXEFFECTDEFAULT {
  LPSTR                 pParamName;
  D3DXEFFECTDEFAULTTYPE Type;
  DWORD                 NumBytes;
  LPVOID                pValue;
} D3DXEFFECTDEFAULT, *LPD3DXEFFECTDEFAULT;
```



## <a name="members"></a><span data-ttu-id="80aae-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="80aae-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="80aae-107">**pParamName**</span><span class="sxs-lookup"><span data-stu-id="80aae-107">**pParamName**</span></span>
</dt> <dd>

<span data-ttu-id="80aae-108">Tipo: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="80aae-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="80aae-109">Nombre del parámetro.</span><span class="sxs-lookup"><span data-stu-id="80aae-109">Parameter name.</span></span>

</dd> <dt>

<span data-ttu-id="80aae-110">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="80aae-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="80aae-111">Tipo: **[ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)**</span><span class="sxs-lookup"><span data-stu-id="80aae-111">Type: **[**D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="80aae-112">Tipo de datos de pValue.</span><span class="sxs-lookup"><span data-stu-id="80aae-112">Data type in pValue.</span></span> <span data-ttu-id="80aae-113">Para obtener más información, consulte [ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)</span><span class="sxs-lookup"><span data-stu-id="80aae-113">For more information, see [**D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)</span></span>

</dd> <dt>

<span data-ttu-id="80aae-114">**NumBytes**</span><span class="sxs-lookup"><span data-stu-id="80aae-114">**NumBytes**</span></span>
</dt> <dd>

<span data-ttu-id="80aae-115">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80aae-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="80aae-116">Tamaño, en bytes, de los datos a los que señala pValue.</span><span class="sxs-lookup"><span data-stu-id="80aae-116">Size, in bytes, of the data pointed to by pValue.</span></span>

</dd> <dt>

<span data-ttu-id="80aae-117">**pValue**</span><span class="sxs-lookup"><span data-stu-id="80aae-117">**pValue**</span></span>
</dt> <dd>

<span data-ttu-id="80aae-118">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80aae-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="80aae-119">Puntero a la ubicación de memoria que contiene los datos.</span><span class="sxs-lookup"><span data-stu-id="80aae-119">Pointer to the memory location that contains the data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80aae-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80aae-120">Requirements</span></span>



| <span data-ttu-id="80aae-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="80aae-121">Requirement</span></span> | <span data-ttu-id="80aae-122">Value</span><span class="sxs-lookup"><span data-stu-id="80aae-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80aae-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80aae-123">Header</span></span><br/> | <dl> <span data-ttu-id="80aae-124"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="80aae-124"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80aae-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="80aae-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80aae-126">Estructuras de efectos</span><span class="sxs-lookup"><span data-stu-id="80aae-126">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
