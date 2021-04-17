---
description: 'En C++, puede establecer la seguridad en todo el proceso mediante una llamada a CoInitializeSecurity antes de conectarse a WMI a través de IWbemLocator:: ConnectServer.'
ms.assetid: 83c04a96-3829-4c07-91a7-06e5b75b2c12
ms.tgt_platform: multiple
title: Establecer la seguridad en IWbemServices y en otros servidores proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d593c52091182b1f0580908624e0b4068ed3f8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717036"
---
# <a name="setting-the-security-on-iwbemservices-and-other-proxies"></a>Establecer la seguridad en IWbemServices y en otros servidores proxy

En C++, puede establecer la seguridad en todo el proceso mediante una llamada a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) antes de conectarse a WMI a través de [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). También puede cambiar el nivel de autenticación, el nivel de suplantación o el servicio de autenticación en una llamada que obtiene un puntero a un proxy WMI, como [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) o [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult). La llamada a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) también le permite cambiar el servicio de autenticación (Kerberos, NTLM o Negotiate).

Los scripts y las aplicaciones de Visual Basic solo establecen de forma indirecta seguridad en los servidores proxy a través de llamadas a [**SWbemServices**](swbemservices.md) y otros objetos de automatización. Para obtener más información sobre cómo establecer y cambiar la autenticación y la suplantación en el script, vea [establecer el nivel de seguridad del proceso predeterminado con VBScript](setting-the-default-process-security-level-using-vbscript.md).

El cambio de niveles de seguridad o servicios es principalmente un problema al conectarse a WMI en un equipo remoto que ejecuta un sistema operativo diferente. Para obtener más información, consulte [conexión entre distintos sistemas operativos](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).

Una aplicación cliente se conecta a un proxy WMI mediante una identidad. Una identidad es un objeto de datos que consta de un nombre de usuario, una contraseña y una configuración de entidad. En el caso de una aplicación cliente WMI, la llamada a la interfaz [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) crea la identidad inicial. El método [**ConnectServer**](swbemlocator-connectserver.md) toma la identidad en un conjunto de tres parámetros, que se puede establecer en **null** para indicar el usuario actual. También puede especificar un parámetro que no sea **null** para indicar un usuario y un dominio específicos. Si la llamada se realiza correctamente, **ConnectServer** devuelve un puntero a través del cual se puede tener acceso a diversos procesos remotos, como un servicio WMI o el sistema operativo Windows directamente.

Al igual que muchas interfaces COM, [**ConnectServer**](swbemlocator-connectserver.md) devuelve un puntero a un proxy. Un proxy es un objeto de datos que representa un proceso remoto, como WMI o un proveedor remoto. COM usa un proxy para permitir que los desarrolladores tengan acceso a los datos remotos como si fueran locales.

Las siguientes interfaces WMI usan servidores proxy:

-   [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) (objeto de scripting de [**SWbemServices**](swbemservices.md) )
-   [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)
-   [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)
-   [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) (objeto de scripting de [**SWbemRefresher**](swbemrefresher.md) )

    El actualizador de WMI es un caso especial porque se le pasa un puntero [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , cuya configuración de seguridad debe estar establecida correctamente. Para obtener más información sobre el uso de objetos de actualización, vea [obtener acceso a los datos de rendimiento en C++](accessing-performance-data-in-c--.md).

Después de recibir un puntero a un proceso remoto, puede realizar una de estas dos acciones. Si sabe lo que hace el proceso, puede optar por establecer la seguridad en el puntero y acceder al proceso con normalidad. Este es el caso de la mayoría de los punteros a un servicio WMI. Para obtener más información, consulte [configuración de los niveles de seguridad en una conexión WMI](setting-the-security-levels-on-a-wmi-connection.md). Como alternativa, debe tener acceso a una interfaz COM diferente en el proxy, como [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release), a través de una llamada a la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) en el proxy.

## <a name="defaults-and-recommendations"></a>Valores predeterminados y recomendaciones

La versión distribuida del modelo de objetos componentes (DCOM) negocia el servicio de autenticación predeterminado (Kerberos, NTLM o Negotiate) y no se puede especificar el servicio de autenticación predeterminado mediante [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). La especificación de la **\_ \_ \_ opción predeterminada** de autenticación de RPC C en el parámetro del servicio de autenticación de [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) permite a DCOM seleccionar el servicio adecuado. En el caso de las conexiones remotas, el servicio predeterminado es Negotiate, que es el servicio recomendado para las aplicaciones que funcionan en dominios Kerberos y no Kerberos. En el caso de las conexiones locales, el servicio de autenticación predeterminado es NT LAN Manager (NTLM).

En el ejemplo de código siguiente se muestra el servicio de autenticación predeterminado que se está usando.


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



El ejemplo de código de este tema requiere las siguientes instrucciones Reference e \# include.


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



En el caso de los scripts, se recomienda usar los valores predeterminados que DCOM selecciona para las llamadas remotas. En el equipo local, no se puede especificar un servicio de autenticación para llamadas a WMI. Para obtener más información, vea [establecer el servicio de autenticación con VBScript](setting-the-authentication-service-using-vbscript.md) y [construir una cadena de moniker](constructing-a-moniker-string.md).

 

 
