---
description: La conexión a un espacio de nombres WMI en un equipo remoto puede requerir que se cambie la configuración del firewall de Windows, el control de cuentas de usuario (UAC), DCOM o el administrador de objetos de Modelo de información común (CIMOM).
ms.assetid: 028b3101-0945-4288-bf32-ef4ad12a55f9
ms.tgt_platform: multiple
title: Configuración de una conexión WMI remota
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6ee254e12ecd806cd286d4a55746e203a3136b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544846"
---
# <a name="setting-up-a-remote-wmi-connection"></a>Configuración de una conexión WMI remota

La conexión a un espacio de nombres WMI en un equipo remoto puede requerir que se cambie la configuración del [firewall de Windows](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), el control de [cuentas de usuario (UAC)](/previous-versions/aa905108(v=msdn.10)), DCOM o el administrador de objetos de modelo de información común (CIMOM).

En este tema se describen las siguientes secciones:

-   [Configuración de Firewall de Windows](#windows-firewall-settings)
-   [Configuración de Control de cuentas de usuario](#user-account-control-settings)
-   [Configuración de DCOM](#dcom-settings)
-   [Configuración de CIMOM](#cimom-settings)
-   [Temas relacionados](#related-topics)

## <a name="windows-firewall-settings"></a>Configuración de Windows Firewall

La configuración de WMI para la configuración de Firewall de Windows solo permite conexiones WMI, en lugar de otras aplicaciones DCOM.

Debe establecerse una excepción en el firewall para WMI en el equipo de destino remoto. La excepción para WMI permite a WMI recibir conexiones remotas y devoluciones de llamada asincrónicas para Unsecapp.exe. Para obtener más información, vea [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).

Si una aplicación cliente crea su propio receptor, ese receptor debe agregarse explícitamente a las excepciones de Firewall para permitir que las devoluciones de llamada se realicen correctamente.

La excepción para WMI también funciona si se ha iniciado WMI con un puerto fijo, mediante el comando **WinMgmt/standalonehost** . Para obtener más información, consulte [configuración de un puerto fijo para WMI](setting-up-a-fixed-port-for-wmi.md).

Puede habilitar o deshabilitar el tráfico WMI a través de la interfaz de usuario del firewall de Windows.

**Para habilitar o deshabilitar el tráfico WMI mediante la interfaz de usuario del firewall**

1.  En el **Panel de control**, haga clic en **seguridad** y, a continuación, en **firewall de Windows**.
2.  Haga clic en **Cambiar configuración** y, a continuación, haga clic en la pestaña **excepciones** .
3.  En la ventana excepciones, active la casilla de **instrumental de administración de Windows (WMI)** para habilitar el tráfico WMI a través del firewall. Para deshabilitar el tráfico WMI, desactive la casilla.

Puede habilitar o deshabilitar el tráfico WMI a través del firewall en el símbolo del sistema.

**Para habilitar o deshabilitar el tráfico WMI en el símbolo del sistema mediante el grupo de reglas WMI**

-   Use los comandos siguientes en un símbolo del sistema. Escriba lo siguiente para habilitar el tráfico WMI a través del firewall.

    **netsh advfirewall firewall set Rule Group = "instrumental de administración de Windows (WMI)" New enable = Yes**

    Escriba el siguiente comando para deshabilitar el tráfico WMI a través del firewall.

    **netsh advfirewall firewall set Rule Group = "instrumental de administración de Windows (WMI)" New enable = no**

En lugar de usar el comando de grupo de reglas de WMI único, también puede usar comandos individuales para cada uno de los servicios DCOM, WMI y Sink.

**Para habilitar el tráfico WMI mediante reglas independientes para DCOM, WMI, receptor de devoluciones de llamada y conexiones salientes**

1.  Para establecer una excepción de Firewall para el puerto DCOM 135, use el siguiente comando.

    **netsh advfirewall Firewall Add Rule Dir = in name = "DCOM" Program =% SystemRoot% \\ system32 \\svchost.exe Service = RPCSS Action = allow Protocol = TCP localport = 135**

2.  Para establecer una excepción de Firewall para el servicio WMI, use el siguiente comando.

    **netsh advfirewall Firewall Add Rule Dir = in name = "WMI" Program =% SystemRoot% \\ system32 \\svchost.exe Service = WinMgmt Action = allow Protocol = TCP localport = any**

3.  Para establecer una excepción de Firewall para el receptor que recibe las devoluciones de llamada desde un equipo remoto, use el siguiente comando.

    **netsh advfirewall Firewall Add Rule Dir = in name = "UnsecApp" Program =% SystemRoot% \\ system32 \\ WBEM \\unsecapp.exe Action = allow**

4.  Para establecer una excepción de Firewall para las conexiones salientes a un equipo remoto con el que el equipo local se comunica de forma asincrónica, use el siguiente comando.

    **netsh advfirewall Firewall Add Rule dir = out name = "WMI \_ out" Program =% SystemRoot% \\ system32 \\svchost.exe Service = WinMgmt Action = allow Protocol = TCP localport = any**

Para deshabilitar las excepciones de Firewall por separado, use los comandos siguientes.

**Para deshabilitar el tráfico WMI mediante reglas independientes para DCOM, WMI, receptor de devoluciones de llamada y conexiones salientes**

1.  Para deshabilitar la excepción DCOM.

    **netsh advfirewall Firewall Delete Rule name = "DCOM"**

2.  Para deshabilitar la excepción de servicio WMI.

    **netsh advfirewall Firewall Delete Rule name = "WMI"**

3.  Para deshabilitar la excepción de receptor.

    **netsh advfirewall Firewall Delete Rule name = "UnsecApp"**

4.  Para deshabilitar la excepción de salida.

    **netsh advfirewall Firewall Delete Rule name = "WMI \_ out"**

## <a name="user-account-control-settings"></a>Configuración de Control de cuentas de usuario

El filtrado de tokens de acceso de control de cuentas de usuario (UAC) puede afectar a las operaciones permitidas en los espacios de nombres WMI o a los datos que se devuelven. En UAC, todas las cuentas del grupo de administradores locales se ejecutan con un [*token de acceso*](/windows/desktop/SecGloss/a-gly)de usuario estándar, también conocido como filtrado de tokens de acceso de UAC. Una cuenta de administrador puede ejecutar un script con privilegios elevados, "ejecutar como administrador".

Cuando no se conecta a la cuenta predefinida de administrador, UAC afecta a las conexiones a un equipo remoto de forma distinta en función de si los dos equipos están en un dominio o un grupo de trabajo. Para obtener más información sobre UAC y las conexiones remotas, vea [control de cuentas de usuario y WMI](user-account-control-and-wmi.md).

## <a name="dcom-settings"></a>Configuración de DCOM

Para obtener más información sobre la configuración de DCOM, consulte [protección de una conexión WMI remota](securing-a-remote-wmi-connection.md). Sin embargo, UAC afecta a las conexiones para las cuentas de usuario que no son de dominio. Si se conecta a un equipo remoto mediante una cuenta de usuario que no es de dominio incluida en el grupo de administradores local del equipo remoto, debe conceder explícitamente derechos de acceso remoto DCOM, activación e inicio a la cuenta.

## <a name="cimom-settings"></a>Configuración de CIMOM

La configuración de CIMOM debe actualizarse si la conexión remota se realiza entre equipos que no tienen una relación de confianza. de lo contrario, se producirá un error en una conexión asincrónica. Esta configuración no se debe modificar para los equipos que se encuentra en el mismo dominio o en dominios de confianza.

La siguiente entrada del registro debe modificarse para permitir las devoluciones de llamada anónimas:

**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **AllowAnonymousCallback**<dl> <dt>

               Data type
</dt> <dd>               \_valor DWORD reg</dd> </dl>

Si el valor de **AllowAnonymousCallback** se establece en 0, el servicio WMI impide las devoluciones de llamada anónimas al cliente. Si el valor se establece en 1, el servicio WMI permite devoluciones de llamada anónimas al cliente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
