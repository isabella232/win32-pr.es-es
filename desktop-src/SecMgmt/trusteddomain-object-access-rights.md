---
description: Enumera y explica los derechos de acceso del objeto TrustedDomain.
ms.assetid: eb82864c-7e69-4ed5-a55d-d6792670bcd1
title: Derechos de acceso a objetos de TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f79dc44b54ff907cbe3d1f700cc673f75a40d57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686668"
---
# <a name="trusteddomain-object-access-rights"></a><span data-ttu-id="53e2c-103">Derechos de acceso a objetos de TrustedDomain</span><span class="sxs-lookup"><span data-stu-id="53e2c-103">TrustedDomain Object Access Rights</span></span>

<span data-ttu-id="53e2c-104">El tipo de objeto [**TrustedDomain**](trusteddomain-object.md) tiene los siguientes tipos de acceso:</span><span class="sxs-lookup"><span data-stu-id="53e2c-104">The [**TrustedDomain**](trusteddomain-object.md) object type has the following access types:</span></span>



| <span data-ttu-id="53e2c-105">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="53e2c-105">Access type</span></span>                  | <span data-ttu-id="53e2c-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="53e2c-106">Description</span></span>                                                                      |
|------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="53e2c-107">\_nombre de \_ dominio de consulta de confianza \_</span><span class="sxs-lookup"><span data-stu-id="53e2c-107">TRUSTED\_QUERY\_DOMAIN\_NAME</span></span> | <span data-ttu-id="53e2c-108">Este tipo de acceso es necesario para consultar el nombre del dominio de confianza.</span><span class="sxs-lookup"><span data-stu-id="53e2c-108">This access type is needed to query the name of the trusted domain.</span></span>              |
| <span data-ttu-id="53e2c-109">\_controladores de conjuntos de confianza \_</span><span class="sxs-lookup"><span data-stu-id="53e2c-109">TRUSTED\_SET\_CONTROLLERS</span></span>    | <span data-ttu-id="53e2c-110">Este tipo de acceso es necesario para establecer la lista de controladores del dominio de confianza.</span><span class="sxs-lookup"><span data-stu-id="53e2c-110">This access type is needed to set the list of controllers of the trusted domain.</span></span> |
| <span data-ttu-id="53e2c-111">\_POSIX de consulta de confianza \_</span><span class="sxs-lookup"><span data-stu-id="53e2c-111">TRUSTED\_QUERY\_POSIX</span></span>        | <span data-ttu-id="53e2c-112">Este tipo de acceso es necesario para recuperar el desplazamiento de identificador POSIX de un dominio de confianza.</span><span class="sxs-lookup"><span data-stu-id="53e2c-112">This access type is needed to retrieve the Posix ID offset of a trusted domain.</span></span>  |
| <span data-ttu-id="53e2c-113">\_POSIX de conjunto de confianza \_</span><span class="sxs-lookup"><span data-stu-id="53e2c-113">TRUSTED\_SET\_POSIX</span></span>          | <span data-ttu-id="53e2c-114">Este tipo de acceso es necesario para establecer el desplazamiento de identificador POSIX de un dominio de confianza.</span><span class="sxs-lookup"><span data-stu-id="53e2c-114">This access type is needed to set the Posix ID offset of a trusted domain.</span></span>       |



 

## <a name="generic-access-masks"></a><span data-ttu-id="53e2c-115">Máscaras de acceso genéricas</span><span class="sxs-lookup"><span data-stu-id="53e2c-115">Generic Access Masks</span></span>

<span data-ttu-id="53e2c-116">Este tipo de objeto tiene las siguientes asignaciones de acceso genérico:</span><span class="sxs-lookup"><span data-stu-id="53e2c-116">This object type has the following generic access mappings:</span></span>

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                    TRUSTED_QUERY_DOMAIN_NAME

    GENERIC_WRITE        STANDARD_RIGHTS_WRITE |
                    TRUSTED_SET_POSIX

    GENERIC_EXECUTE    STANDARD_RIGHTS_EXECUTE |
                    TRUSTED_QUERY_POSIX
```

## <a name="standard-access-types"></a><span data-ttu-id="53e2c-117">Tipos de acceso estándar</span><span class="sxs-lookup"><span data-stu-id="53e2c-117">Standard Access Types</span></span>

<span data-ttu-id="53e2c-118">Este objeto no admite el tipo de acceso estándar SINCRONIZAr (opcional).</span><span class="sxs-lookup"><span data-stu-id="53e2c-118">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="53e2c-119">Se admiten todos los tipos de acceso necesarios.</span><span class="sxs-lookup"><span data-stu-id="53e2c-119">All required access types are supported.</span></span> <span data-ttu-id="53e2c-120">La máscara de todos los tipos de acceso admitidos para este tipo de objeto es:</span><span class="sxs-lookup"><span data-stu-id="53e2c-120">The mask of all supported access types for this object type is:</span></span>

``` syntax
    TRUSTED_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    TRUSTED_QUERY_DOMAIN_NAME |
                    TRUSTED_QUERY_CONTROLLERS |
                    TRUSTED_SET_CONTROLLERS
```

 

 



