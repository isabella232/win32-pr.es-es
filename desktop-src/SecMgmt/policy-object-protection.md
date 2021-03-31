---
description: Describe cómo se protege el objeto de directiva de forma predeterminada.
ms.assetid: e2d65ebf-5fbd-4e25-9862-a8188abb5492
title: Protección de objetos de Directiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802fea6ce37a070c8230c3c9993df78a45f439bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809319"
---
# <a name="policy-object-protection"></a><span data-ttu-id="dd572-103">Protección de objetos de Directiva</span><span class="sxs-lookup"><span data-stu-id="dd572-103">Policy Object Protection</span></span>

<span data-ttu-id="dd572-104">El objeto de [**Directiva**](policy-object.md) está protegido de forma predeterminada con la siguiente configuración:</span><span class="sxs-lookup"><span data-stu-id="dd572-104">The [**Policy**](policy-object.md) object is protected by default with the following settings:</span></span>

-   <span data-ttu-id="dd572-105">El mundo del grupo local tiene \_ acceso de ejecución genérico.</span><span class="sxs-lookup"><span data-stu-id="dd572-105">The local group WORLD has GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="dd572-106">Se concede a la Directiva todo el acceso al sistema de IDENTIFICADOres conocidos \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="dd572-106">The well-known ID System is granted POLICY\_ALL\_ACCESS.</span></span>
-   <span data-ttu-id="dd572-107">El administrador LOCAL del grupo local \_ tiene \_ acceso genérico de lectura, \_ escritura genérica y \_ ejecución genérica.</span><span class="sxs-lookup"><span data-stu-id="dd572-107">The local group LOCAL\_ADMIN has GENERIC\_READ, GENERIC\_WRITE, and GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="dd572-108">El administrador LOCAL \_ del grupo se asigna como propietario y grupo principal de este objeto.</span><span class="sxs-lookup"><span data-stu-id="dd572-108">The group LOCAL\_ADMIN is assigned as owner and primary group of this object.</span></span>

<span data-ttu-id="dd572-109">No se puede crear ni destruir el objeto de [**Directiva**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="dd572-109">The [**Policy**](policy-object.md) object cannot be created or destroyed.</span></span>

 

 



