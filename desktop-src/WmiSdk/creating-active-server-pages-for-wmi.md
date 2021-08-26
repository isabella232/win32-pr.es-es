---
description: Describe cómo crear Microsoft Active Server Pages (ASP) que muestran información sobre equipos remotos en equipos que no tienen WMI instalado.
ms.assetid: add08566-6408-43e4-9d0d-4c0851540602
ms.tgt_platform: multiple
title: Crear Active Server para WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee7b31a5f4874e0ae4431ac452ea604da9c154bbb78e8debb91aad7ea892fa09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030615"
---
# <a name="creating-active-server-pages-for-wmi"></a>Crear Active Server para WMI

Microsoft Active Server Pages (ASP) puede crear páginas web dinámicas mediante la inclusión de scripts del lado servidor y del lado cliente. Las páginas ASP pueden ser mucho más rápidas que las páginas HTML de cliente porque la mayor parte del trabajo se realiza en el servidor. También puede usar páginas ASP para mostrar información sobre equipos remotos a otros equipos que no tengan instalado Windows Management Instrumentation (WMI).

En el procedimiento siguiente se describe cómo usar WMI con ASP.

**Para usar WMI con ASP**

1.  Escriba una página ASP (.asp) que use WMI y colómela en un directorio accesible para el servidor web.

    Los scripts ASP para WMI se pueden desarrollar con varios lenguajes de scripting, incluido VBScript. Puede construir la parte del script WMI de una página ASP exactamente como construye cualquier otro script que use WMI, con una restricción importante: no puede usar métodos WMI asincrónicos dentro de páginas ASP. Tenga en cuenta también que las llamadas **a GetObject** **o CreateObject** deben estar en el código del lado servidor. Para obtener más información, vea [Scripting API para WMI.](scripting-api-for-wmi.md)

2.  Configure la configuración de autenticación para Internet Information Services (IIS). Para obtener más información, vea [Configuring IIS 5 and Later for WMI ASP Scripting](configuring-iis-5-for-wmi-asp-scripting.md).
3.  Deshabilite el acceso anónimo y habilite Windows autenticación integrada para el archivo ASP. Puede configurar estos valores para la página ASP mediante el complemento iis ubicado en la carpeta **Herramientas** administrativas de la **Panel de control**.

## <a name="wmi-asp-page-example"></a>Ejemplo de página ASP de WMI

En el ejemplo siguiente se usa Windows Management Instrumentation (WMI) dentro de una página de Active Server (ASP) para mostrar la dirección IP y la configuración predeterminada de la puerta de enlace IP para el servidor desde el que se ejecuta este script.


```VB
<%@ LANGUAGE="VBSCRIPT"%>
<HTML>
<HEAD>
<TITLE>WMI ASP Example:
    Read Default Gateway and IP Address information </TITLE>
</HEAD>

<BODY>

<%
On Error Resume Next
set IPConfigSet = GetObject("winmgmts:" _
   & "{impersonationLevel=impersonate}!root\cimv2").ExecQuery" _
    & "("SELECT IPAddress, DefaultIPGateway "" _ 
    & " FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled=TRUE")
%>

<%If Err <> 0 Then %>
    <%if err.number = -2147217405 then%>
        <p>Error 0x80041003: Access Denied: 
           Check permissions and file security for this ASP file.</p>
    <%else%>
        <p>Error description: <%=Err.description%> 
           error number <%=Err.number%></p>
    <%end if%>

<%end if %>

<%for each IPConfig in IPConfigSet%>

    <%if Not IsNull(IPConfig.IPAddress) then %>
        <%for i=LBound(IPConfig.IPAddress) 
            to UBound(IPConfig.IPAddress)%>
            <p>IP Address: <%=IPConfig.IPAddress(i)%></p>
        <%next%>
    <%end if%>
    

    <%if Not IsNull(IPConfig.DefaultIPGateway) then %>
        <%for i=LBound(IPConfig.DefaultIPGateway) 
            to UBound(IPConfig.DefaultIPGateway)%>
            <p>Default IP Gateway: 
                <%=IPConfig.DefaultIPGateway(i)%></p>
        <%next%>
    <%end if%>
<%next%>

<%If Err <> 0 Then %>
    <p>error description: <%=Err.description%> 
       error number <%=Err.number%></p>
<%end if %>

</BODY>
</HTML>
```



 

 



