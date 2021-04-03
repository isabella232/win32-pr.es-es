---
description: La referencia de scripting de WMI contiene definiciones para la API de scripting de WMI.
ms.assetid: 83fc78fc-929d-4d32-940e-9147543a6324
ms.tgt_platform: multiple
title: API de scripting para WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c43587fd8f40c2524bcabd79fe80e3d00d74b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908565"
---
# <a name="scripting-api-for-wmi"></a><span data-ttu-id="42ead-103">API de scripting para WMI</span><span class="sxs-lookup"><span data-stu-id="42ead-103">Scripting API for WMI</span></span>

<span data-ttu-id="42ead-104">La referencia de scripting de WMI contiene definiciones para la API de scripting de WMI.</span><span class="sxs-lookup"><span data-stu-id="42ead-104">The WMI scripting reference contains definitions for the WMI Scripting API.</span></span> <span data-ttu-id="42ead-105">Use esta API si escribe aplicaciones con Microsoft Visual Basic, Visual Basic para Aplicaciones, Visual Basic Scripting Edition (VBScript) o cualquier otro lenguaje de scripting que admita tecnologías de Active Scripting.</span><span class="sxs-lookup"><span data-stu-id="42ead-105">Use this API if writing applications with Microsoft Visual Basic, Visual Basic for Applications, Visual Basic Scripting Edition (VBScript), or any other scripting language that supports active scripting technologies.</span></span>

> [!Note]  
> <span data-ttu-id="42ead-106">PowerShell también está disponible para scripting con WMI.</span><span class="sxs-lookup"><span data-stu-id="42ead-106">PowerShell is also available for scripting with WMI.</span></span> <span data-ttu-id="42ead-107">El cmdlet Get-WMI y los tres aceleradores de tipos ( \[ WMI \] , \[ WMIClass \] y \[ wmisearcher \] ) permiten el acceso administrativo básico a WMI.</span><span class="sxs-lookup"><span data-stu-id="42ead-107">The Get-WMI cmdlet and the three type accelerators (\[wmi\], \[wmiclass\], and \[wmisearcher\]) enable basic administrative access to WMI.</span></span> <span data-ttu-id="42ead-108">Para obtener más información, vea [scripting con Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).</span><span class="sxs-lookup"><span data-stu-id="42ead-108">For more information, see [Scripting with Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).</span></span>

 

<span data-ttu-id="42ead-109">Los objetos de scripting de WMI, a excepción de [**SWbemDateTime**](swbemdatetime.md) , no están marcados como seguros para scripts para scripts que se ejecutan en páginas HTML en Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="42ead-109">WMI scripting objects, except for [**SWbemDateTime**](swbemdatetime.md) are not marked safe for scripting for scripts running on HTML pages in Internet Explorer.</span></span> <span data-ttu-id="42ead-110">Por lo tanto, a menos que se reduzca el nivel de seguridad de Internet Explorer, se producirá un error en el script.</span><span class="sxs-lookup"><span data-stu-id="42ead-110">Therefore, unless the security level within Internet Explorer is lowered, the script will fail.</span></span> <span data-ttu-id="42ead-111">**SWbemDateTime** está marcado como Safe para la inicialización y el scripting.</span><span class="sxs-lookup"><span data-stu-id="42ead-111">**SWbemDateTime** is marked safe for initialization and scripting.</span></span> <span data-ttu-id="42ead-112">Sin embargo, use todos los objetos de scripting de WMI en las llamadas **GetObject** y **CreateObject** en el código del lado servidor en páginas de Active Server (ASP).</span><span class="sxs-lookup"><span data-stu-id="42ead-112">However, use all WMI scripting objects in **GetObject** and **CreateObject** calls on server-side code in Active Server Pages (ASP).</span></span>

-   [<span data-ttu-id="42ead-113">Modelo de objetos de API de scripting</span><span class="sxs-lookup"><span data-stu-id="42ead-113">Scripting API Object Model</span></span>](scripting-api-object-model.md)
-   [<span data-ttu-id="42ead-114">Convenciones de documentos para la API de scripting</span><span class="sxs-lookup"><span data-stu-id="42ead-114">Document Conventions for the Scripting API</span></span>](document-conventions-for-the-scripting-api.md)
-   [<span data-ttu-id="42ead-115">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="42ead-115">Scripting API Objects</span></span>](scripting-api-objects.md)
-   [<span data-ttu-id="42ead-116">Scripting de constantes de API</span><span class="sxs-lookup"><span data-stu-id="42ead-116">Scripting API Constants</span></span>](scripting-api-constants.md)

## <a name="related-topics"></a><span data-ttu-id="42ead-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="42ead-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42ead-118">Referencia de WMI</span><span class="sxs-lookup"><span data-stu-id="42ead-118">WMI Reference</span></span>](wmi-reference.md)
</dt> <dt>

[<span data-ttu-id="42ead-119">Códigos de retorno de WMI</span><span class="sxs-lookup"><span data-stu-id="42ead-119">WMI Return Codes</span></span>](wmi-return-codes.md)
</dt> </dl>

 

 



