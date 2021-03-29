---
title: La función named_type_free_inst
description: El código auxiliar llama a \_ la \_ función inst Free de tipo con nombre \_ para liberar memoria asociada al tipo transmitido.
ms.assetid: 4b9e10cb-25bb-4f00-86a0-5436e5ac71d9
keywords:
- named_type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2d3b5103572eb58e4311c65b0e1cff02e91f66f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774628"
---
# <a name="the-named_type_free_inst-function"></a><span data-ttu-id="2e93c-104">\_ \_ Función inst Free de tipo con nombre \_</span><span class="sxs-lookup"><span data-stu-id="2e93c-104">The named\_type\_free\_inst Function</span></span>

<span data-ttu-id="2e93c-105">El código auxiliar llama a la función **\_ \_ \_ inst Free de tipo con nombre** para liberar memoria asociada al tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="2e93c-105">The stubs call the **named\_type\_free\_inst** function to free memory associated with the transmitted type.</span></span> <span data-ttu-id="2e93c-106">La función se define como:</span><span class="sxs-lookup"><span data-stu-id="2e93c-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <named_type>_free_inst(<type> __RPC_FAR *)
```

<span data-ttu-id="2e93c-107">El parámetro apunta a la instancia del tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="2e93c-107">The parameter points to the instance of the transmitted type.</span></span> <span data-ttu-id="2e93c-108">Este objeto no se debe liberar.</span><span class="sxs-lookup"><span data-stu-id="2e93c-108">This object should not be freed.</span></span> <span data-ttu-id="2e93c-109">Para obtener una explicación sobre cuándo llamar a la función, vea [el \_ atributo representated as](the-represent-as-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="2e93c-109">For a discussion on when to call the function, see [The represent\_as Attribute](the-represent-as-attribute.md).</span></span>

 

 




