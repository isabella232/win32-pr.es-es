---
title: Protocolo
description: Indica que esta clase OLE 2 se va a insertar en contenedores OLE 1.
ms.assetid: 320dff51-ac27-42f3-8c0f-353b29e289d9
keywords:
- Clave del registro de protocolo COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176cb3fce826a6416270fc35a902621521341e6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714205"
---
# <a name="protocol"></a><span data-ttu-id="a0f44-104">Protocolo</span><span class="sxs-lookup"><span data-stu-id="a0f44-104">Protocol</span></span>

<span data-ttu-id="a0f44-105">Indica que esta clase OLE 2 se va a insertar en contenedores OLE 1.</span><span class="sxs-lookup"><span data-stu-id="a0f44-105">Indicates that this OLE 2 class is insertable in OLE 1 containers.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="a0f44-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="a0f44-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Protocol
         StdFileEditing
            Server = path
            Verb
               0 = verb1
               1 = verb2
               ...
```

## <a name="remarks"></a><span data-ttu-id="a0f44-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0f44-107">Remarks</span></span>

<span data-ttu-id="a0f44-108">La entrada **StdFileEditing** especifica la información de compatibilidad de OLE 1.</span><span class="sxs-lookup"><span data-stu-id="a0f44-108">The **StdFileEditing** entry specifies OLE 1 compatibility information.</span></span> <span data-ttu-id="a0f44-109">Debe estar presente solo si los objetos de esta clase se pueden insertar en contenedores OLE 1.</span><span class="sxs-lookup"><span data-stu-id="a0f44-109">It should be present only if objects of this class are insertable in OLE 1 containers.</span></span>

<span data-ttu-id="a0f44-110">**Server** especifica la ruta de acceso completa a la aplicación de servidor OLE 2 y **Verb** especifica los verbos.</span><span class="sxs-lookup"><span data-stu-id="a0f44-110">**Server** specifies the full path to the OLE 2 server application and **Verb** specifies the verbs.</span></span> <span data-ttu-id="a0f44-111">El verbo 0 es el verbo principal y los verbos adicionales se deben numerar consecutivamente.</span><span class="sxs-lookup"><span data-stu-id="a0f44-111">Verb 0 is the primary verb and additional verbs must be numbered consecutively.</span></span>

 

 




