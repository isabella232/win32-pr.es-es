---
title: InprocHandler32
description: Especifica si una aplicación utiliza un controlador personalizado.
ms.assetid: da611bb6-1f69-449a-9821-e2fbbe413a97
keywords:
- Clave del registro InprocHandler32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c918669aa3de1c8cf2622e3caf4acc9ae18f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418476"
---
# <a name="inprochandler32"></a><span data-ttu-id="4851f-104">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="4851f-104">InprocHandler32</span></span>

<span data-ttu-id="4851f-105">Especifica si una aplicación utiliza un controlador personalizado.</span><span class="sxs-lookup"><span data-stu-id="4851f-105">Specifies whether an application uses a custom handler.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="4851f-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="4851f-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler32 = handler.dll
```

## <a name="remarks"></a><span data-ttu-id="4851f-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4851f-107">Remarks</span></span>

<span data-ttu-id="4851f-108">Se trata de un valor de **reg \_ SZ** que especifica el controlador personalizado que utiliza la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4851f-108">This is a **REG\_SZ** value that specifies the custom handler used by the application.</span></span> <span data-ttu-id="4851f-109">Si no se utiliza un controlador personalizado, la entrada debe establecerse en Ole32.dll.</span><span class="sxs-lookup"><span data-stu-id="4851f-109">If a custom handler is not used, the entry should be set to Ole32.dll.</span></span>

<span data-ttu-id="4851f-110">Si un contenedor está buscando en el registro un controlador personalizado, la versión de 16 bits tiene prioridad con un contenedor de 16 bits y la versión de 32 bits tiene prioridad con un contenedor de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4851f-110">If a container is searching the registry for a custom handler, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4851f-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4851f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4851f-112">**InprocHandler**</span><span class="sxs-lookup"><span data-stu-id="4851f-112">**InprocHandler**</span></span>](inprochandler.md)
</dt> </dl>

 

 




