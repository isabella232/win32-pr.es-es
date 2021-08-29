---
description: En Windows 7, WMI implementó la clase \_ OptionalFeature de Win32. Esta clase recupera el estado de las características opcionales que están presentes en un equipo.
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: Consultar el estado de las características opcionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8a8cceccdfeec6f902a56e8903a1d41e504750e
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786691"
---
# <a name="querying-the-status-of-optional-features"></a>Consultar el estado de las características opcionales

En Windows 7, WMI implementó la clase [**\_ OptionalFeature de Win32.**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) Esta clase recupera el estado de las características opcionales que están presentes en un equipo.

Puede usar Windows PowerShell cmdlets para consultar el estado de las características opcionales. Todos los ejemplos de este tema usan el cmdlet Get-WmiObject . Para obtener más información, [vea Get-WmiObject](/previous-versions//dd315295(v=technet.10)).

**Para recuperar todas las instancias de características opcionales presentes en un equipo**


    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject Win32_OptionalFeature</code></pre> | 


    

**Para consultar una característica opcional especificando el nombre de la característica**


    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject -query "select * from Win32_OptionalFeature where name = 'TelnetClient'"</code></pre> | 


    

    > [!Note]  
    > The **name** property is case-sensitive.

     

**Para consultar características opcionales especificando el estado de instalación**


    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject -query "select * from win32_optionalfeature where installstate= 1"</code></pre> | 


    

    For more information about the possible values for the **InstallState** property, see [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
