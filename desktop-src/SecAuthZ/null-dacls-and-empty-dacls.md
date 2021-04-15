---
description: Una DACL null concede acceso completo a cualquier usuario que lo solicite. Una DACL vacía es una DACL inicializada y asignada correctamente que no contiene entradas de control de acceso. Una DACL vacía no concede ningún acceso al objeto al que se asigna.
ms.assetid: 26e5c98d-bbdc-4f9f-96e0-18d1c429f1e6
title: DACL NULL y listas DACL vacías (autorización)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c06942d7b2d188a74b7e3e307cf60d6740a4251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668393"
---
# <a name="null-dacls-and-empty-dacls-authorization"></a><span data-ttu-id="637ab-105">DACL NULL y listas DACL vacías (autorización)</span><span class="sxs-lookup"><span data-stu-id="637ab-105">Null DACLs and Empty DACLs (Authorization)</span></span>

<span data-ttu-id="637ab-106">Si la [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) que pertenece al [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) de un objeto se establece en **null**, se crea una DACL null.</span><span class="sxs-lookup"><span data-stu-id="637ab-106">If the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) that belongs to an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly) is set to **NULL**, a null DACL is created.</span></span> <span data-ttu-id="637ab-107">Una DACL null concede acceso completo a cualquier usuario que lo solicite; la comprobación de seguridad normal no se realiza con respecto al objeto.</span><span class="sxs-lookup"><span data-stu-id="637ab-107">A null DACL grants full access to any user that requests it; normal security checking is not performed with respect to the object.</span></span> <span data-ttu-id="637ab-108">Una DACL null no se debería confundir con una DACL vacía.</span><span class="sxs-lookup"><span data-stu-id="637ab-108">A null DACL should not be confused with an empty DACL.</span></span> <span data-ttu-id="637ab-109">Una DACL vacía es una DACL inicializada y asignada correctamente que no contiene [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE).</span><span class="sxs-lookup"><span data-stu-id="637ab-109">An empty DACL is a properly allocated and initialized DACL that contains no [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs).</span></span> <span data-ttu-id="637ab-110">Una DACL vacía no concede ningún acceso al objeto al que se asigna.</span><span class="sxs-lookup"><span data-stu-id="637ab-110">An empty DACL grants no access to the object it is assigned to.</span></span>

<span data-ttu-id="637ab-111">Para obtener un ejemplo de cómo crear una DACL, vea [crear una DACL](/windows/desktop/SecBP/creating-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="637ab-111">For an example of how to create a DACL, see [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).</span></span>

 

 
