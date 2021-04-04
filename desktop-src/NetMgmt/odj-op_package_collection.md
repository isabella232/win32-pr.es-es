---
title: OP_PACKAGE_PART_COLLECTION
description: Definición de OP_PACKAGE_PART_COLLECTION IDL
ms.assetid: a7abf011-0335-4869-b4d9-144b2f392241
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8eb61397045a382fe5933025a4eeda2f563e838
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "104078557"
---
# <a name="op_package_part_collection-structure"></a><span data-ttu-id="6769b-103">Estructura de OP_PACKAGE_PART_COLLECTION</span><span class="sxs-lookup"><span data-stu-id="6769b-103">OP_PACKAGE_PART_COLLECTION structure</span></span>

<span data-ttu-id="6769b-104">Especifica una estructura que contiene una matriz de estructuras OP_PACKAGE_PART.</span><span class="sxs-lookup"><span data-stu-id="6769b-104">Specifies a structure that contains an array of OP_PACKAGE_PART structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="6769b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6769b-105">Syntax</span></span>

```C++
typedef struct _OP_PACKAGE_PART_COLLECTION
{
    ULONG                                 cParts;
    [size_is(cParts)]   POP_PACKAGE_PART  pParts;
    OP_BLOB                               Extension;
} OP_PACKAGE_PART_COLLECTION, *POP_PACKAGE_PART_COLLECTION;
```

## <a name="members"></a><span data-ttu-id="6769b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="6769b-106">Members</span></span>

### <a name="cparts"></a><span data-ttu-id="6769b-107">cParts</span><span class="sxs-lookup"><span data-stu-id="6769b-107">cParts</span></span>

<span data-ttu-id="6769b-108">Contiene el número de elementos de pParts.</span><span class="sxs-lookup"><span data-stu-id="6769b-108">Contains the number of elements in pParts.</span></span>

### <a name="pparts"></a><span data-ttu-id="6769b-109">pParts</span><span class="sxs-lookup"><span data-stu-id="6769b-109">pParts</span></span>

<span data-ttu-id="6769b-110">Contiene una matriz de estructuras OP_PACKAGE_PART.</span><span class="sxs-lookup"><span data-stu-id="6769b-110">Contains an array of OP_PACKAGE_PART structures.</span></span>

### <a name="extension"></a><span data-ttu-id="6769b-111">Extensión</span><span class="sxs-lookup"><span data-stu-id="6769b-111">Extension</span></span>

<span data-ttu-id="6769b-112">Reservado para uso futuro y debe establecerse en ceros.</span><span class="sxs-lookup"><span data-stu-id="6769b-112">Reserved for future use and MUST be set to all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="6769b-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="6769b-113">See also</span></span>

[<span data-ttu-id="6769b-114">**Definiciones IDL de unión a dominio sin conexión**</span><span class="sxs-lookup"><span data-stu-id="6769b-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="6769b-115">**\_elemento de paquete de OP \_**</span><span class="sxs-lookup"><span data-stu-id="6769b-115">**OP\_PACKAGE\_PART**</span></span>](odj-op_package_part.md)

[<span data-ttu-id="6769b-116">**BLOB de operaciones \_**</span><span class="sxs-lookup"><span data-stu-id="6769b-116">**OP\_BLOB**</span></span>](odj-op_blob.md)

