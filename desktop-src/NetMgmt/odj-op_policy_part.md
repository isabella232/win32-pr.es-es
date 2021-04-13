---
title: OP_POLICY_PART
description: Definición de OP_POLICY_PART IDL
ms.assetid: 3988b298-b21d-4476-bfa5-ac606bcbd6c8
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: ef0e3b96ce564ed7ff8e2ce0886e33ca474a1cf8
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "104421569"
---
# <a name="op_policy_part-structure"></a><span data-ttu-id="f6893-103">Estructura de OP_POLICY_PART</span><span class="sxs-lookup"><span data-stu-id="f6893-103">OP_POLICY_PART structure</span></span>

<span data-ttu-id="f6893-104">Contiene una matriz de estructuras OP_POLICY_ELEMENT_LIST.</span><span class="sxs-lookup"><span data-stu-id="f6893-104">Contains an array of OP_POLICY_ELEMENT_LIST structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6893-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6893-105">Syntax</span></span>

```C++
typedef struct _OP_POLICY_PART
{
    ULONG                                       cElementLists;
    [size_is(cElementLists)]
                        POP_POLICY_ELEMENT_LIST pElementLists;
    OP_BLOB                                     Extension;
} OP_POLICY_PART, *POP_POLICY_PART;
```

## <a name="members"></a><span data-ttu-id="f6893-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="f6893-106">Members</span></span>

### <a name="celementlists"></a><span data-ttu-id="f6893-107">cElementLists</span><span class="sxs-lookup"><span data-stu-id="f6893-107">cElementLists</span></span>

<span data-ttu-id="f6893-108">Contiene el número de elementos de pElementLists.</span><span class="sxs-lookup"><span data-stu-id="f6893-108">Contains the number of elements in pElementLists.</span></span>

### <a name="pelementlists"></a><span data-ttu-id="f6893-109">pElementLists</span><span class="sxs-lookup"><span data-stu-id="f6893-109">pElementLists</span></span>

<span data-ttu-id="f6893-110">Contiene una matriz de estructuras OP_POLICY_ELEMENT_LIST.</span><span class="sxs-lookup"><span data-stu-id="f6893-110">Contains an array of OP_POLICY_ELEMENT_LIST structures.</span></span>

### <a name="extension"></a><span data-ttu-id="f6893-111">Extensión</span><span class="sxs-lookup"><span data-stu-id="f6893-111">Extension</span></span>

<span data-ttu-id="f6893-112">Reservado para uso futuro y debe contener ceros.</span><span class="sxs-lookup"><span data-stu-id="f6893-112">Reserved for future use and must contain all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6893-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6893-113">See also</span></span>

[<span data-ttu-id="f6893-114">**Definiciones IDL de unión a dominio sin conexión**</span><span class="sxs-lookup"><span data-stu-id="f6893-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="f6893-115">**\_lista de \_ elementos de directiva de OP \_**</span><span class="sxs-lookup"><span data-stu-id="f6893-115">**OP\_POLICY\_ELEMENT\_LIST**</span></span>](odj-op_policy_element_list.md)
