---
description: Enumera y explica los derechos de acceso del objeto de datos privado.
ms.assetid: 82be57d0-487c-4eb7-83d5-0dd2d53a452b
title: Derechos de acceso a objetos de datos privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142aecfe133a9c04237aacf58413e026c4cb3164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497188"
---
# <a name="private-data-object-access-rights"></a><span data-ttu-id="24837-103">Derechos de acceso a objetos de datos privados</span><span class="sxs-lookup"><span data-stu-id="24837-103">Private Data Object Access Rights</span></span>

<span data-ttu-id="24837-104">Los tipos de acceso de este tipo de objeto son:</span><span class="sxs-lookup"><span data-stu-id="24837-104">The access types of this object type are:</span></span>



| <span data-ttu-id="24837-105">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="24837-105">Access type</span></span>          | <span data-ttu-id="24837-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="24837-106">Description</span></span>                                      |
|----------------------|--------------------------------------------------|
| <span data-ttu-id="24837-107">\_valor de consulta Secret \_</span><span class="sxs-lookup"><span data-stu-id="24837-107">SECRET\_QUERY\_VALUE</span></span> | <span data-ttu-id="24837-108">Este tipo de acceso es necesario para recuperar un secreto.</span><span class="sxs-lookup"><span data-stu-id="24837-108">This access type is needed to retrieve a secret.</span></span> |
| <span data-ttu-id="24837-109">\_valor del conjunto de secretos \_</span><span class="sxs-lookup"><span data-stu-id="24837-109">SECRET\_SET\_VALUE</span></span>   | <span data-ttu-id="24837-110">Este tipo de acceso es necesario para modificar un secreto.</span><span class="sxs-lookup"><span data-stu-id="24837-110">This access type is needed to modify a secret.</span></span>   |



 

## <a name="generic-access-masks"></a><span data-ttu-id="24837-111">Máscaras de acceso genéricas</span><span class="sxs-lookup"><span data-stu-id="24837-111">Generic Access Masks</span></span>

<span data-ttu-id="24837-112">Este tipo de objeto tiene las siguientes asignaciones de acceso genérico:</span><span class="sxs-lookup"><span data-stu-id="24837-112">This object type has the following generic access mappings:</span></span>

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    SECRET_QUERY_VALUE

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    SECRET_SET_VALUE

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a><span data-ttu-id="24837-113">Tipos de acceso estándar:</span><span class="sxs-lookup"><span data-stu-id="24837-113">Standard Access Types:</span></span>

<span data-ttu-id="24837-114">Este objeto no admite el tipo de acceso estándar SINCRONIZAr (opcional).</span><span class="sxs-lookup"><span data-stu-id="24837-114">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="24837-115">Se admiten todos los tipos de acceso necesarios.</span><span class="sxs-lookup"><span data-stu-id="24837-115">All required access types are supported.</span></span> <span data-ttu-id="24837-116">La máscara de todos los tipos de acceso admitidos para este tipo de objeto es:</span><span class="sxs-lookup"><span data-stu-id="24837-116">The mask of all supported access types for this object type is:</span></span>

``` syntax
    SECRET_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    SECRET_QUERY_VALUE |
                    SECRET_SET_VALUE
```

 

 



