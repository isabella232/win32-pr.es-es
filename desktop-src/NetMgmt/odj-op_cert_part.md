---
title: OP_CERT_PART
description: Definición de OP_CERT_PART IDL
ms.assetid: 30492801-f26e-447f-bcbf-d1108e7ae524
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: feb4f05171204442085f7d69691aa010d13e6042
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "105720191"
---
# <a name="op_cert_part-structure"></a><span data-ttu-id="5941c-103">Estructura de OP_CERT_PART</span><span class="sxs-lookup"><span data-stu-id="5941c-103">OP_CERT_PART structure</span></span>

<span data-ttu-id="5941c-104">Contiene los almacenes de certificados y PFX serializados.</span><span class="sxs-lookup"><span data-stu-id="5941c-104">Contains serialized PFX and certificate stores.</span></span>

## <a name="syntax"></a><span data-ttu-id="5941c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5941c-105">Syntax</span></span>

```C++
typedef struct _OP_CERT_PART
{
    ULONG                                       cPfxStores;
    [size_is(cPfxStores)]   POP_CERT_PFX_STORE  pPfxStores;
    ULONG                                       cSstStores;
    [size_is(cSstStores)]   POP_CERT_SST_STORE  pSstStores;
    OP_BLOB                                     Extension;
} OP_CERT_PART, *POP_CERT_PART;
```

## <a name="members"></a><span data-ttu-id="5941c-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="5941c-106">Members</span></span>

### <a name="cpfxstores"></a><span data-ttu-id="5941c-107">cPfxStores</span><span class="sxs-lookup"><span data-stu-id="5941c-107">cPfxStores</span></span>

<span data-ttu-id="5941c-108">Contiene el número de elementos de pPfxStores.</span><span class="sxs-lookup"><span data-stu-id="5941c-108">Contains the number of elements in pPfxStores.</span></span>

### <a name="ppfxstores"></a><span data-ttu-id="5941c-109">pPfxStores</span><span class="sxs-lookup"><span data-stu-id="5941c-109">pPfxStores</span></span>

<span data-ttu-id="5941c-110">Contiene una matriz de estructuras OP_CERT_PFX_STORE.</span><span class="sxs-lookup"><span data-stu-id="5941c-110">Contains an array of OP_CERT_PFX_STORE structures.</span></span>

### <a name="csststores"></a><span data-ttu-id="5941c-111">cSstStores</span><span class="sxs-lookup"><span data-stu-id="5941c-111">cSstStores</span></span>

<span data-ttu-id="5941c-112">Contiene el número de elementos de pSstStores.</span><span class="sxs-lookup"><span data-stu-id="5941c-112">Contains the number of elements in pSstStores.</span></span>

### <a name="psststores"></a><span data-ttu-id="5941c-113">pSstStores</span><span class="sxs-lookup"><span data-stu-id="5941c-113">pSstStores</span></span>

<span data-ttu-id="5941c-114">Contiene una matriz de estructuras OP_CERT_SST_STORE.</span><span class="sxs-lookup"><span data-stu-id="5941c-114">Contains an array of OP_CERT_SST_STORE structures.</span></span>

### <a name="extension"></a><span data-ttu-id="5941c-115">Extensión</span><span class="sxs-lookup"><span data-stu-id="5941c-115">Extension</span></span>

<span data-ttu-id="5941c-116">Reservado para uso futuro y debe contener ceros.</span><span class="sxs-lookup"><span data-stu-id="5941c-116">Reserved for future use and must contain all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="5941c-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="5941c-117">See also</span></span>

[<span data-ttu-id="5941c-118">**Definiciones IDL de unión a dominio sin conexión**</span><span class="sxs-lookup"><span data-stu-id="5941c-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="5941c-119">**\_ \_ almacén pfx del certificado de OP \_**</span><span class="sxs-lookup"><span data-stu-id="5941c-119">**OP\_CERT\_PFX\_STORE**</span></span>](odj-op_cert_pfx_store.md)

[<span data-ttu-id="5941c-120">**\_ \_ almacén SST del certificado de OP \_**</span><span class="sxs-lookup"><span data-stu-id="5941c-120">**OP\_CERT\_SST\_STORE**</span></span>](odj-op_cert_sst_store.md)

[<span data-ttu-id="5941c-121">**BLOB de operaciones \_**</span><span class="sxs-lookup"><span data-stu-id="5941c-121">**OP\_BLOB**</span></span>](odj-op_blob.md)

