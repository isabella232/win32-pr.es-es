---
title: Generar el UUID
description: El primer paso para definir la interfaz es usar la utilidad uuidgen para generar un identificador único universal (UUID).
ms.assetid: 870641b7-affc-4de4-bc7f-4c8ca2873fb6
keywords:
- RPC llamada a procedimiento remoto, tareas, generar el UUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e263bfe21c4a564106c0d6328c0de891c18bca1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903435"
---
# <a name="generating-the-uuid"></a><span data-ttu-id="77fa9-104">Generar el UUID</span><span class="sxs-lookup"><span data-stu-id="77fa9-104">Generating the UUID</span></span>

<span data-ttu-id="77fa9-105">El primer paso para definir la interfaz es usar la utilidad **uuidgen** para generar un identificador único universal (UUID).</span><span class="sxs-lookup"><span data-stu-id="77fa9-105">The first step in defining the interface is to use the **uuidgen** utility to generate a universally unique identifier (UUID).</span></span> <span data-ttu-id="77fa9-106">Un UUID permite que las aplicaciones cliente y servidor se identifiquen entre sí.</span><span class="sxs-lookup"><span data-stu-id="77fa9-106">A UUID enables the client and server applications identify each other.</span></span> <span data-ttu-id="77fa9-107">La utilidad **uuidgen** (Uuidgen.exe) se instala automáticamente al instalar el kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="77fa9-107">The **uuidgen** utility (Uuidgen.exe) is automatically installed when you install the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="77fa9-108">El siguiente comando genera un UUID y crea un archivo de plantilla denominado Hello. idl.</span><span class="sxs-lookup"><span data-stu-id="77fa9-108">The following command generates a UUID and creates a template file called Hello.idl.</span></span>

<span data-ttu-id="77fa9-109">**uuidgen/i/ohello.idl**</span><span class="sxs-lookup"><span data-stu-id="77fa9-109">**uuidgen /i /ohello.idl**</span></span>

<span data-ttu-id="77fa9-110">La plantilla Hello. idl tendrá el siguiente aspecto (con un UUID diferente, por supuesto).</span><span class="sxs-lookup"><span data-stu-id="77fa9-110">Your hello.idl template will look like this (with a different UUID, of course).</span></span>

``` syntax
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface INTERFACENAME
{
 
}
```

 

 




