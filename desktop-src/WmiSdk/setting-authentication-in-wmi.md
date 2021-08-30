---
description: Al realizar llamadas fuera del proceso de llamada o a un servicio WMI remoto, WMI usa la versión distribuida del Modelo de objetos componentes (DCOM).
ms.assetid: 261b4f18-5de5-4e06-a887-f5afd9c45511
ms.tgt_platform: multiple
title: Establecer la autenticación en WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f8807f018f48087e0806dd2dd0a3c4fd44c427ea4dca3af9ae23e7410a626b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860435"
---
# <a name="setting-authentication-in-wmi"></a>Establecer la autenticación en WMI

Al realizar llamadas fuera del proceso de llamada o a un servicio WMI remoto, WMI usa la versión distribuida del Modelo de objetos componentes (DCOM). Las llamadas remotas y fuera de proceso se realizan a través de servidores proxy, que requieren la autenticación de las credenciales del proceso de llamada.

El nivel de autenticación se establece al conectarse a un equipo y un espacio de nombres WMI. Para conectarse a WMI, llame [**a IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) en C++. En scripting o Visual Basic, se conecta a WMI mediante SWbemLocator.ConnectServer o a través de la [cadena de moniker.](constructing-a-moniker-string.md) La seguridad de DCOM y WMI requieren ciertos niveles de autenticación al conectarse entre equipos. El nivel necesario difiere en función del sistema operativo que se conecte. Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés).

WMI normalmente se ejecuta en un host de servicio compartido y comparte la misma autenticación que otros procesos del host. Para ejecutar el proceso WMI con un nivel de autenticación diferente, ejecute WMI con el comando [**winmgmt**](winmgmt.md) con el modificador **/standalonehost** y establezca el nivel de autenticación para WMI en general. Para obtener más información, vea [Mantenimiento de la seguridad WMI.](maintaining-wmi-security.md)

Para obtener más información y ejemplos de código sobre cómo establecer la autenticación para conexiones WMI, vea Establecer el servicio de autenticación mediante [VBScript](setting-the-authentication-service-using-vbscript.md) y Establecer la autenticación [mediante C++.](setting-authentication-using-c-.md) Estos temas también contienen tablas que muestran las constantes de autenticación para C++ y scripting.

## <a name="using-proxies-in-wmi"></a>Uso de servidores proxy en WMI

Para establecer la autenticación de un proxy, llame a la [**función CoSetProxyBlanket.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) Para obtener más información y un ejemplo de código, vea [Establecer la seguridad en IWbemServices y otros servidores proxy.](setting-the-security-on-iwbemservices-and-other-proxies.md)

La siguiente [API COM para objetos WMI](com-api-for-wmi.md) usa servidores proxy directamente en C++ o C# para llamar fuera de proceso o a un servicio WMI remoto:

-   [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)
-   [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)
-   [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)
-   [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)

Los objetos de scripting, [**como SWbemObject,**](swbemobject.md) [**SWbemServices**](swbemservices.md)y [**SWbemRefresher,**](swbemrefresher.md) no usan servidores proxy directamente. En su lugar, los objetos de scripting representan un contenedor o una capa que llama a la [API COM para los objetos WMI](com-api-for-wmi.md) enumerados anteriormente. Para obtener más información y un ejemplo de código de configuración de la autenticación en scripting, vea Establecer el nivel de seguridad [de proceso predeterminado mediante VBScript.](setting-the-default-process-security-level-using-vbscript.md)

 

 
