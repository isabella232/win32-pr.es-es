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
# <a name="querying-the-status-of-optional-features"></a>Consultar el estado de las características opcionales

En Windows 7, WMI implementó la clase [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) . Esta clase recupera el estado de las características opcionales que están presentes en un equipo.

Puede usar cmdlets de Windows PowerShell para consultar el estado de las características opcionales. En todos los ejemplos de este tema se usa el cmdlet Get-WmiObject. Para obtener más información, vea [Get-WMIObject](/previous-versions//dd315295(v=technet.10)).

**Para recuperar todas las instancias de características opcionales presentes en un equipo**

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>PowerShell</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject Win32_OptionalFeature</code></pre></td>
    </tr>
    </tbody>
    </table>

    

**Para consultar una característica opcional especificando el nombre de la característica**

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>PowerShell</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from Win32_OptionalFeature where name = &#39;TelnetClient&#39;&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    > [!Note]  
    > La propiedad **Name** distingue mayúsculas de minúsculas.

     

**Para consultar características opcionales especificando el estado de instalación**

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>PowerShell</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from win32_optionalfeature where installstate= 1&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    Para obtener más información sobre los posibles valores de la propiedad **InstallState** , vea [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
