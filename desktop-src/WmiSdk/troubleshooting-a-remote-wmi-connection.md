---
description: En las secciones siguientes se describen los problemas comunes que pueden tener los desarrolladores con la creación de una conexión WMI remota.
ms.assetid: 328e420b-a859-4ce9-8a31-67150eb0a78f
ms.tgt_platform: multiple
title: Solución de problemas de una conexión WMI remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10603f713fecf861750d70c4166da91e081dc273a0d6d6134ed916a7f84f2bd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312421"
---
# <a name="troubleshooting-a-remote-wmi-connection"></a>Solución de problemas de una conexión WMI remota

En las secciones siguientes se describen los problemas comunes que pueden tener los desarrolladores con la creación de una conexión WMI remota.

En este tema se de abordan las siguientes secciones:

-   [Acceso denegado de DCOM](#dcom-access-denied)
-   [Error al Conectar](#failure-to-connect)
-   [Tiempo de espera de la conexión WMI](#wmi-connection-timed-out)
-   [Temas relacionados](#related-topics)

## <a name="dcom-access-denied"></a>Acceso denegado de DCOM

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Síntoma
</dt> <dd>

Error de conexión con el error "DCOM Access Denied", junto con el valor decimal -2147024891 o hexadecimal value0x80070005.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Problema
</dt> <dd>

Es posible que DCOM no esté configurado para permitir una conexión WMI.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolución
</dt> <dd>

Puede configurar las opciones de DCOM para WMI mediante la utilidad  de configuración de DCOM (**DCOMCnfg.exe**) que se encuentra en Herramientas **administrativas en Panel de control**. Esta utilidad expone la configuración que permite a determinados usuarios conectarse al equipo de forma remota a través de DCOM. Los miembros del grupo Administradores pueden conectarse de forma remota al equipo de forma predeterminada. Con esta utilidad puede establecer la seguridad para iniciar, acceder y configurar el servicio WMI.

Para obtener más información, [vea Proteger una conexión WMI remota.](securing-a-remote-wmi-connection.md)

</dd> </dl>

## <a name="failure-to-connect"></a>Error al Conectar

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Síntoma
</dt> <dd>

No se puede conectar a WMI en un sistema remoto.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Problema
</dt> <dd>

Es posible que esté intentando conectarse a un sistema que no admite WMI. No se admiten las siguientes conexiones entre las versiones del sistema operativo:

-   No se puede conectar a un equipo que ejecuta una edición Starter, Basic o Home.

Como alternativa, puede estar intentando conectarse a un espacio de nombres que requiere una conexión cifrada, que requiere un nivel de autenticación de `pktPrivacy` , **WbemAuthenticationLevelPktPrivacy** o **RPC C \_ \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolución
</dt> <dd>

Para obtener más información, vea [Securing WMI Namespaces](securing-wmi-namespaces.md), [Securing C++ Clients and Providers](securing-c---clients-and-providers.md)o [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).

</dd> </dl>

## <a name="wmi-connection-timed-out"></a>Tiempo de espera de la conexión WMI

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Síntoma
</dt> <dd>

Se ha pasado el tiempo de espera de la conexión WMI.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Problema
</dt> <dd>

Debido a problemas de retraso de red, el equipo simplemente no puede responder a tiempo.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolución
</dt> <dd>

Al conectarse a WMI mediante una llamada a [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) o [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), puede establecer la marca **wbemConnectFlagUseMaxWait** (scripting) o el valor **WBEM \_ FLAG CONNECT USE MAX \_ \_ \_ \_ WAIT** en C++ en 128 (0x80) para imponer un tiempo de espera de dos (2) minutos en la llamada.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 



