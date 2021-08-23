---
description: En C++ puede establecer la seguridad en todo el proceso llamando a CoInitializeSecurity antes de conectarse a WMI a través de IWbemLocator::ConnectServer.
ms.assetid: 83c04a96-3829-4c07-91a7-06e5b75b2c12
ms.tgt_platform: multiple
title: Establecer la seguridad en IWbemServices y otros servidores proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da997b9d4a8f91cf31e8619af983209d4a07a571932c85304d372379d7f752b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050273"
---
# <a name="setting-the-security-on-iwbemservices-and-other-proxies"></a>Establecer la seguridad en IWbemServices y otros servidores proxy

Mientras esté en C++ puede establecer la seguridad en todo el proceso llamando a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) antes de conectarse a WMI a través de [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). También puede cambiar el nivel de autenticación, el nivel de suplantación o el servicio de autenticación en una llamada que obtiene un puntero a un proxy WMI, como [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) o [**IWbemCallResult.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) Llamar [**a CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) también le permite cambiar el servicio de autenticación (Kerberos, NTLM o negotiate).

Los scripts y Visual Basic solo establecen la seguridad en los servidores proxy indirectamente a través de llamadas a [**SWbemServices**](swbemservices.md) y otros objetos de automatización. Para obtener más información sobre cómo establecer y cambiar la autenticación y la suplantación en el script, vea Establecer el nivel de seguridad [de proceso predeterminado mediante VBScript.](setting-the-default-process-security-level-using-vbscript.md)

Cambiar los niveles de seguridad o los servicios es principalmente un problema al conectarse a WMI en un equipo remoto que ejecuta un sistema operativo diferente. Para obtener más información, vea [Conectarse entre diferentes sistemas operativos.](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)

Una aplicación cliente se conecta a un proxy WMI mediante una identidad. Una identidad es un objeto de datos que consta de un nombre de usuario, una contraseña y una configuración de autoridad. Para una aplicación cliente WMI, la llamada a la [**interfaz IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) crea la identidad inicial. El [**método ConnectServer**](swbemlocator-connectserver.md) toma la identidad en un conjunto de tres parámetros, que puede establecer en **NULL** para indicar el usuario actual. También puede especificar un parámetro que **no sea NULL** para indicar un usuario y un dominio específicos. Si la llamada se realiza correctamente, **ConnectServer** devuelve un puntero a través del cual puede tener acceso a una variedad de procesos remotos, como un servicio WMI o Windows sistema operativo directamente.

Al igual que muchas interfaces COM, [**ConnectServer**](swbemlocator-connectserver.md) devuelve un puntero a un proxy. Un proxy es un objeto de datos que representa un proceso remoto, como WMI o un proveedor remoto. COM usa un proxy para permitir que los desarrolladores accedan a datos remotos como si los datos fueran locales.

Las siguientes interfaces WMI usan servidores proxy:

-   [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) ( objeto de scripting [**SWbemServices)**](swbemservices.md)
-   [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)
-   [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)
-   [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) ( objeto de scripting [**SWbemRefresher)**](swbemrefresher.md)

    El actualizador wmi es un caso especial porque se pasa un puntero [**IWbemServices,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) cuya configuración de seguridad debe establecerse correctamente. Para obtener más información sobre el uso de objetos de actualizador, vea [Acceso a datos de rendimiento en C++.](accessing-performance-data-in-c--.md)

Después de recibir un puntero a un proceso remoto, puede hacer una de estas dos cosas. Si sabe lo que hace el proceso, puede establecer la seguridad en el puntero y acceder al proceso con normalidad. Este es el caso de la mayoría de los punteros a un servicio WMI. Para obtener más información, vea [Establecer los niveles de seguridad en una conexión WMI.](setting-the-security-levels-on-a-wmi-connection.md) Como alternativa, debe tener acceso a una interfaz COM diferente en el proxy, como [**IUnknown::Release,**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)a través de una llamada a la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) en el proxy.

## <a name="defaults-and-recommendations"></a>Valores predeterminados y Recomendaciones

La versión distribuida del modelo de objetos componentes (DCOM) negocia el servicio de autenticación predeterminado (Kerberos, NTLM o Negotiate) y no se puede especificar el servicio de autenticación predeterminado mediante [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). Si se **especifica RPC \_ C \_ AUTHN \_ DEFAULT** en el parámetro del servicio de autenticación [**de CoSetProxyBlanket,**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) DCOM puede seleccionar el servicio adecuado. Para las conexiones remotas, el servicio predeterminado es Negotiate, que es el servicio recomendado para las aplicaciones que funcionan en dominios Kerberos y no Kerberos. Para las conexiones locales, el servicio de autenticación predeterminado es NT LAN Manager (NTLM).

En el ejemplo de código siguiente se muestra el servicio de autenticación predeterminado que se está utilizando.


```C++
// The pWbemServices variable is of type IWbemServices*

HRESULT hr = CoSetProxyBlanket(
     pWbemServices,                //Proxy
     RPC_C_AUTHN_DEFAULT,          //Authentication service 
     RPC_C_AUTHZ_DEFAULT,          //Authorization service 
     COLE_DEFAULT_PRINCIPAL,       //Server principal name used 
                                       // by authentication service
     RPC_C_AUTHN_LEVEL_DEFAULT,    //Authentication level
     RPC_C_IMP_LEVEL_IMPERSONATE,  //Impersonation level
     COLE_DEFAULT_AUTHINFO,       //Client identity
     EOAC_DEFAULT                  //Capability flags
     );
```



El ejemplo de código de este tema requiere las siguientes instrucciones reference \# e include.


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



Para el scripting, se recomienda usar los valores predeterminados que DCOM selecciona para las llamadas remotas. En el equipo local no se puede especificar un servicio de autenticación para las llamadas a WMI. Para obtener más información, vea [Establecer el servicio de autenticación mediante VBScript](setting-the-authentication-service-using-vbscript.md) y Construir una cadena de [Moniker](constructing-a-moniker-string.md).

 

 
