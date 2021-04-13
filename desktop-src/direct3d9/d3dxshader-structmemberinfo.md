---
description: Estructura auxiliar que contiene información sobre la estructura de los miembros.
ms.assetid: 2fbe5e97-047e-48bf-9413-dd297632288a
title: D3DXSHADER_STRUCTMEMBERINFO estructura (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_STRUCTMEMBERINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 01782331459956c0878b46861db0d4f11e19c7dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362524"
---
# <a name="d3dxshader_structmemberinfo-structure"></a><span data-ttu-id="9a213-103">D3DXSHADER \_ estructura STRUCTMEMBERINFO</span><span class="sxs-lookup"><span data-stu-id="9a213-103">D3DXSHADER\_STRUCTMEMBERINFO structure</span></span>

<span data-ttu-id="9a213-104">Estructura auxiliar que contiene información sobre la estructura de los miembros.</span><span class="sxs-lookup"><span data-stu-id="9a213-104">A helper structure containing member structure information.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a213-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a213-105">Syntax</span></span>


```C++
typedef struct D3DXSHADER_STRUCTMEMBERINFO {
  DWORD Name;
  DWORD TypeInfo;
} D3DXSHADER_STRUCTMEMBERINFO, *LPD3DXSHADER_STRUCTMEMBERINFO;
```



## <a name="members"></a><span data-ttu-id="9a213-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="9a213-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9a213-107">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="9a213-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="9a213-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a213-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9a213-109">Desplazamiento desde el principio de esta estructura, en bytes, a la cadena que contiene el nombre del miembro de estructura.</span><span class="sxs-lookup"><span data-stu-id="9a213-109">Offset from the beginning of this structure, in bytes, to the string that contains the structure member name.</span></span>

</dd> <dt>

<span data-ttu-id="9a213-110">**Requerida**</span><span class="sxs-lookup"><span data-stu-id="9a213-110">**TypeInfo**</span></span>
</dt> <dd>

<span data-ttu-id="9a213-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a213-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9a213-112">Desplazamiento desde el principio de esta estructura, en bytes, a la cadena que contiene la información de tipo.</span><span class="sxs-lookup"><span data-stu-id="9a213-112">Offset from the beginning of this structure, in bytes, to the string that contains the type information.</span></span> <span data-ttu-id="9a213-113">Consulte [**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md).</span><span class="sxs-lookup"><span data-stu-id="9a213-113">See [**D3DXSHADER\_TYPEINFO**](d3dxshader-typeinfo.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9a213-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a213-114">Requirements</span></span>



| <span data-ttu-id="9a213-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a213-115">Requirement</span></span> | <span data-ttu-id="9a213-116">Value</span><span class="sxs-lookup"><span data-stu-id="9a213-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a213-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a213-117">Header</span></span><br/> | <dl> <span data-ttu-id="9a213-118"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a213-118"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a213-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a213-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a213-120">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="9a213-120">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="9a213-121">**D3DXSHADER \_ TYPEINFO**</span><span class="sxs-lookup"><span data-stu-id="9a213-121">**D3DXSHADER\_TYPEINFO**</span></span>](d3dxshader-typeinfo.md)
</dt> </dl>

 

 
