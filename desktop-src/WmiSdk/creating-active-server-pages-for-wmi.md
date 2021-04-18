---
description: Describe cómo crear páginas de Microsoft Active Server (ASP) que muestran información acerca de los equipos remotos en equipos que no tienen WMI instalado.
ms.assetid: add08566-6408-43e4-9d0d-4c0851540602
ms.tgt_platform: multiple
title: Crear páginas Active Server para WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 52143284be54868d36b55a6dd86e0b49c82d863d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707408"
---
# <a name="creating-active-server-pages-for-wmi"></a>Crear páginas Active Server para WMI

Microsoft Active Server páginas (ASP) puede crear páginas web dinámicas mediante la inclusión de scripts en el lado servidor y en el lado cliente. Las páginas ASP pueden ser mucho más rápidas que las páginas HTML de cliente, ya que la mayor parte del trabajo se realiza en el servidor. También puede usar páginas ASP para mostrar información acerca de los equipos remotos en otros equipos que no tienen Instrumental de administración de Windows (WMI) instalado.

En el procedimiento siguiente se describe cómo utilizar WMI con ASP.

**Para utilizar WMI con ASP**

1.  Escriba una página ASP (. asp) que use WMI y colóquela en un directorio accesible para el servidor Web.

    Los scripts ASP para WMI se pueden desarrollar con varios lenguajes de scripting, incluido VBScript. Puede construir la parte del script de WMI de una página ASP exactamente como crea cualquier otro script que use WMI, con una restricción importante: no se pueden usar métodos de WMI asincrónicos en páginas ASP. Tenga en cuenta también que las llamadas a **GetObject** o **CreateObject** deben estar en el código del servidor. Para obtener más información, consulte [API de scripting para WMI](scripting-api-for-wmi.md).

2.  Configure la configuración de autenticación para Internet Information Services (IIS). Para obtener más información, vea [configurar IIS 5 y versiones posteriores para el scripting de ASP de WMI](configuring-iis-5-for-wmi-asp-scripting.md).
3.  Deshabilite el acceso anónimo y habilite la autenticación integrada de Windows para el archivo ASP. Puede configurar estas opciones para la página ASP mediante el complemento IIS que se encuentra en la carpeta **herramientas administrativas** del **Panel de control**.

## <a name="wmi-asp-page-example"></a>Ejemplo de página ASP de WMI

En el ejemplo siguiente se usa Instrumental de administración de Windows (WMI) dentro de una página de Active Server (ASP) para mostrar la dirección IP y la configuración de puerta de enlace IP predeterminada para el servidor desde el que se ejecuta este script.


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



 

 



