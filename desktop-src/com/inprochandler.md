---
title: InprocHandler
description: Especifica si una aplicación utiliza un controlador personalizado.
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- Clave del registro InprocHandler COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8c19089ece43496465351b44e9faa8793ba893
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418958"
---
# <a name="inprochandler"></a><span data-ttu-id="b7082-104">InprocHandler</span><span class="sxs-lookup"><span data-stu-id="b7082-104">InprocHandler</span></span>

<span data-ttu-id="b7082-105">Especifica si una aplicación utiliza un controlador personalizado.</span><span class="sxs-lookup"><span data-stu-id="b7082-105">Specifies whether an application uses a custom handler.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="b7082-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="b7082-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler = handler.dll
```

## <a name="remarks"></a><span data-ttu-id="b7082-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7082-107">Remarks</span></span>

<span data-ttu-id="b7082-108">Se trata de un valor de **reg \_ SZ** que especifica el controlador personalizado que utiliza la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7082-108">This is a **REG\_SZ** value that specifies the custom handler used by the application.</span></span> <span data-ttu-id="b7082-109">Si no se utiliza un controlador personalizado, la entrada debe establecerse en Ole32.dll.</span><span class="sxs-lookup"><span data-stu-id="b7082-109">If a custom handler is not used, the entry should be set to Ole32.dll.</span></span>

<span data-ttu-id="b7082-110">Si un contenedor está buscando en el registro un controlador personalizado, la versión de 16 bits tiene prioridad con un contenedor de 16 bits y la versión de 32 bits tiene prioridad con un contenedor de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b7082-110">If a container is searching the registry for a custom handler, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7082-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b7082-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7082-112">**InprocHandler32**</span><span class="sxs-lookup"><span data-stu-id="b7082-112">**InprocHandler32**</span></span>](inprochandler32.md)
</dt> </dl>

 

 




