---
description: En las secciones siguientes se describen los problemas comunes que pueden tener los desarrolladores con la creación de una conexión WMI remota.
ms.assetid: 328e420b-a859-4ce9-8a31-67150eb0a78f
ms.tgt_platform: multiple
title: Solución de problemas de una conexión WMI remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae475f91836b9e99b1c7faaf149c452e00a66722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696785"
---
# <a name="troubleshooting-a-remote-wmi-connection"></a>Solución de problemas de una conexión WMI remota

En las secciones siguientes se describen los problemas comunes que pueden tener los desarrolladores con la creación de una conexión WMI remota.

En este tema se describen las siguientes secciones:

-   [Acceso a DCOM denegado](#dcom-access-denied)
-   [Error de conexión](#failure-to-connect)
-   [Se agotó el tiempo de espera de la conexión WMI](#wmi-connection-timed-out)
-   [Temas relacionados](#related-topics)

## <a name="dcom-access-denied"></a>Acceso a DCOM denegado

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Manejo
</dt> <dd>

no se pudo realizar la conexión con el error "acceso a DCOM denegado", junto con el valor decimal-2147024891 o Hex value0x80070005.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Publicación
</dt> <dd>

Es posible que DCOM no esté configurado para permitir una conexión WMI.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Traducción
</dt> <dd>

Puede configurar DCOM para WMI mediante la utilidad de configuración DCOM (**DCOMCnfg.exe**) que se encuentra en **herramientas administrativas** del **Panel de control**. Esta utilidad expone la configuración que permite a determinados usuarios conectarse al equipo de forma remota a través de DCOM. Los miembros del grupo administradores pueden conectarse remotamente al equipo de forma predeterminada. Con esta utilidad puede establecer la seguridad para iniciar, tener acceso y configurar el servicio WMI.

Para obtener más información, consulte [protección de una conexión WMI remota](securing-a-remote-wmi-connection.md).

</dd> </dl>

## <a name="failure-to-connect"></a>Error de conexión

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Manejo
</dt> <dd>

No se puede conectar a WMI en un sistema remoto.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Publicación
</dt> <dd>

Es posible que esté intentando conectarse a un sistema que no es compatible con WMI. No se admiten las siguientes conexiones entre versiones de sistema operativo:

-   No se puede conectar a un equipo que ejecute una edición Starter, Basic o Home.

Como alternativa, es posible que esté intentando conectarse a un espacio de nombres que requiera una conexión cifrada, una que requiera un nivel de autenticación `pktPrivacy` , **WbemAuthenticationLevelPktPrivacy** o una **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Traducción
</dt> <dd>

Para obtener más información, vea [proteger los espacios de nombres de WMI](securing-wmi-namespaces.md), [proteger los clientes y proveedores de C++](securing-c---clients-and-providers.md)o [establecer el nivel de seguridad de proceso predeterminado con VBScript](setting-the-default-process-security-level-using-vbscript.md).

</dd> </dl>

## <a name="wmi-connection-timed-out"></a>Se agotó el tiempo de espera de la conexión WMI

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Manejo
</dt> <dd>

Se agota el tiempo de espera de la conexión WMI.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Publicación
</dt> <dd>

Debido a problemas de retraso de red, el equipo no es capaz de responder a tiempo.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Traducción
</dt> <dd>

Al conectarse a WMI a través de una llamada a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) o [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), puede establecer el valor de la marca **wbemConnectFlagUseMaxWait** (scripting) o la marca WBEM de la opción **\_ \_ Connect \_ use \_ Max \_ Wait** in C++ en 128 (0x80) para imponer un tiempo de espera de dos (2) minutos en la llamada.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 



