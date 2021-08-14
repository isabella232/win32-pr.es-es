---
description: Una de las tareas principales de IWbemLocator::ConnectServer para WMI es devolver un puntero a un proxy IWbemServices.
ms.assetid: bbff43b7-79f8-4c7b-a772-d3d962cf3859
ms.tgt_platform: multiple
title: Establecer la autenticación mediante C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7b0ef3bcd1e9908815c94dacc3815fec77eaea33f2da48119dbe3178563eae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315622"
---
# <a name="setting-authentication-using-c"></a>Establecer la autenticación mediante C++

Una de las tareas principales de [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) para WMI es devolver un puntero a un proxy [**IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) A través del proxy **IWbemServices,** puede acceder a las funcionalidades de la infraestructura WMI. Sin embargo, el puntero al proxy **IWbemServices** tiene la identidad del proceso de aplicación cliente y no la identidad del **proceso IWbemServices.** Por lo tanto, si intenta acceder a **IWbemServices** con el puntero , puede recibir un código de acceso denegado como **E \_ ACCESSDENIED**. Para evitar el error de acceso denegado, debe establecer la identidad del nuevo puntero con una llamada a la [**interfaz CoSetProxyBlanket.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)

Un proveedor puede establecer la seguridad en un espacio de nombres para que no se devuelva ningún dato a menos que use la privacidad de paquetes **(PktPrivacy)** en la conexión a ese espacio de nombres. Esto garantiza que los datos se cifran a medida que cruzan la red. Si intenta establecer un nivel de autenticación inferior, recibirá un mensaje de acceso denegado. Para obtener más información, vea [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).

Para obtener más información sobre cómo establecer la autenticación en scripting, vea [Establecer el nivel de seguridad de proceso predeterminado mediante VBScript.](setting-the-default-process-security-level-using-vbscript.md)

## <a name="setting-security-on-a-remote-iunknown-interface"></a>Establecer la seguridad en una interfaz IUnknown remota

En algunas situaciones, se requiere más acceso a un servidor que solo un puntero a un proxy. En ocasiones, es posible que tenga que obtener una conexión segura a la [**interfaz IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del proxy. Con **IUnknown,** puede consultar el sistema remoto para obtener interfaces y otras técnicas necesarias.

Cuando un proxy se encuentra en un equipo remoto, el servidor delega todas las llamadas a la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del proxy en la **interfaz IUnknown.** Por ejemplo, si llama a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en un proxy y la interfaz solicitada no formaba parte del proxy, el proxy envía la llamada al servidor remoto. A su vez, el servidor remoto comprueba la compatibilidad de la interfaz adecuada. Si el servidor admite la interfaz , COM serializa un nuevo proxy de nuevo al cliente para que la aplicación pueda usar la nueva interfaz.

Surgen problemas si el cliente no tiene permisos de acceso al servidor remoto, pero usa las credenciales de un usuario que sí lo tiene. En esta situación, se produce un error en cualquier intento de acceder [**a QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el servidor remoto. También se produce un error en la versión final del proxy, porque el usuario actual no tiene acceso al servidor remoto. Un síntoma de esto es un retraso de uno o dos segundos antes de que la aplicación cliente no se libere el proxy final. El error se produce porque COM intentó acceder al servidor remoto mediante la configuración de seguridad predeterminada del usuario actual, que no incluye las credenciales modificadas que permitían el acceso al servidor en primer lugar. Para obtener más información, vea [Establecer la seguridad en IWbemServices y otros servidores proxy.](setting-the-security-on-iwbemservices-and-other-proxies.md)

Para evitar errores de conexión, use [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) para establecer explícitamente la autenticación de seguridad en el puntero devuelto desde [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Con **CoSetProxyBlanket**, puede asegurarse de que el servidor remoto recibe la identidad de autenticación correcta.

En el ejemplo de código siguiente se muestra cómo [**usar CoSetProxyBlanket para**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) acceder a una [**interfaz IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) remota.


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
> Al establecer la seguridad en la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) de un proxy, COM crea una copia del proxy que no se puede liberar hasta que se llama a [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer la autenticación en WMI](setting-authentication-in-wmi.md)
</dt> </dl>

 

 
