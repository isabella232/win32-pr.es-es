---
title: InprocHandler32
description: InprocHandler32 especifica si una aplicación usa un controlador personalizado en el HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID clave del Registro.
ms.assetid: da611bb6-1f69-449a-9821-e2fbbe413a97
keywords:
- Com de clave del Registro InprocHandler32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be73a8b2577a554b0bb8b5ba5a851e630edbf90a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406008"
---
# <a name="inprochandler32"></a><span data-ttu-id="fe981-104">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="fe981-104">InprocHandler32</span></span>

<span data-ttu-id="fe981-105">Especifica si una aplicación usa un controlador personalizado.</span><span class="sxs-lookup"><span data-stu-id="fe981-105">Specifies whether an application uses a custom handler.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="fe981-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="fe981-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler32 = handler.dll
```

## <a name="remarks"></a><span data-ttu-id="fe981-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe981-107">Remarks</span></span>

<span data-ttu-id="fe981-108">Se trata de **un valor \_ REG SZ** que especifica el controlador personalizado utilizado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fe981-108">This is a **REG\_SZ** value that specifies the custom handler used by the application.</span></span> <span data-ttu-id="fe981-109">Si no se usa un controlador personalizado, la entrada debe establecerse en Ole32.dll.</span><span class="sxs-lookup"><span data-stu-id="fe981-109">If a custom handler is not used, the entry should be set to Ole32.dll.</span></span>

<span data-ttu-id="fe981-110">Si un contenedor busca en el Registro un controlador personalizado, la versión de 16 bits tiene prioridad con un contenedor de 16 bits y la versión de 32 bits tiene prioridad con un contenedor de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fe981-110">If a container is searching the registry for a custom handler, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe981-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fe981-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe981-112">**InprocHandler**</span><span class="sxs-lookup"><span data-stu-id="fe981-112">**InprocHandler**</span></span>](inprochandler.md)
</dt> </dl>

 

 




