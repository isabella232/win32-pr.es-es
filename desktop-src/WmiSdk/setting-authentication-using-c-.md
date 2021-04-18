---
description: 'Una de las tareas principales de IWbemLocator:: ConnectServer para WMI es devolver un puntero a un proxy IWbemServices.'
ms.assetid: bbff43b7-79f8-4c7b-a772-d3d962cf3859
ms.tgt_platform: multiple
title: Establecer la autenticación con C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 293d317ac521d36bf7ff616a0340f86c364ce885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706651"
---
# <a name="setting-authentication-using-c"></a><span data-ttu-id="3c7e6-103">Establecer la autenticación con C++</span><span class="sxs-lookup"><span data-stu-id="3c7e6-103">Setting Authentication Using C++</span></span>

<span data-ttu-id="3c7e6-104">Una de las tareas principales de [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) para WMI es devolver un puntero a un proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="3c7e6-104">One of the main tasks of [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) for WMI is returning a pointer to an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy.</span></span> <span data-ttu-id="3c7e6-105">A través del proxy **IWbemServices** , puede tener acceso a las capacidades de la infraestructura WMI.</span><span class="sxs-lookup"><span data-stu-id="3c7e6-105">Through the **IWbemServices** proxy, you can access the capabilities of the WMI infrastructure.</span></span> <span data-ttu-id="3c7e6-106">Sin embargo, el puntero al proxy **IWbemServices** tiene la identidad del proceso de la aplicación cliente y no la identidad del proceso **IWbemServices** .</span><span class="sxs-lookup"><span data-stu-id="3c7e6-106">However, the pointer to the **IWbemServices** proxy has the identity of the client application process and not the identity of the **IWbemServices** process.</span></span> <span data-ttu-id="3c7e6-107">Por lo tanto, si intenta obtener acceso a **IWbemServices** con el puntero, puede recibir un código de acceso denegado como **E \_ ACCESSDENIED**.</span><span class="sxs-lookup"><span data-stu-id="3c7e6-107">Therefore, if you attempt to access **IWbemServices** with the pointer, you can receive an access-denied code such as **E\_ACCESSDENIED**.</span></span> <span data-ttu-id="3c7e6-108">Para evitar el error de acceso denegado, debe establecer la identidad del nuevo puntero con una llamada a la interfaz [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="3c7e6-108">To avoid the access-denied error, you must set the identity of the new pointer with a call to the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) interface.</span></span>

<span data-ttu-id="3c7e6-109">Un proveedor puede establecer la seguridad en un espacio de nombres para que no se devuelvan datos a menos que se use la privacidad de paquetes (**PktPrivacy**) en la conexión a ese espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="3c7e6-109">A provider can set the security on a namespace so that no data is returned unless you use packet privacy (**PktPrivacy**) in your connection to that namespace.</span></span> <span data-ttu-id="3c7e6-110">Esto garantiza que los datos se cifren a medida que atraviesan la red.</span><span class="sxs-lookup"><span data-stu-id="3c7e6-110">This ensures that data is encrypted as it crosses the network.</span></span> <span data-ttu-id="3c7e6-111">Si intenta establecer un nivel de autenticación inferior, recibirá un mensaje de acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="3c7e6-111">If you try to set a lower authentication level, you will get an access denied message.</span></span> <span data-ttu-id="3c7e6-112">Para obtener más información, consulte [configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="3c7e6-112">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

<span data-ttu-id="3c7e6-113">Para obtener más información sobre cómo establecer la autenticación en scripting, vea [establecer el nivel de seguridad de proceso predeterminado mediante VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="3c7e6-113">For more information about setting authentication in scripting, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

## <a name="setting-security-on-a-remote-iunknown-interface"></a><span data-ttu-id="3c7e6-114">Establecer la seguridad en una interfaz IUnknown remota</span><span class="sxs-lookup"><span data-stu-id="3c7e6-114">Setting Security on a Remote IUnknown Interface</span></span>

<span data-ttu-id="3c7e6-115">En algunas situaciones, se requiere más acceso a un servidor que simplemente un puntero a un proxy.</span><span class="sxs-lookup"><span data-stu-id="3c7e6-115">In some situations, more access to a server than just a pointer to a proxy is required.</span></span> <span data-ttu-id="3c7e6-116">En ocasiones, puede que necesite obtener una conexión segura a la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del proxy.</span><span class="sxs-lookup"><span data-stu-id="3c7e6-116">At times, you may need to gain a secure connection to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the proxy.</span></span> <span data-ttu-id="3c7e6-117">Con **IUnknown**, puede consultar el sistema remoto en busca de interfaces y otras técnicas necesarias.</span><span class="sxs-lookup"><span data-stu-id="3c7e6-117">Using **IUnknown**, you can query the remote system for interfaces and other necessary techniques.</span></span>

<span data-ttu-id="3c7e6-118">Cuando un proxy se encuentra en un equipo remoto, el servidor delega todas las llamadas a la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del proxy a la interfaz **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="3c7e6-118">When a proxy is located on a remote computer, the server delegates all calls to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the proxy to the **IUnknown** interface.</span></span> <span data-ttu-id="3c7e6-119">Por ejemplo, si llama a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en un proxy y la interfaz solicitada no forma parte del proxy, el proxy envía la llamada al servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="3c7e6-119">For example, if you call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on a proxy and the requested interface was not part of the proxy, the proxy sends the call to the remote server.</span></span> <span data-ttu-id="3c7e6-120">A su vez, el servidor remoto comprueba la compatibilidad con la interfaz adecuada.</span><span class="sxs-lookup"><span data-stu-id="3c7e6-120">In turn, the remote server checks for the appropriate interface support.</span></span> <span data-ttu-id="3c7e6-121">Si el servidor admite la interfaz, COM vuelve a serializar un nuevo proxy en el cliente para que la aplicación pueda usar la nueva interfaz.</span><span class="sxs-lookup"><span data-stu-id="3c7e6-121">If the server does support the interface, COM marshals a new proxy back to the client so that the application can use the new interface.</span></span>

<span data-ttu-id="3c7e6-122">Surgen problemas si el cliente no tiene permisos de acceso al servidor remoto, pero usa las credenciales de un usuario que lo hace.</span><span class="sxs-lookup"><span data-stu-id="3c7e6-122">Problems arise if the client does not have access permissions to the remote server, yet is using the credentials of a user that does.</span></span> <span data-ttu-id="3c7e6-123">En esta situación, se produce un error en cualquier intento de obtener acceso a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="3c7e6-123">In this situation, any attempt to access [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the remote server fails.</span></span> <span data-ttu-id="3c7e6-124">También se produce un error en la versión final del proxy, ya que el usuario actual no tiene acceso al servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="3c7e6-124">The final release on the proxy fails as well, because the current user does not have access to the remote server.</span></span> <span data-ttu-id="3c7e6-125">Un síntoma de esto es un retraso de uno o dos segundos antes de que la aplicación cliente produzca un error en la versión final del proxy.</span><span class="sxs-lookup"><span data-stu-id="3c7e6-125">A symptom of this is a one or two second lag before the client application fails the final proxy release.</span></span> <span data-ttu-id="3c7e6-126">El error se produce porque COM intentó tener acceso al servidor remoto con la configuración de seguridad predeterminada del usuario actual, que no incluye las credenciales modificadas que permitían el acceso al servidor en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="3c7e6-126">The failure occurs because COM attempted to access the remote server using the default security settings of the current user, which do not include the modified credentials that allowed access to the server in the first place.</span></span> <span data-ttu-id="3c7e6-127">Para obtener más información, vea [establecer la seguridad en IWbemServices y en otros servidores proxy](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="3c7e6-127">For more information, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

<span data-ttu-id="3c7e6-128">Para evitar la conexión errónea, use [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) para establecer explícitamente la autenticación de seguridad en el puntero devuelto desde [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="3c7e6-128">To avoid the failed connection, use [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) to explicitly set the security authentication on the pointer returned from [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="3c7e6-129">Con **CoSetProxyBlanket**, puede asegurarse de que el servidor remoto recibe la identidad de autenticación correcta.</span><span class="sxs-lookup"><span data-stu-id="3c7e6-129">Using **CoSetProxyBlanket**, you can ensure that the remote server receives the correct authentication identity.</span></span>

<span data-ttu-id="3c7e6-130">En el ejemplo de código siguiente se muestra cómo usar [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) para tener acceso a una interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) remota.</span><span class="sxs-lookup"><span data-stu-id="3c7e6-130">The following code example shows how to use [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) to access a remote [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>


```C++
SEC_WINNT_AUTH_IDENTITY_W* pAuthIdentity = 
   new SEC_WINNT_AUTH_IDENTITY_W;
ZeroMemory(pAuthIdentity, sizeof(SEC_WINNT_AUTH_IDENTITY_W));

pAuthIdentity->User = new WCHAR[32];
StringCbCopyW(pAuthIdentity->User,sizeof(L"MyUser"),L"MyUser");
pAuthIdentity->UserLength = wcslen(pAuthIdentity->User);

pAuthIdentity->Domain = new WCHAR[32];
StringCbCopyW(pAuthIdentity->Domain,sizeof(L"MyDomain"),L"MyDomain");
pAuthIdentity->DomainLength = wcslen(pAuthIdentity->Domain);

pAuthIdentity->Password = new WCHAR[32];
pAuthIdentity->Password[0] = NULL;
pAuthIdentity->PasswordLength = wcslen( pAuthIdentity->Password);

pAuthIdentity->Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

IWbemServices* pWbemServices = 0;

// Set proxy security
hr = CoSetProxyBlanket(pWbemServices, 
                       RPC_C_AUTHN_DEFAULT, 
                       RPC_C_AUTHZ_NONE, 
                       COLE_DEFAULT_PRINCIPAL, 
                       RPC_C_AUTHN_LEVEL_DEFAULT, 
                       RPC_C_IMP_LEVEL_IMPERSONATE, 
                       pAuthIdentity, 
                       EOAC_NONE 
);
if (FAILED(hr))
{
   cout << "Count not set proxy blanket. Error code = 0x"
        << hex << hr << endl;
   pWbemServices->Release();
   return 1;
}

// Set IUnknown security
IUnknown*    pUnk = NULL;
pWbemServices->QueryInterface(IID_IUnknown, (void**) &pUnk);

hr = CoSetProxyBlanket(pUnk, 
                       RPC_C_AUTHN_DEFAULT, 
                       RPC_C_AUTHZ_NONE, 
                       COLE_DEFAULT_PRINCIPAL, 
                       RPC_C_AUTHN_LEVEL_DEFAULT, 
                       RPC_C_IMP_LEVEL_IMPERSONATE, 
                       pAuthIdentity, 
                       EOAC_NONE 
);
if (FAILED(hr))
{
   cout << "Count not set proxy blanket. Error code = 0x"
        << hex << hr << endl;
   pUnk->Release();
   pWbemServices->Release();
   delete [] pAuthIdentity->User;
   delete [] pAuthIdentity->Domain;
   delete [] pAuthIdentity->Password;
   delete pAuthIdentity;   
   return 1;
}

// cleanup IUnknown
pUnk->Release();

//
// Perform a bunch of operations
//

// Cleanup
pWbemServices->Release();

delete [] pAuthIdentity->User;
delete [] pAuthIdentity->Domain;
delete [] pAuthIdentity->Password;

delete pAuthIdentity;
```



> [!Note]  
> <span data-ttu-id="3c7e6-131">Cuando se establece la seguridad en la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) de un proxy, com crea una copia del proxy que no se puede liberar hasta que se llame a [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="3c7e6-131">When you set security on the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of a proxy, COM creates a copy of the proxy that cannot be released until you call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3c7e6-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3c7e6-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c7e6-133">Configuración de la autenticación en WMI</span><span class="sxs-lookup"><span data-stu-id="3c7e6-133">Setting Authentication in WMI</span></span>](setting-authentication-in-wmi.md)
</dt> </dl>

 

 
