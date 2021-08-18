---
description: En Windows 7, WMI implementó la clase \_ OptionalFeature de Win32. Esta clase recupera el estado de las características opcionales que están presentes en un equipo.
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: Consultar el estado de las características opcionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec27457336adcc5c358aad0a5e139c1c7c07f6bcb72335ec549f9ca98cc1e5a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996035"
---
# <a name="querying-the-status-of-optional-features"></a>Consultar el estado de las características opcionales

En Windows 7, WMI implementó la [**clase \_ OptionalFeature de Win32.**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) Esta clase recupera el estado de las características opcionales que están presentes en un equipo.

Puede usar Windows PowerShell cmdlets para consultar el estado de las características opcionales. Todos los ejemplos de este tema usan el cmdlet Get-WmiObject. Para obtener más información, [vea Get-WmiObject](/previous-versions//dd315295(v=technet.10)).

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
    > La **propiedad name** distingue mayúsculas de minúsculas.

     

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

    

    Para obtener más información sobre los valores posibles para **la propiedad InstallState,** vea [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
