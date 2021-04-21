---
UID: NS:directml.DML_SCALAR_UNION
title: DML_SCALAR_UNION
description: Unión de tipos escalares.
helpviewer_keywords:
- DML_SCALAR_UNION
- DML_SCALAR_UNION structure
- direct3d12.dml_scalar_union
- directml/DML_SCALAR_UNION
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
ms.keywords: DML_SCALAR_UNION, DML_SCALAR_UNION structure, direct3d12.dml_scalar_union, directml/DML_SCALAR_UNION
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_SCALAR_UNION
- directml/DML_SCALAR_UNION
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_SCALAR_UNION
ms.openlocfilehash: d53ec7025d3da5a07a648849e366d436755ad3f1
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803962"
---
# <a name="dml_scalar_union-union-directmlh"></a><span data-ttu-id="9d5e1-103">DML_SCALAR_UNION unión (directml.h)</span><span class="sxs-lookup"><span data-stu-id="9d5e1-103">DML_SCALAR_UNION union (directml.h)</span></span>
<span data-ttu-id="9d5e1-104">Unión de tipos escalares.</span><span class="sxs-lookup"><span data-stu-id="9d5e1-104">A union of scalar types.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9d5e1-105">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="9d5e1-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="9d5e1-106">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="9d5e1-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9d5e1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d5e1-107">Syntax</span></span>
```cpp
union DML_SCALAR_UNION {
  BYTE   Bytes[8];
  INT8   Int8;
  UINT8  UInt8;
  INT16  Int16;
  UINT16 UInt16;
  INT32  Int32;
  UINT32 UInt32;
  INT64  Int64;
  UINT64 UInt64;
  FLOAT  Float32;
  DOUBLE Float64;
};
```



## <a name="members"></a><span data-ttu-id="9d5e1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="9d5e1-108">Members</span></span>

`Bytes`

<span data-ttu-id="9d5e1-109">Matriz de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="9d5e1-109">An 8-byte array.</span></span>


`Int8`

<span data-ttu-id="9d5e1-110">Entero de 8 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="9d5e1-110">An 8-bit signed integer.</span></span>


`UInt8`

<span data-ttu-id="9d5e1-111">Entero de 8 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="9d5e1-111">An 8-bit unsigned integer.</span></span>


`Int16`

<span data-ttu-id="9d5e1-112">Entero de 16 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="9d5e1-112">A 16-bit signed integer.</span></span>


`UInt16`

<span data-ttu-id="9d5e1-113">Entero de 16 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="9d5e1-113">A 16-bit unsigned integer.</span></span>


`Int32`

<span data-ttu-id="9d5e1-114">Entero de 32 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="9d5e1-114">A 32-bit signed integer.</span></span>


`UInt32`

<span data-ttu-id="9d5e1-115">Entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="9d5e1-115">A 32-bit unsigned integer.</span></span>


`Int64`

<span data-ttu-id="9d5e1-116">Entero de 64 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="9d5e1-116">A 64-bit signed integer.</span></span>


`UInt64`

<span data-ttu-id="9d5e1-117">Entero de 64 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="9d5e1-117">A 64-bit unsigned integer.</span></span>


`Float32`

<span data-ttu-id="9d5e1-118">Número de punto flotante de precisión sencilla.</span><span class="sxs-lookup"><span data-stu-id="9d5e1-118">A single precision floating-point number.</span></span>


`Float64`

<span data-ttu-id="9d5e1-119">Número de punto flotante de precisión doble.</span><span class="sxs-lookup"><span data-stu-id="9d5e1-119">A double precision floating-point number.</span></span>



## <a name="requirements"></a><span data-ttu-id="9d5e1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d5e1-120">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9d5e1-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="9d5e1-121">**Header**</span></span> | <span data-ttu-id="9d5e1-122">directml.h</span><span class="sxs-lookup"><span data-stu-id="9d5e1-122">directml.h</span></span> |