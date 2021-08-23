---
description: El servicio de autenticación Kerberos especifica el nombre principal del servidor para garantizar la identidad del equipo al que se conecta.
ms.assetid: 3d58db28-2e69-4e27-9f27-61529abbf750
ms.tgt_platform: multiple
title: Especificar el nombre principal del servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8b3d05d6933653a7d2a1737d36f00f6ca65c39bd7739e5f2e9f4232eb507f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816428"
---
# <a name="specifying-the-server-principal-name"></a>Especificar el nombre principal del servidor

El servicio de autenticación Kerberos especifica el nombre principal del servidor para garantizar la identidad del equipo al que se conecta. Especifique el nombre principal del servidor en la llamada al método de scripting [**SWbemLocator.ConnectServer,**](swbemlocator-connectserver.md) para lo que debe dar el nombre del equipo remoto. En C++, especifique el nombre principal del servidor en el *parámetro pServerPrincName* al llamar a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) para el proxy. Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés).

Este parámetro es necesario para que Kerberos admita la autenticación mutua. Sin embargo, el uso del nombre principal del servidor predeterminado no permite la autenticación mutua. Los clientes para los que la autenticación mutua es crítica deben especificar un nombre principal de servidor que coincida con la identidad del servidor que usa el servicio WMI. Para obtener más información sobre cómo establecer la seguridad de proxy y un ejemplo de C++ que muestra cómo establecer el nombre principal del servidor, vea Establecer la seguridad en [IWbemServices y otros servidores proxy.](setting-the-security-on-iwbemservices-and-other-proxies.md)

Para obtener más información sobre cómo establecer el nombre principal del servidor en el script y Visual Basic, vea [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) y [Conectarse a WMI](connecting-to-wmi-on-a-remote-computer.md)en un equipo remoto.

A diferencia de la mayoría de los protocolos de seguridad para Windows Management Instrumentation (WMI) y Component Object Model (COM), no se puede establecer la entidad de seguridad del servidor en una llamada a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). Sin embargo, puede establecer la entidad de seguridad del servidor con el parámetro *bstrAuthority* para [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)o el parámetro *pServerPrincName* para [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

El ejemplo de código de este tema requiere que la \# siguiente instrucción include se compile correctamente.


```C++
#include <wbemidl.h>
```



En el ejemplo de código siguiente se muestra cómo establecer el nombre principal del servidor con [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecimiento del servicio de autenticación mediante VBScript](setting-the-authentication-service-using-vbscript.md)
</dt> <dt>

[Establecer la autenticación mediante C++](setting-authentication-using-c-.md)
</dt> <dt>

[Establecer la seguridad en IWbemServices y otros servidores proxy](setting-the-security-on-iwbemservices-and-other-proxies.md)
</dt> </dl>

 

 
