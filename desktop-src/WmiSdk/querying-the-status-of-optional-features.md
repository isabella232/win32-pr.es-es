---
description: En Windows 7, WMI implementó la \_ clase Win32 OptionalFeature. Esta clase recupera el estado de las características opcionales que están presentes en un equipo.
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: Consultar el estado de las características opcionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c190b2a2143dae1e22c30b3e5e803908bcb4116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812650"
---
# <a name="querying-the-status-of-optional-features"></a><span data-ttu-id="664dd-104">Consultar el estado de las características opcionales</span><span class="sxs-lookup"><span data-stu-id="664dd-104">Querying the Status of Optional Features</span></span>

<span data-ttu-id="664dd-105">En Windows 7, WMI implementó la clase [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) .</span><span class="sxs-lookup"><span data-stu-id="664dd-105">In Windows 7, WMI implemented the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class.</span></span> <span data-ttu-id="664dd-106">Esta clase recupera el estado de las características opcionales que están presentes en un equipo.</span><span class="sxs-lookup"><span data-stu-id="664dd-106">This class retrieves the status of the optional features that are present on a computer.</span></span>

<span data-ttu-id="664dd-107">Puede usar cmdlets de Windows PowerShell para consultar el estado de las características opcionales.</span><span class="sxs-lookup"><span data-stu-id="664dd-107">You can use Windows PowerShell cmdlets to query the status of optional features.</span></span> <span data-ttu-id="664dd-108">En todos los ejemplos de este tema se usa el cmdlet Get-WmiObject.</span><span class="sxs-lookup"><span data-stu-id="664dd-108">All of the examples in this topic use the Get-WmiObject cmdlet.</span></span> <span data-ttu-id="664dd-109">Para obtener más información, vea [Get-WMIObject](/previous-versions//dd315295(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="664dd-109">For more information, see [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).</span></span>

<span data-ttu-id="664dd-110">**Para recuperar todas las instancias de características opcionales presentes en un equipo**</span><span class="sxs-lookup"><span data-stu-id="664dd-110">**To retrieve all instances of optional features present on a computer**</span></span>

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="664dd-111">PowerShell</span><span class="sxs-lookup"><span data-stu-id="664dd-111">PowerShell</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject Win32_OptionalFeature</code></pre></td>
    </tr>
    </tbody>
    </table>

    

<span data-ttu-id="664dd-112">**Para consultar una característica opcional especificando el nombre de la característica**</span><span class="sxs-lookup"><span data-stu-id="664dd-112">**To query for an optional feature by specifying the feature name**</span></span>

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="664dd-113">PowerShell</span><span class="sxs-lookup"><span data-stu-id="664dd-113">PowerShell</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from Win32_OptionalFeature where name = &#39;TelnetClient&#39;&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    > [!Note]  
    > <span data-ttu-id="664dd-114">La propiedad **Name** distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="664dd-114">The **name** property is case-sensitive.</span></span>

     

<span data-ttu-id="664dd-115">**Para consultar características opcionales especificando el estado de instalación**</span><span class="sxs-lookup"><span data-stu-id="664dd-115">**To query for optional features by specifying the install state**</span></span>

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="664dd-116">PowerShell</span><span class="sxs-lookup"><span data-stu-id="664dd-116">PowerShell</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from win32_optionalfeature where installstate= 1&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    <span data-ttu-id="664dd-117">Para obtener más información sobre los posibles valores de la propiedad **InstallState** , vea [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).</span><span class="sxs-lookup"><span data-stu-id="664dd-117">For more information about the possible values for the **InstallState** property, see [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).</span></span>

## <a name="related-topics"></a><span data-ttu-id="664dd-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="664dd-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="664dd-119">**Win32 \_ OptionalFeature**</span><span class="sxs-lookup"><span data-stu-id="664dd-119">**Win32\_OptionalFeature**</span></span>](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
