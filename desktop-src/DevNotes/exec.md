---
description: HKLM \\ software \\ Microsoft \\ Internet Explorer \\ extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}.
ms.assetid: a0d9e959-d8fd-4546-9529-1dc42fa0bdd6
title: Exec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2711b2c8882f9af12de2f060810ccd4219faa5ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807718"
---
# <a name="exec"></a><span data-ttu-id="ae5ff-103">Exec</span><span class="sxs-lookup"><span data-stu-id="ae5ff-103">Exec</span></span>

<span data-ttu-id="ae5ff-104">**HKLM \\ software \\ Microsoft \\ Internet Explorer \\ extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}**</span><span class="sxs-lookup"><span data-stu-id="ae5ff-104">**HKLM\\Software\\Microsoft\\Internet Explorer\\Extensions\\{e2e2dd38-d088-4134-82b7-f2ba38496583}**</span></span>



| <span data-ttu-id="ae5ff-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ae5ff-105">Data type</span></span> | <span data-ttu-id="ae5ff-106">Intervalo</span><span class="sxs-lookup"><span data-stu-id="ae5ff-106">Range</span></span>                    | <span data-ttu-id="ae5ff-107">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="ae5ff-107">Default value</span></span> |
|-----------|--------------------------|---------------|
| <span data-ttu-id="ae5ff-108">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="ae5ff-108">REG\_SZ</span></span>   | <span data-ttu-id="ae5ff-109">*Ruta de acceso al archivo ejecutable*</span><span class="sxs-lookup"><span data-stu-id="ae5ff-109">*Path to the executable*</span></span> |               |



 

## <a name="browser-integration-steps"></a><span data-ttu-id="ae5ff-110">Pasos de integración del explorador</span><span class="sxs-lookup"><span data-stu-id="ae5ff-110">Browser Integration Steps</span></span>

1.  <span data-ttu-id="ae5ff-111">Use la función [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) para determinar si el diagnóstico de red está instalado.</span><span class="sxs-lookup"><span data-stu-id="ae5ff-111">Use the [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) function to determine whether the Network Diagnostic is installed.</span></span> <span data-ttu-id="ae5ff-112">Si está instalado, la clave **{e2e2dd38-d088-4134-82b7-f2ba38496583}** está presente.</span><span class="sxs-lookup"><span data-stu-id="ae5ff-112">If it is installed, the **{e2e2dd38-d088-4134-82b7-f2ba38496583}** key is present.</span></span>
2.  <span data-ttu-id="ae5ff-113">Use la función [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) para recuperar la ruta de acceso del archivo ejecutable de diagnóstico de red de la entrada **exec** .</span><span class="sxs-lookup"><span data-stu-id="ae5ff-113">Use the [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) function to retrieve the path of the Network Diagnostic executable file from the **Exec** entry.</span></span>
3.  <span data-ttu-id="ae5ff-114">Muestra la nueva página de error si el diagnóstico está instalado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="ae5ff-114">Display the new error page if the diagnostic is installed on the system.</span></span>
4.  <span data-ttu-id="ae5ff-115">Cree una extensión de explorador que cree un elemento de la barra de herramientas estándar si el diagnóstico está instalado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="ae5ff-115">Create a browser extension that creates a standard toolbar item if the diagnostic is installed on the system.</span></span>
5.  <span data-ttu-id="ae5ff-116">Ejecute el archivo ejecutable de diagnóstico de red mediante la ruta de acceso recuperada en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="ae5ff-116">Execute the Network Diagnostic executable using the path retrieved in step 2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae5ff-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ae5ff-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae5ff-118">Información general sobre las características de diagnóstico de red</span><span class="sxs-lookup"><span data-stu-id="ae5ff-118">Network Diagnostics Tools Feature Overview</span></span>](https://www.microsoft.com/technet/prodtechnol/winxppro/maintain/netdiag.mspx)
</dt> </dl>

 

 
