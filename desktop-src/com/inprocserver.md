---
title: InprocServer
description: Especifica la ruta de acceso al archivo DLL de servidor en proceso.
ms.assetid: f14cc8f7-e93e-4db8-8b0d-ea77a6301f33
keywords:
- Clave del registro de InprocServer COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5682693d711f734bbc60def8a711f11e2bad0ef9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994215"
---
# <a name="inprocserver"></a><span data-ttu-id="30e94-104">InprocServer</span><span class="sxs-lookup"><span data-stu-id="30e94-104">InprocServer</span></span>

<span data-ttu-id="30e94-105">Especifica la ruta de acceso al archivo DLL de servidor en proceso.</span><span class="sxs-lookup"><span data-stu-id="30e94-105">Specifies the path to the in-process server DLL.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="30e94-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="30e94-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer
         (Default) = path
```

## <a name="remarks"></a><span data-ttu-id="30e94-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30e94-107">Remarks</span></span>

<span data-ttu-id="30e94-108">La entrada **InprocServer** es relativamente inusual para las clases que se van a insertar.</span><span class="sxs-lookup"><span data-stu-id="30e94-108">The **InprocServer** entry is relatively rare for insertable classes.</span></span>

<span data-ttu-id="30e94-109">Los servidores en proceso están registrados actualmente mediante la entrada del registro **InprocServer** .</span><span class="sxs-lookup"><span data-stu-id="30e94-109">In-process servers are currently registered using the **InprocServer** registry entry.</span></span> <span data-ttu-id="30e94-110">Los servidores en proceso de 32 y 64 bits deben usar la entrada [**InProcServer32**](inprocserver32.md) .</span><span class="sxs-lookup"><span data-stu-id="30e94-110">The 32-bit and 64-bit in-process servers should use the [**InprocServer32**](inprocserver32.md) entry.</span></span> <span data-ttu-id="30e94-111">Si un contenedor está buscando en el registro un servidor en proceso, la versión de 16 bits tiene prioridad con un contenedor de 16 bits y la versión de 32 bits tiene prioridad con un contenedor de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="30e94-111">If a container is searching the registry for an in-process server, the 16-bit version has priority with a 16-bit container and 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30e94-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="30e94-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30e94-113">**InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="30e94-113">**InprocServer32**</span></span>](inprocserver32.md)
</dt> </dl>

 

 




