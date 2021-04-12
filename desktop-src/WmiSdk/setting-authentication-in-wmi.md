---
description: Al realizar llamadas fuera del proceso de llamada o a un servicio WMI remoto, WMI utiliza la versión distribuida del modelo de objetos componentes (DCOM).
ms.assetid: 261b4f18-5de5-4e06-a887-f5afd9c45511
ms.tgt_platform: multiple
title: Configuración de la autenticación en WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0293d74c528e7c1c0e77a1ffb9f5f9ee7dfd5f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277696"
---
# <a name="setting-authentication-in-wmi"></a>Configuración de la autenticación en WMI

Al realizar llamadas fuera del proceso de llamada o a un servicio WMI remoto, WMI utiliza la versión distribuida del modelo de objetos componentes (DCOM). Las llamadas fuera de proceso y remotas se realizan a través de servidores proxy, que requieren la autenticación de las credenciales del proceso de llamada.

Establezca el nivel de autenticación al conectarse a un equipo y al espacio de nombres WMI. Para conectarse a WMI, llame a [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) en C++. En scripting o Visual Basic, se conecta a WMI mediante SWbemLocator. ConnectServer o a través de la cadena de [moniker](constructing-a-moniker-string.md) . La seguridad de DCOM y WMI requieren determinados niveles de autenticación al conectarse entre equipos. El nivel requerido es diferente según el sistema operativo que se va a conectar. Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés).

Normalmente, WMI se ejecuta en un host de servicio compartido y comparte la misma autenticación que otros procesos del host. Para ejecutar el proceso WMI con un nivel de autenticación diferente, ejecute WMI con el comando [**WinMgmt**](winmgmt.md) con el modificador **/standalonehost** y establezca el nivel de autenticación para WMI en general. Para obtener más información, vea [mantener la seguridad de WMI](maintaining-wmi-security.md).

Para obtener más información y ejemplos de código sobre cómo establecer la autenticación para las conexiones WMI, vea [establecer el servicio de autenticación con VBScript](setting-the-authentication-service-using-vbscript.md) y [establecer la autenticación con C++](setting-authentication-using-c-.md). Estos temas también contienen tablas que enumeran las constantes de autenticación para C++ y scripting.

## <a name="using-proxies-in-wmi"></a>Usar servidores proxy en WMI

Para establecer la autenticación de un proxy, llame a la función [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) . Para obtener más información y un ejemplo de código, vea [establecer la seguridad en IWbemServices y en otros servidores proxy](setting-the-security-on-iwbemservices-and-other-proxies.md).

La siguiente [API com para objetos WMI](com-api-for-wmi.md) usa servidores proxy directamente en C++ o C# para llamar a fuera de proceso o a un servicio WMI remoto:

-   [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)
-   [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)
-   [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)
-   [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)

Los objetos de scripting, como [**SWbemObject**](swbemobject.md), [**SWbemServices**](swbemservices.md)y [**SWbemRefresher**](swbemrefresher.md) , no usan servidores proxy directamente. En su lugar, los objetos de scripting representan un contenedor o una capa que llama a la [API com para](com-api-for-wmi.md) los objetos WMI enumerados anteriormente. Para obtener más información y un ejemplo de código sobre cómo establecer la autenticación en scripting, vea [establecer el nivel de seguridad del proceso predeterminado con VBScript](setting-the-default-process-security-level-using-vbscript.md).

 

 
