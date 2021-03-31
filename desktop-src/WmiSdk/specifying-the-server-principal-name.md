---
description: El servicio de autenticación Kerberos especifica el nombre de la entidad de seguridad del servidor para garantizar la identidad del equipo al que se está conectando.
ms.assetid: 3d58db28-2e69-4e27-9f27-61529abbf750
ms.tgt_platform: multiple
title: Especificar el nombre de la entidad de seguridad del servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a2f5aa4053b5ae7452e5f5e9c0ddcac15630ae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155849"
---
# <a name="specifying-the-server-principal-name"></a><span data-ttu-id="603af-103">Especificar el nombre de la entidad de seguridad del servidor</span><span class="sxs-lookup"><span data-stu-id="603af-103">Specifying the Server Principal Name</span></span>

<span data-ttu-id="603af-104">El servicio de autenticación Kerberos especifica el nombre de la entidad de seguridad del servidor para garantizar la identidad del equipo al que se está conectando.</span><span class="sxs-lookup"><span data-stu-id="603af-104">The Kerberos authentication service specifies the server principal name to ensure the identity of the computer to which it is connecting.</span></span> <span data-ttu-id="603af-105">Especifique el nombre de la entidad de seguridad del servidor en la llamada al método de scripting [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) proporcionando el nombre del equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="603af-105">Specify the server principal name in the call to the scripting method [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) by giving the name of the remote computer.</span></span> <span data-ttu-id="603af-106">En C++, especifique el nombre de la entidad de seguridad del servidor en el parámetro *pServerPrincName* al llamar a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) para el proxy.</span><span class="sxs-lookup"><span data-stu-id="603af-106">In C++, specify the server principal name in the *pServerPrincName* parameter when calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) for the proxy.</span></span> <span data-ttu-id="603af-107">Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés).</span><span class="sxs-lookup"><span data-stu-id="603af-107">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="603af-108">Este parámetro es necesario para que Kerberos admita la autenticación mutua.</span><span class="sxs-lookup"><span data-stu-id="603af-108">This parameter is required for Kerberos to support mutual authentication.</span></span> <span data-ttu-id="603af-109">Sin embargo, el uso del nombre de entidad de seguridad de servidor predeterminado no permite la autenticación mutua.</span><span class="sxs-lookup"><span data-stu-id="603af-109">However, using the default server principal name does not allow mutual authentication.</span></span> <span data-ttu-id="603af-110">Los clientes para los que la autenticación mutua es crítica, deben especificar un nombre de entidad de seguridad de servidor que coincida con la identidad del servidor que usa el servicio WMI.</span><span class="sxs-lookup"><span data-stu-id="603af-110">Clients for which mutual authentication is critical, must specify a server principal name that matches the server identity that the WMI service is using.</span></span> <span data-ttu-id="603af-111">Para obtener más información sobre la configuración de la seguridad de proxy y un ejemplo de C++ que muestra cómo establecer el nombre principal del servidor, vea [establecer la seguridad en IWbemServices y en otros servidores proxy](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="603af-111">For more information about setting proxy security and a C++ example showing how to set the server principal name, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

<span data-ttu-id="603af-112">Para obtener más información acerca de cómo establecer el nombre de la entidad de seguridad de servidor en script y Visual Basic, vea [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) y [conectarse a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="603af-112">For more information about setting the server principal name in script and Visual Basic, see [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) and [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="603af-113">A diferencia de la mayoría de los protocolos de seguridad de Instrumental de administración de Windows (WMI) y del modelo de objetos componentes (COM), no se puede establecer la entidad de seguridad de servidor en una llamada a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="603af-113">Unlike most security protocols for Windows Management Instrumentation (WMI) and Component Object Model (COM), you cannot set the server principal in a call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="603af-114">Sin embargo, puede establecer la entidad de seguridad de servidor con el parámetro *bstrAuthority* para [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)o el parámetro *pServerPrincName* para [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="603af-114">However, you can set the server principal with the *bstrAuthority* parameter for [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), or the *pServerPrincName* parameter for [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

<span data-ttu-id="603af-115">El ejemplo de código de este tema requiere la siguiente \# instrucción include para compilar correctamente.</span><span class="sxs-lookup"><span data-stu-id="603af-115">The code example in this topic requires the following \#include statement to correctly compile.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="603af-116">En el ejemplo de código siguiente se muestra cómo establecer el nombre de la entidad de seguridad del servidor con [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="603af-116">The following code example shows how to set the server principal name with [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>


```C++
IWbemServices* g_pNameSpace = NULL;

// Namespace to which to connect
BSTR  bstrNameSpace = 
SysAllocString( L"\\\\MyMachine\\root\default" );

// The bstrAuthority string contains the server
// principal name MyDomain\\MyMachine
// and the authentication service, which is Kerberos.
BSTR  bstrAuthority = 
SysAllocString( L"kerberos:MyDomain\\MyMachine"  );

HRESULT hr = NULL;
IWbemLocator* pWbemLocator = 0;

  hr = pWbemLocator->ConnectServer(
          bstrNameSpace,  // NameSpace name
          NULL,           // User name
          NULL,           // Password
          NULL,           // Locale
          0L,             // Security flags
          bstrAuthority,  // Authority, server principal name
          NULL,           // WBEM context
          &g_pNameSpace   // Namespace
          );

  // Free memory resources.
  g_pNameSpace->Release();
  SysFreeString(bstrNameSpace);
  SysFreeString(bstrAuthority);
```



## <a name="related-topics"></a><span data-ttu-id="603af-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="603af-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="603af-118">Establecer el servicio de autenticación mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="603af-118">Setting the Authentication Service Using VBScript</span></span>](setting-the-authentication-service-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="603af-119">Establecer la autenticación con C++</span><span class="sxs-lookup"><span data-stu-id="603af-119">Setting Authentication Using C++</span></span>](setting-authentication-using-c-.md)
</dt> <dt>

[<span data-ttu-id="603af-120">Establecer la seguridad en IWbemServices y en otros servidores proxy</span><span class="sxs-lookup"><span data-stu-id="603af-120">Setting the Security on IWbemServices and Other Proxies</span></span>](setting-the-security-on-iwbemservices-and-other-proxies.md)
</dt> </dl>

 

 
