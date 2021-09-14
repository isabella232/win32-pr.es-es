---
description: La conexión a un espacio de nombres WMI en un equipo remoto puede requerir que cambie la configuración de firewall de Windows, control de cuentas de usuario (UAC), DCOM o administrador de objetos Modelo de información común (CIMOM).
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170521"
---
# <a name="setting-up-a-remote-wmi-connection"></a>Configuración de una conexión WMI remota

La conexión a un espacio de nombres WMI en un equipo remoto puede requerir que cambie la configuración de firewall de [Windows,](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11))control de cuentas de usuario [(UAC),](/previous-versions/aa905108(v=msdn.10))DCOM o administrador de objetos Modelo de información común (CIMOM).

En este tema se de abordan las secciones siguientes:

-   [Windows Firewall Configuración](#windows-firewall-settings)
-   [Configuración de Control de cuentas de usuario](#user-account-control-settings)
-   [DCOM Configuración](#dcom-settings)
-   [Cimom Configuración](#cimom-settings)
-   [Temas relacionados](#related-topics)

## <a name="windows-firewall-settings"></a>Configuración de Windows Firewall

La configuración de WMI Windows configuración del Firewall de archivos permite solo las conexiones WMI, en lugar de otras aplicaciones DCOM.

Se debe establecer una excepción en el firewall para WMI en el equipo de destino remoto. La excepción de WMI permite a WMI recibir conexiones remotas y devoluciones de llamada asincrónicas para Unsecapp.exe. Para obtener más información, vea [Establecer la seguridad en una llamada asincrónica.](setting-security-on-an-asynchronous-call.md)

Si una aplicación cliente crea su propio receptor, ese receptor debe agregarse explícitamente a las excepciones del firewall para permitir que las devoluciones de llamada se realizarán correctamente.

La excepción de WMI también funciona si WMI se ha iniciado con un puerto fijo, mediante el **comando winmgmt /standalonehost.** Para obtener más información, vea [Configurar un puerto fijo para WMI.](setting-up-a-fixed-port-for-wmi.md)

Puede habilitar o deshabilitar el tráfico WMI a través de la interfaz de usuario Windows firewall.

**Para habilitar o deshabilitar el tráfico WMI mediante la interfaz de usuario del firewall**

1.  En el Panel de control , **haga** clic en **Seguridad y,** a continuación, haga clic **Windows Firewall.**
2.  Haga **clic en Configuración** y, a continuación, haga clic en la **pestaña** Excepciones.
3.  En la ventana Excepciones, active la casilla de Windows **Management Instrumentation (WMI)** para habilitar el tráfico WMI a través del firewall. Para deshabilitar el tráfico WMI, desactive la casilla.

Puede habilitar o deshabilitar el tráfico WMI a través del firewall en el símbolo del sistema.

**Para habilitar o deshabilitar el tráfico WMI en el símbolo del sistema mediante el grupo de reglas WMI**

-   Use los siguientes comandos en un símbolo del sistema. Escriba lo siguiente para habilitar el tráfico WMI a través del firewall.

    **netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=yes**

    Escriba el siguiente comando para deshabilitar el tráfico WMI a través del firewall.

    **netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=no**

En lugar de usar el comando de grupo de reglas WMI único, también puede usar comandos individuales para cada DCOM, servicio WMI y receptor.

**Para habilitar el tráfico WMI mediante reglas independientes para DCOM, WMI, receptor de devolución de llamada y conexiones salientes**

1.  Para establecer una excepción de firewall para el puerto DCOM 135, use el siguiente comando.

    **netsh advfirewall firewall add rule dir=in name="DCOM" program=%systemroot% \\ system32 \\svchost.exe service=rpcss action=allow protocol=TCP localport=135**

2.  Para establecer una excepción de firewall para el servicio WMI, use el siguiente comando.

    **netsh advfirewall firewall add rule dir=in name ="WMI" program=%systemroot% \\ system32 \\svchost.exe service=winmgmt action = allow protocol=TCP localport=any**

3.  Para establecer una excepción de firewall para el receptor que recibe devoluciones de llamada de un equipo remoto, use el siguiente comando.

    **netsh advfirewall firewall add rule dir=in name ="UnsecApp" program=%systemroot% \\ system32 \\ wbem \\unsecapp.exe action=allow**

4.  Para establecer una excepción de firewall para las conexiones salientes a un equipo remoto con el que el equipo local se comunica de forma asincrónica, use el siguiente comando.

    **netsh advfirewall firewall add rule dir=out name ="WMI \_ OUT" program=%systemroot% \\ system32 \\svchost.exe service=winmgmt action=allow protocol=TCP localport=any**

Para deshabilitar las excepciones de firewall por separado, use los siguientes comandos.

**Para deshabilitar el tráfico WMI mediante reglas independientes para DCOM, WMI, receptor de devolución de llamada y conexiones salientes**

1.  Para deshabilitar la excepción DCOM.

    **netsh advfirewall firewall delete rule name="DCOM"**

2.  Para deshabilitar la excepción del servicio WMI.

    **netsh advfirewall firewall delete rule name="WMI"**

3.  Para deshabilitar la excepción de receptor.

    **netsh advfirewall firewall delete rule name="UnsecApp"**

4.  Para deshabilitar la excepción saliente.

    **netsh advfirewall firewall delete rule name="WMI \_ OUT"**

## <a name="user-account-control-settings"></a>Configuración de Control de cuentas de usuario

El filtrado de tokens de acceso de Control de cuentas de usuario (UAC) puede afectar a qué operaciones se permiten en los espacios de nombres WMI o qué datos se devuelven. En UAC, todas las cuentas del grupo administradores locales se ejecutan con un [*token*](/windows/desktop/SecGloss/a-gly)de acceso de usuario estándar, también conocido como filtrado de tokens de acceso de UAC. Una cuenta de administrador puede ejecutar un script con privilegios elevados: "Ejecutar como administrador".

Cuando no se conecta a la cuenta de administrador integrada, UAC afecta a las conexiones a un equipo remoto de forma diferente en función de si los dos equipos están en un dominio o un grupo de trabajo. Para obtener más información sobre UAC y las conexiones remotas, vea [Control de cuentas de usuario y WMI.](user-account-control-and-wmi.md)

## <a name="dcom-settings"></a>DCOM Configuración

Para obtener más información sobre la configuración de DCOM, vea [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md). Sin embargo, UAC afecta a las conexiones de cuentas de usuario que no son de dominio. Si se conecta a un equipo remoto mediante una cuenta de usuario que no es de dominio incluida en el grupo administradores local del equipo remoto, debe conceder explícitamente derechos de inicio, activación e acceso DCOM remoto a la cuenta.

## <a name="cimom-settings"></a>Cimom Configuración

La configuración de CIMOM debe actualizarse si la conexión remota está entre equipos que no tienen una relación de confianza; De lo contrario, se producirá un error en una conexión asincrónica. Esta configuración no debe modificarse para equipos del mismo dominio o en dominios de confianza.

La siguiente entrada del Registro debe modificarse para permitir devoluciones de llamada anónimas:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **AllowAnonymousCallback**<dl> <dt>

               Data type
</dt> <dd>               REG \_ DWORD</dd> </dl>

Si el **valor AllowAnonymousCallback** se establece en 0, el servicio WMI impide las devoluciones de llamada anónimas al cliente. Si el valor se establece en 1, el servicio WMI permite devoluciones de llamada anónimas al cliente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
