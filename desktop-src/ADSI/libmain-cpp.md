---
title: LIBMAIN. CPP
description: En el componente de proveedor de ejemplo, un ejemplo de código del punto de entrada de DLL estándar para Adssmp.dll está en LibMain. cpp. En la tabla siguiente se enumeran las rutinas admitidas.
ms.assetid: aa05fbd1-509d-4ed6-8a49-1ce11ce54c0e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e309d3c6454901b26f5ab67351033b39d73dd7aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656166"
---
# <a name="libmaincpp"></a><span data-ttu-id="cf6c8-104">LIBMAIN. CPP</span><span class="sxs-lookup"><span data-stu-id="cf6c8-104">LIBMAIN.CPP</span></span>

<span data-ttu-id="cf6c8-105">En el componente de proveedor de ejemplo, un ejemplo de código del punto de entrada de DLL estándar para Adssmp.dll está en LibMain. cpp.</span><span class="sxs-lookup"><span data-stu-id="cf6c8-105">In the example provider component, a code example of the standard DLL entry point for Adssmp.dll is in Libmain.cpp.</span></span> <span data-ttu-id="cf6c8-106">En la tabla siguiente se enumeran las rutinas admitidas.</span><span class="sxs-lookup"><span data-stu-id="cf6c8-106">Supported routines are listed in the following table.</span></span>



| <span data-ttu-id="cf6c8-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="cf6c8-107">Item</span></span>                                  | <span data-ttu-id="cf6c8-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf6c8-108">Description</span></span>                                                              |
|---------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="cf6c8-109">**DllGetClassObject**</span><span class="sxs-lookup"><span data-stu-id="cf6c8-109">**DllGetClassObject**</span></span><br/>      | <span data-ttu-id="cf6c8-110">Punto de entrada de DLL estándar para buscar generadores de clases.</span><span class="sxs-lookup"><span data-stu-id="cf6c8-110">Standard DLL entry point for locating class factories.</span></span><br/>        |
| <span data-ttu-id="cf6c8-111">**DllCanUnloadNow**</span><span class="sxs-lookup"><span data-stu-id="cf6c8-111">**DllCanUnloadNow**</span></span><br/>        | <span data-ttu-id="cf6c8-112">Punto de entrada de DLL estándar para determinar si se puede descargar el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="cf6c8-112">Standard DLL entry point to determine if DLL can be unloaded.</span></span><br/> |
| <span data-ttu-id="cf6c8-113">**LibMain**</span><span class="sxs-lookup"><span data-stu-id="cf6c8-113">**LibMain**</span></span><br/>                | <span data-ttu-id="cf6c8-114">Punto de entrada de inicialización de DLL estándar.</span><span class="sxs-lookup"><span data-stu-id="cf6c8-114">Standard DLL initialization entry point.</span></span><br/>                      |
| <span data-ttu-id="cf6c8-115">**IsCompatibleOleVersion**</span><span class="sxs-lookup"><span data-stu-id="cf6c8-115">**IsCompatibleOleVersion**</span></span><br/> | <span data-ttu-id="cf6c8-116">Comprobar la compatibilidad con el tiempo de ejecución de OLE.</span><span class="sxs-lookup"><span data-stu-id="cf6c8-116">Verify compatibility with the OLE run time.</span></span><br/>                   |
| <span data-ttu-id="cf6c8-117">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="cf6c8-117">**DllMain**</span></span><br/>                | <span data-ttu-id="cf6c8-118">Punto de entrada para la mayoría de las versiones de Windows 2000 o Windows NT.</span><span class="sxs-lookup"><span data-stu-id="cf6c8-118">Entry point for most Windows 2000 or Windows NT versions.</span></span><br/>     |



 

 

 





