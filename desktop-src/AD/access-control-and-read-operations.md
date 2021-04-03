---
title: Operaciones de Access Control y de lectura
description: La seguridad es un filtro implícito para buscar, enumerar contenedores o leer propiedades.
ms.assetid: ee46cbc4-5539-48ce-991f-3ad0429f65ca
ms.tgt_platform: multiple
keywords:
- Access Control y leer operaciones de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aac8797828dd6322723a95f5e2048f986f1230d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075025"
---
# <a name="access-control-and-read-operations"></a><span data-ttu-id="65aff-104">Operaciones de Access Control y de lectura</span><span class="sxs-lookup"><span data-stu-id="65aff-104">Access Control and Read Operations</span></span>

<span data-ttu-id="65aff-105">La seguridad es un filtro implícito para buscar, enumerar contenedores o leer propiedades.</span><span class="sxs-lookup"><span data-stu-id="65aff-105">Security is an implicit filter for searching, enumerating containers, or reading properties.</span></span> <span data-ttu-id="65aff-106">Si no tiene los derechos de acceso necesarios, se pueden producir errores en los intentos de enumeración de objetos o en propiedades de lectura con los siguientes códigos de error incluso si existe el objeto o la propiedad:</span><span class="sxs-lookup"><span data-stu-id="65aff-106">If you do not have the necessary access rights, attempts to list objects or read properties can fail with the following error codes even thought the object or property exists:</span></span>

-   <span data-ttu-id="65aff-107">**E \_ ADS \_ \_ objeto de dominio no válido \_**</span><span class="sxs-lookup"><span data-stu-id="65aff-107">**E\_ADS\_INVALID\_DOMAIN\_OBJECT**</span></span>
-   <span data-ttu-id="65aff-108">**\_no se \_ admite la propiedad de ADS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="65aff-108">**E\_ADS\_PROPERTY\_NOT\_SUPPORTED**</span></span>
-   <span data-ttu-id="65aff-109">**\_ \_ \_ no \_ se encontró la propiedad de ADS**</span><span class="sxs-lookup"><span data-stu-id="65aff-109">**E\_ADS\_PROPERTY\_NOT\_FOUND**</span></span>

<span data-ttu-id="65aff-110">Tenga en cuenta que un llamador **con \_ el derecho ADS \_ ACTRL \_ DS \_** acceso a un contenedor puede enumerar los objetos secundarios en el contenedor.</span><span class="sxs-lookup"><span data-stu-id="65aff-110">Be aware that a caller with **ADS\_RIGHT\_ACTRL\_DS\_LIST** access to a container can enumerate the child objects in the container.</span></span> <span data-ttu-id="65aff-111">Sin embargo, un intento de acceder a un objeto secundario puede seguir produciendo un error **como \_ E \_ ADS \_ objeto desconocido** si el autor de la llamada no tiene el **derecho de ADS \_ \_ ACTRL \_ DS \_ List \_ Object** Access al objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="65aff-111">But an attempt to access a child object can still fail with an error such as **E\_ADS\_UNKNOWN\_OBJECT** if the caller does not have **ADS\_RIGHT\_ACTRL\_DS\_LIST\_OBJECT** access to the child object.</span></span>

<span data-ttu-id="65aff-112">El impacto de la seguridad en las operaciones de lectura no se manifiesta necesariamente como un error.</span><span class="sxs-lookup"><span data-stu-id="65aff-112">The impact of security on read operations is not necessarily manifested as an error.</span></span> <span data-ttu-id="65aff-113">Por ejemplo, una operación de búsqueda puede realizarse correctamente, pero los resultados de la búsqueda no incluyen objetos o propiedades a los que el llamador no tiene acceso.</span><span class="sxs-lookup"><span data-stu-id="65aff-113">For example, a search operation can succeed, but the search results do not include objects or properties to which the caller does not have access.</span></span>

 

 




