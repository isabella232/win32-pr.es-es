---
description: Esta macro crea un valor que usa el problema para emitir un final de la consulta.
ms.assetid: 9ced932a-5d98-4bf8-aa11-06560f53546d
title: D3DISSUE_END (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DISSUE_END
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 7a448346bdc5dcfbbca4cf0d55273bdadc2fdcbb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362616"
---
# <a name="d3dissue_end"></a><span data-ttu-id="73a2a-103">Final de D3DISSUE \_</span><span class="sxs-lookup"><span data-stu-id="73a2a-103">D3DISSUE\_END</span></span>

<span data-ttu-id="73a2a-104">Esta macro crea un valor que usa el [**problema**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) para emitir un final de la consulta.</span><span class="sxs-lookup"><span data-stu-id="73a2a-104">This macro creates a value used by [**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) to issue a query end.</span></span>

``` syntax
#define D3DISSUE_END (1 << 0)
```

## <a name="parameters"></a><span data-ttu-id="73a2a-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73a2a-105">Parameters</span></span>





 

## <a name="remarks"></a><span data-ttu-id="73a2a-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73a2a-106">Remarks</span></span>

<span data-ttu-id="73a2a-107">Esta macro cambia el estado de la consulta a no señalado.</span><span class="sxs-lookup"><span data-stu-id="73a2a-107">This macro changes the query state to nonsignaled.</span></span>

<span data-ttu-id="73a2a-108">D3DISSUE \_ End es válido para los siguientes tipos de consulta.</span><span class="sxs-lookup"><span data-stu-id="73a2a-108">D3DISSUE\_END is valid for the following query types.</span></span>

-   <span data-ttu-id="73a2a-109">D3DQUERYTYPE \_ VCACHE</span><span class="sxs-lookup"><span data-stu-id="73a2a-109">D3DQUERYTYPE\_VCACHE</span></span>
-   <span data-ttu-id="73a2a-110">D3DQUERYTYPE \_ ResourceManager</span><span class="sxs-lookup"><span data-stu-id="73a2a-110">D3DQUERYTYPE\_ResourceManager</span></span>
-   <span data-ttu-id="73a2a-111">D3DQUERYTYPE \_ VERTEXSTATS</span><span class="sxs-lookup"><span data-stu-id="73a2a-111">D3DQUERYTYPE\_VERTEXSTATS</span></span>
-   <span data-ttu-id="73a2a-112">\_Evento D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="73a2a-112">D3DQUERYTYPE\_EVENT</span></span>
-   <span data-ttu-id="73a2a-113">Oclusión de D3DQUERYTYPE \_</span><span class="sxs-lookup"><span data-stu-id="73a2a-113">D3DQUERYTYPE\_OCCLUSION</span></span>

## <a name="requirements"></a><span data-ttu-id="73a2a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73a2a-114">Requirements</span></span>



| <span data-ttu-id="73a2a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="73a2a-115">Requirement</span></span> | <span data-ttu-id="73a2a-116">Value</span><span class="sxs-lookup"><span data-stu-id="73a2a-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73a2a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73a2a-117">Header</span></span><br/> | <dl> <span data-ttu-id="73a2a-118"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="73a2a-118"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73a2a-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="73a2a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73a2a-120">Macros</span><span class="sxs-lookup"><span data-stu-id="73a2a-120">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="73a2a-121">**Inicio de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="73a2a-121">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md)
</dt> <dt>

[<span data-ttu-id="73a2a-122">**D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="73a2a-122">**D3DQUERYTYPE**</span></span>](./d3dquerytype.md)
</dt> </dl>

 

 
