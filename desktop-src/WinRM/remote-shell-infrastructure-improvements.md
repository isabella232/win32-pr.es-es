---
title: Mejoras en la infraestructura de Remote Shell
description: Windows Administración remota versión 2.0 (WinRM 2.0) ofrece muchas mejoras en la infraestructura de shell remoto.
ms.assetid: b22693ba-fa43-44bb-9b2d-0c64fad6e3cc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf88a472319b4b4677992f97509a3603cfe4a32f272388caf9db100b6e7457ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121665"
---
# <a name="remote-shell-infrastructure-improvements"></a>Mejoras en la infraestructura de Remote Shell

Windows Administración remota versión 2.0 (WinRM 2.0) ofrece muchas mejoras en la infraestructura de shell remoto. En los temas siguientes se describen estas mejoras en detalle:

-   [Compatibilidad con varios saltos](multi-hop-support.md)
-   [Administración de cuotas para shells remotos](quotas.md)

Una de las mejoras en la infraestructura de shell remoto de WinRM es la adición de un administrador de shell más sólido que mantiene la información de shell específica del usuario. Los usuarios de WinRM pueden crear shells en equipos remotos para ejecutar comandos o scripts. Además, los usuarios pueden crear varios shells en un equipo. Tanto los usuarios como los administradores necesitan la capacidad de administrar shells. Los usuarios pueden enumerar, obtener y eliminar los shells que han creado. Los administradores pueden enumerar todos los shells activos y recuperar detalles sobre shells específicos en un host local o remoto. Los administradores también pueden eliminar cualquier shell activo en un host local o remoto.

Cuando un usuario o administrador enumera los shells activos, el servicio WinRM puede devolver la siguiente información.

<dl> <dt>

<span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>ShellId
</dt> <dd>

Especifica el identificador único del shell.

</dd> <dt>

<span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>Variables de entorno
</dt> <dd>

Especifica las variables de entorno establecidas por el usuario.

</dd> <dt>

<span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>WorkingDirectory
</dt> <dd>

Especifica el directorio inicial del shell.

</dd> <dt>

<span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>ResourceURI
</dt> <dd>

Especifica el URI del recurso para la operación de shell. El URI del recurso se puede usar para recuperar la configuración del complemento que es específica de la instancia del shell.

</dd> <dt>

<span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout
</dt> <dd>

Especifica la duración máxima, en milisegundos, que el shell permanecerá abierto sin ninguna solicitud.

</dd> <dt>

<span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>InputStreams
</dt> <dd>

Especifica los flujos de entrada para el shell.

</dd> <dt>

<span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>OutputStreams
</dt> <dd>

Especifica los flujos de salida para el shell.

</dd> <dt>

<span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Hora de creación del shell
</dt> <dd>

Especifica la marca de tiempo de creación del shell.

</dd> <dt>

<span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>IdleTime
</dt> <dd>

Especifica la duración, en milisegundos, de que el shell ha estado inactivo.

</dd> <dt>

<span id="UserId"></span><span id="userid"></span><span id="USERID"></span>Userid
</dt> <dd>

Especifica el identificador de usuario.

</dd> <dt>

<span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>Nombre de host o dirección IP
</dt> <dd>

Especifica el nombre de host o la dirección IP del equipo que creó el shell.

</dd> <dt>

<span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Uso de memoria del shell
</dt> <dd>

Especifica la cantidad de memoria que ha usado el shell.

</dd> <dt>

<span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>Número de procesos
</dt> <dd>

Especifica el número de procesos creados por el shell.

</dd> </dl>

## <a name="enumerating-a-shell-on-a-local-host"></a>Enumerar un shell en un host local

El siguiente comando muestra cómo usar la utilidad winrm para enumerar los shells en un cliente winRM: **winrm enumerar shell**.

En el siguiente ejemplo basado en texto se muestra la salida de la enumeración de shell:

``` syntax
Shell
    ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E
    ResourceUri = http://schemas.microsoft.com/wbem/wsman/1/windows/shell/cmd
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin
    OutputStreams = stdout stderr
    ShellRunTime = P0DT0H0M36S
    ShellInactivity = P0DT0H0M35S

Shell
    ShellId = EE3F11CE-FB3C-4C4E-B113-6F4D643C97D8
    ResourceUri = http://schemas.microsoft.com/powershell/Microsoft.PowerShell
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin pr
    OutputStreams = stdout
    ShellRunTime = P0DT0H1M46S
    ShellInactivity = P0DT0H0M45S
    MemoryUsed = 48MB
    ChildProcesses = 0

Shell
    ShellId = 8FD7F2C4-A434-4D58-A7E8-46F8BF202D0B
    ResourceUri = http://schemas.microsoft.com/powershell/Microsoft.PowerShell
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin pr
    OutputStreams = stdout
    ShellRunTime = P0DT0H1M47S
    ShellInactivity = P0DT0H0M47S
    MemoryUsed = 48MB
    ChildProcesses = 0
```

Para obtener más información, vea la ayuda en línea proporcionada mediante la ejecución del siguiente comando: **winrm enumerate -?**.

## <a name="retrieving-information-about-a-specific-shell"></a>Recuperar información sobre un shell específico

Un administrador o usuario también puede usar el identificador ShellId para recuperar información sobre el shell. El siguiente comando muestra cómo usar la utilidad winrm para obtener información sobre un shell específico: **winrm get shell? ShellId=0A6E6A01-8AB2-4037-86CC-BFC826A1244E**.

En el siguiente ejemplo basado en texto se muestra la salida de la información del shell:

``` syntax
Shell
    ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E
    ResourceUri = http://schemas.microsoft.com/wbem/wsman/1/windows/shell/cmd
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin
    OutputStreams = stdout stderr
    ShellRunTime = P0DT0H0M36S
    ShellInactivity = P0DT0H0M35S
```

Para obtener más información, consulte la ayuda en línea proporcionada por el siguiente comando: **winrm get -?**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con varios saltos](multi-hop-support.md)
</dt> <dt>

[Administración de cuotas para shells remotos](quotas.md)
</dt> <dt>

[Referencia administrada para WS-Management comandos de PowerShell](winrm-powershell-commandlets.md)
</dt> </dl>

 

 




