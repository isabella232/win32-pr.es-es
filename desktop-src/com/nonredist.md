---
title: NONREDIST
description: Agrega nombres a la lista de archivos que no se deben exportar cuando las aplicaciones COM+ se empaquetan para instalarse en otros equipos. Tenga en cuenta que se trata de una subclave, no de un valor.
ms.assetid: c50e20e4-1a25-4978-ab84-8f7b4b2f6069
keywords:
- Valor del registro nonredit COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d537208ecaf98cec46591966e4ae7d9c205850a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076413"
---
# <a name="nonredist"></a><span data-ttu-id="3029f-105">NONREDIST</span><span class="sxs-lookup"><span data-stu-id="3029f-105">NONREDIST</span></span>

<span data-ttu-id="3029f-106">Agrega nombres a la lista de archivos que no se deben exportar cuando las aplicaciones COM+ se empaquetan para instalarse en otros equipos.</span><span class="sxs-lookup"><span data-stu-id="3029f-106">Adds names to the list of files that should not be exported when COM+ applications are packaged for installation on other computers.</span></span> <span data-ttu-id="3029f-107">Tenga en cuenta que se trata de una subclave, no de un valor.</span><span class="sxs-lookup"><span data-stu-id="3029f-107">Note that this is a subkey, not a value.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="3029f-108">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="3029f-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   NONREDIST
      name1
      name2
```

## <a name="remarks"></a><span data-ttu-id="3029f-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3029f-109">Remarks</span></span>

<span data-ttu-id="3029f-110">Los archivos que se agregan a la lista se representan mediante pares de nombre/valor almacenados bajo esta clave.</span><span class="sxs-lookup"><span data-stu-id="3029f-110">The files you add to the list are represented by name/value pairs stored under this key.</span></span> <span data-ttu-id="3029f-111">En cada par de nombre y valor, el nombre es el nombre de archivo y el valor está reservado.</span><span class="sxs-lookup"><span data-stu-id="3029f-111">In each name/value pair, the name is the file name and the value is reserved.</span></span>

 

 




