---
description: Explica cómo se protegen los objetos de cuenta.
ms.assetid: a07ef46e-f4b6-4e21-bdd7-72d03e1c88b3
title: Protección de objetos de cuenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f495a3dc943ef73eef5074e0edc73247ceb02d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668017"
---
# <a name="account-object-protection"></a><span data-ttu-id="1d29c-103">Protección de objetos de cuenta</span><span class="sxs-lookup"><span data-stu-id="1d29c-103">Account Object Protection</span></span>

<span data-ttu-id="1d29c-104">Los objetos de [**cuenta**](account-object.md) están protegidos de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="1d29c-104">[**Account**](account-object.md) objects are protected in the following fashion:</span></span>

-   <span data-ttu-id="1d29c-105">El grupo **mundial** tiene \_ ejecución genérica.</span><span class="sxs-lookup"><span data-stu-id="1d29c-105">The group **WORLD** has GENERIC\_EXECUTE.</span></span>
-   <span data-ttu-id="1d29c-106">El **\_ administrador local** del grupo tiene acceso de eliminación, genérico \_ lectura, escritura genérica \_ , \_ ejecución genérica y escritura \_ DACL.</span><span class="sxs-lookup"><span data-stu-id="1d29c-106">The group **LOCAL\_ADMIN** has DELETE, GENERIC\_READ, GENERIC\_WRITE, GENERIC\_EXECUTE, and WRITE\_DACL access.</span></span>
-   <span data-ttu-id="1d29c-107">El **\_ administrador local** de grupo se asigna como propietario y grupo principal de objetos de cuenta.</span><span class="sxs-lookup"><span data-stu-id="1d29c-107">The group **LOCAL\_ADMIN** is assigned as owner and primary group of Account objects.</span></span>

 

 



