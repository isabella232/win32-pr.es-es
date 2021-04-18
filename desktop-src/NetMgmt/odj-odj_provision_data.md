---
title: ODJ_PROVISION_DATA
description: Definición de ODJ_PROVISION_DATA IDL
ms.assetid: ff623d04-ad3f-4846-b9de-aaa280713018
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f07d8c200103fa21afc080c60157645fe6730766
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "105720196"
---
# <a name="odj_provision_data-structure"></a><span data-ttu-id="d7730-103">Estructura de ODJ_PROVISION_DATA</span><span class="sxs-lookup"><span data-stu-id="d7730-103">ODJ_PROVISION_DATA structure</span></span>

<span data-ttu-id="d7730-104">Especifica la estructura de serialización más externa utilizada por las API de unión a dominio sin conexión.</span><span class="sxs-lookup"><span data-stu-id="d7730-104">Specifies the outermost serialization structure used by the offline domain join apis.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7730-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7730-105">Syntax</span></span>

```C++
typedef struct _ODJ_PROVISION_DATA
{
    ULONG ulVersion;
    ULONG ulcBlobs;
    [size_is(ulcBlobs)] PODJ_BLOB pBlobs;
} ODJ_PROVISION_DATA;
```

## <a name="members"></a><span data-ttu-id="d7730-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d7730-106">Members</span></span>

### <a name="ulversion"></a><span data-ttu-id="d7730-107">ulVersion</span><span class="sxs-lookup"><span data-stu-id="d7730-107">ulVersion</span></span>

<span data-ttu-id="d7730-108">Debe establecerse en 1.</span><span class="sxs-lookup"><span data-stu-id="d7730-108">This must be set to 1.</span></span>

### <a name="ulcblobs"></a><span data-ttu-id="d7730-109">ulcBlobs</span><span class="sxs-lookup"><span data-stu-id="d7730-109">ulcBlobs</span></span>

<span data-ttu-id="d7730-110">Debe establecerse en el número de elementos de la matriz pBlobs.</span><span class="sxs-lookup"><span data-stu-id="d7730-110">This must be set to the number of elements in the pBlobs array.</span></span>

### <a name="pblobs"></a><span data-ttu-id="d7730-111">pBlobs</span><span class="sxs-lookup"><span data-stu-id="d7730-111">pBlobs</span></span>

<span data-ttu-id="d7730-112">Apunta a una matriz de estructuras de ODJ_BLOB.</span><span class="sxs-lookup"><span data-stu-id="d7730-112">Points to an array of ODJ_BLOB structures.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7730-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7730-113">See also</span></span>

[<span data-ttu-id="d7730-114">**Definiciones IDL de unión a dominio sin conexión**</span><span class="sxs-lookup"><span data-stu-id="d7730-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="d7730-115">**\_BLOB ODJ**</span><span class="sxs-lookup"><span data-stu-id="d7730-115">**ODJ\_BLOB**</span></span>](odj-odj_blob.md)


