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
# <a name="specifying-the-server-principal-name"></a>Especificar el nombre de la entidad de seguridad del servidor

El servicio de autenticación Kerberos especifica el nombre de la entidad de seguridad del servidor para garantizar la identidad del equipo al que se está conectando. Especifique el nombre de la entidad de seguridad del servidor en la llamada al método de scripting [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) proporcionando el nombre del equipo remoto. En C++, especifique el nombre de la entidad de seguridad del servidor en el parámetro *pServerPrincName* al llamar a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) para el proxy. Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés).

Este parámetro es necesario para que Kerberos admita la autenticación mutua. Sin embargo, el uso del nombre de entidad de seguridad de servidor predeterminado no permite la autenticación mutua. Los clientes para los que la autenticación mutua es crítica, deben especificar un nombre de entidad de seguridad de servidor que coincida con la identidad del servidor que usa el servicio WMI. Para obtener más información sobre la configuración de la seguridad de proxy y un ejemplo de C++ que muestra cómo establecer el nombre principal del servidor, vea [establecer la seguridad en IWbemServices y en otros servidores proxy](setting-the-security-on-iwbemservices-and-other-proxies.md).

Para obtener más información acerca de cómo establecer el nombre de la entidad de seguridad de servidor en script y Visual Basic, vea [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) y [conectarse a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md).

A diferencia de la mayoría de los protocolos de seguridad de Instrumental de administración de Windows (WMI) y del modelo de objetos componentes (COM), no se puede establecer la entidad de seguridad de servidor en una llamada a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). Sin embargo, puede establecer la entidad de seguridad de servidor con el parámetro *bstrAuthority* para [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)o el parámetro *pServerPrincName* para [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

El ejemplo de código de este tema requiere la siguiente \# instrucción include para compilar correctamente.


```C++
#include <wbemidl.h>
```



En el ejemplo de código siguiente se muestra cómo establecer el nombre de la entidad de seguridad del servidor con [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).


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

[Establecer el servicio de autenticación mediante VBScript](setting-the-authentication-service-using-vbscript.md)
</dt> <dt>

[Establecer la autenticación con C++](setting-authentication-using-c-.md)
</dt> <dt>

[Establecer la seguridad en IWbemServices y en otros servidores proxy](setting-the-security-on-iwbemservices-and-other-proxies.md)
</dt> </dl>

 

 
