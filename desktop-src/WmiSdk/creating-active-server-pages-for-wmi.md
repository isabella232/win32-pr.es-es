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
# <a name="creating-active-server-pages-for-wmi"></a><span data-ttu-id="6b32e-103">Crear páginas Active Server para WMI</span><span class="sxs-lookup"><span data-stu-id="6b32e-103">Creating Active Server Pages for WMI</span></span>

<span data-ttu-id="6b32e-104">Microsoft Active Server páginas (ASP) puede crear páginas web dinámicas mediante la inclusión de scripts en el lado servidor y en el lado cliente.</span><span class="sxs-lookup"><span data-stu-id="6b32e-104">Microsoft Active Server Pages (ASP) can create dynamic webpages by including both server-side and client-side scripts.</span></span> <span data-ttu-id="6b32e-105">Las páginas ASP pueden ser mucho más rápidas que las páginas HTML de cliente, ya que la mayor parte del trabajo se realiza en el servidor.</span><span class="sxs-lookup"><span data-stu-id="6b32e-105">ASP pages can be much faster than client HTML pages because most of the work is done on the server.</span></span> <span data-ttu-id="6b32e-106">También puede usar páginas ASP para mostrar información acerca de los equipos remotos en otros equipos que no tienen Instrumental de administración de Windows (WMI) instalado.</span><span class="sxs-lookup"><span data-stu-id="6b32e-106">You can also use ASP pages to display information about remote computers to other computers that do not have Windows Management Instrumentation (WMI) installed.</span></span>

<span data-ttu-id="6b32e-107">En el procedimiento siguiente se describe cómo utilizar WMI con ASP.</span><span class="sxs-lookup"><span data-stu-id="6b32e-107">The following procedure describes how to use WMI with ASP.</span></span>

<span data-ttu-id="6b32e-108">**Para utilizar WMI con ASP**</span><span class="sxs-lookup"><span data-stu-id="6b32e-108">**To use WMI with ASP**</span></span>

1.  <span data-ttu-id="6b32e-109">Escriba una página ASP (. asp) que use WMI y colóquela en un directorio accesible para el servidor Web.</span><span class="sxs-lookup"><span data-stu-id="6b32e-109">Write an ASP page (.asp) that uses WMI, and place it in a directory accessible to your web server.</span></span>

    <span data-ttu-id="6b32e-110">Los scripts ASP para WMI se pueden desarrollar con varios lenguajes de scripting, incluido VBScript.</span><span class="sxs-lookup"><span data-stu-id="6b32e-110">ASP scripts for WMI can be developed with several scripting languages, including VBScript.</span></span> <span data-ttu-id="6b32e-111">Puede construir la parte del script de WMI de una página ASP exactamente como crea cualquier otro script que use WMI, con una restricción importante: no se pueden usar métodos de WMI asincrónicos en páginas ASP.</span><span class="sxs-lookup"><span data-stu-id="6b32e-111">You can construct the WMI script part of an ASP page exactly as you construct any other script that uses WMI, with one important restriction: you cannot use asynchronous WMI methods within ASP pages.</span></span> <span data-ttu-id="6b32e-112">Tenga en cuenta también que las llamadas a **GetObject** o **CreateObject** deben estar en el código del servidor.</span><span class="sxs-lookup"><span data-stu-id="6b32e-112">Note also that any calls to **GetObject** or **CreateObject** must be in the server-side code.</span></span> <span data-ttu-id="6b32e-113">Para obtener más información, consulte [API de scripting para WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="6b32e-113">For more information, see [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

2.  <span data-ttu-id="6b32e-114">Configure la configuración de autenticación para Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="6b32e-114">Set up authentication configuration for Internet Information Services (IIS).</span></span> <span data-ttu-id="6b32e-115">Para obtener más información, vea [configurar IIS 5 y versiones posteriores para el scripting de ASP de WMI](configuring-iis-5-for-wmi-asp-scripting.md).</span><span class="sxs-lookup"><span data-stu-id="6b32e-115">For more information, see [Configuring IIS 5 and Later for WMI ASP Scripting](configuring-iis-5-for-wmi-asp-scripting.md).</span></span>
3.  <span data-ttu-id="6b32e-116">Deshabilite el acceso anónimo y habilite la autenticación integrada de Windows para el archivo ASP.</span><span class="sxs-lookup"><span data-stu-id="6b32e-116">Disable anonymous access, and enable Windows Integrated Authentication for the ASP file.</span></span> <span data-ttu-id="6b32e-117">Puede configurar estas opciones para la página ASP mediante el complemento IIS que se encuentra en la carpeta **herramientas administrativas** del **Panel de control**.</span><span class="sxs-lookup"><span data-stu-id="6b32e-117">You can configure these settings for your ASP page by using the IIS snap-in located in the **Administrative Tools** folder of the **Control Panel**.</span></span>

## <a name="wmi-asp-page-example"></a><span data-ttu-id="6b32e-118">Ejemplo de página ASP de WMI</span><span class="sxs-lookup"><span data-stu-id="6b32e-118">WMI ASP Page Example</span></span>

<span data-ttu-id="6b32e-119">En el ejemplo siguiente se usa Instrumental de administración de Windows (WMI) dentro de una página de Active Server (ASP) para mostrar la dirección IP y la configuración de puerta de enlace IP predeterminada para el servidor desde el que se ejecuta este script.</span><span class="sxs-lookup"><span data-stu-id="6b32e-119">The following example uses Windows Management Instrumentation (WMI) within an Active Server Page (ASP) to display the IP address and default IP gateway settings for the server from which this script is executed.</span></span>


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



 

 



