---
title: Efectos de la seguridad en la búsqueda
description: La seguridad es un filtro implícito al realizar búsquedas, enumerar contenedores o leer propiedades.
ms.assetid: 4a027069-8c3d-4a95-a04b-c9c59200a9ed
ms.tgt_platform: multiple
keywords:
- efectos de la seguridad en la búsqueda Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26feee840c0668b2ea9412932a27927bb1c00012
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773236"
---
# <a name="effects-of-security-on-searching"></a><span data-ttu-id="c8e64-104">Efectos de la seguridad en la búsqueda</span><span class="sxs-lookup"><span data-stu-id="c8e64-104">Effects of Security on Searching</span></span>

<span data-ttu-id="c8e64-105">La seguridad es un filtro implícito al realizar búsquedas, enumerar contenedores o leer propiedades.</span><span class="sxs-lookup"><span data-stu-id="c8e64-105">Security is an implicit filter when performing searches, enumerating containers, or reading properties.</span></span>

<span data-ttu-id="c8e64-106">ADSI no puede devolver ninguna \_ propiedad de este tipo, \_ ni \_ \_ siquiera cuando el objeto existe si no tiene acceso para leer atributos en el objeto.</span><span class="sxs-lookup"><span data-stu-id="c8e64-106">ADSI can return NO\_SUCH\_PROPERTY or NO\_SUCH\_OBJECT errors even when the object exists if you do not have access to read attributes on the object.</span></span>

<span data-ttu-id="c8e64-107">Por ejemplo, un llamador puede enumerar los objetos secundarios de un contenedor porque el autor de la llamada tiene \_ derechos de lista de contenido en el contenedor.</span><span class="sxs-lookup"><span data-stu-id="c8e64-107">For example, a caller may be able to enumerate the child objects in a container because the caller has LIST\_CONTENTS rights on the container.</span></span> <span data-ttu-id="c8e64-108">Pero es posible que el mismo llamador no pueda tener acceso a los objetos enumerados si el autor de la llamada no tiene acceso de lectura a los objetos secundarios.</span><span class="sxs-lookup"><span data-stu-id="c8e64-108">But the same caller may not be able to access the enumerated objects if the caller does not have read access to the child objects.</span></span> <span data-ttu-id="c8e64-109">En este caso, es posible que una consulta para un objeto secundario NO devuelva \_ este tipo de \_ objeto aunque el autor de la llamada haya enumerado correctamente el objeto.</span><span class="sxs-lookup"><span data-stu-id="c8e64-109">In this case, a query for a child object may return NO\_SUCH\_OBJECT even though the caller successfully enumerated the object.</span></span>

<span data-ttu-id="c8e64-110">Si el autor de la llamada no tiene derechos suficientes, se pueden devolver los siguientes códigos de retorno:</span><span class="sxs-lookup"><span data-stu-id="c8e64-110">If the caller does not have sufficient rights, the following return codes may be returned:</span></span>

<span data-ttu-id="c8e64-111">E \_ ADS \_ \_ objeto de dominio no válido \_</span><span class="sxs-lookup"><span data-stu-id="c8e64-111">E\_ADS\_INVALID\_DOMAIN\_OBJECT</span></span>

<span data-ttu-id="c8e64-112">\_no se \_ admite la propiedad de ADS \_ \_</span><span class="sxs-lookup"><span data-stu-id="c8e64-112">E\_ADS\_PROPERTY\_NOT\_SUPPORTED</span></span>

<span data-ttu-id="c8e64-113">\_ \_ \_ no \_ se encontró la propiedad de ADS</span><span class="sxs-lookup"><span data-stu-id="c8e64-113">E\_ADS\_PROPERTY\_NOT\_FOUND</span></span>

 

 




