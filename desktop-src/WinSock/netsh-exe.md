---
description: Los comandos Netsh para IPv6 proporcionan una herramienta de línea de comandos que puede usar para consultar y configurar interfaces, direcciones, cachés y rutas de IPv6. Los comandos IPv6 de la interfaz Netsh se admiten en Windows XP con Service Pack 1 (SP1) y versiones posteriores.
ms.assetid: 68e17a55-4dd5-40cd-8996-25fa278ddd19
title: Netsh.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c283206a8000c101b437bee851f9a78f6f20f0d87de544e8b5db49909ea9bf6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993645"
---
# <a name="netshexe"></a>Netsh.exe

Los comandos Netsh para IPv6 proporcionan una herramienta de línea de comandos que puede usar para consultar y configurar interfaces, direcciones, cachés y rutas de IPv6. Los comandos IPv6 de la interfaz Netsh se admiten en Windows XP con Service Pack 1 (SP1) y versiones posteriores.

Netsh.exe tiene muchos subcomandos para IPv6. En el símbolo del sistema de Windows XP con SP1 y versiones posteriores, puede obtener una lista completa de las opciones de Netsh Interface IPv6; para ello, escriba lo siguiente:

**netsh interface ipv6 /?**

La documentación sobre todos los **comandos netsh** para IPv6 también está disponible en línea en Technet. Para obtener más información sobre **netsh** en Windows Server 2008, vea Comandos de Netsh para [interface (IPv4 e IPv6).](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770948(v=ws.10)) Para obtener más información sobre **netsh** en Windows Server 2003, vea Comandos netsh para [la interfaz IPv6.](/previous-versions/windows/it-pro/windows-server-2003/cc740203(v=ws.10))

Estos son algunos comandos que se usan con frecuencia para IPv6, aunque se admiten muchos otros comandos:

<dl> <dt>

<span id="netsh_interface_ipv6_add_address"></span><span id="NETSH_INTERFACE_IPV6_ADD_ADDRESS"></span>**netsh interface ipv6 add address**
</dt> <dd>

Agrega una dirección IPv6 a una interfaz específica en el equipo local. Este comando tiene parámetros de subopción que se deben especificar.

</dd> <dt>

<span id="netsh_interface_ipv6_add_dns"></span><span id="NETSH_INTERFACE_IPV6_ADD_DNS"></span>**netsh interface ipv6 add dns**
</dt> <dd>

Agrega una dirección IPv6 del servidor DNS a la lista de servidores DNS configurada estáticamente para la interfaz especificada en el equipo local. Este comando tiene parámetros de subopción que se deben especificar.

</dd> <dt>

<span id="netsh_interface_ipv6_add_route"></span><span id="NETSH_INTERFACE_IPV6_ADD_ROUTE"></span>**netsh interface ipv6 add route**
</dt> <dd>

Agrega una ruta para una dirección de prefijo IPv6 especificada en el equipo local. Este comando tiene parámetros de subopción que se deben especificar.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_address"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ADDRESS"></span>**netsh interface ipv6 delete address**
</dt> <dd>

Elimina la dirección IPv6 especificada de una interfaz específica en el equipo local. Este comando tiene parámetros de subopción que se deben especificar.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_dns"></span><span id="NETSH_INTERFACE_IPV6_DELETE_DNS"></span>**netsh interface ipv6 delete dns**
</dt> <dd>

Elimina una dirección de servidor DNS de la lista de servidores DNS configurada estáticamente para la interfaz especificada en el equipo local. Este comando tiene parámetros de subopción que se deben especificar.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_interface"></span><span id="NETSH_INTERFACE_IPV6_DELETE_INTERFACE"></span>**netsh interface ipv6 delete interface**
</dt> <dd>

Elimina una interfaz especificada de la pila IPv6 en el equipo local. Este comando tiene parámetros de subopción que se deben especificar.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_route"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ROUTE"></span>**netsh interface ipv6 delete route**
</dt> <dd>

Elimina una ruta para una dirección de prefijo IPv6 especificada en el equipo local. Este comando tiene parámetros de subopción que se deben especificar.

</dd> <dt>

<span id="netsh_interface_ipv6_dump"></span><span id="NETSH_INTERFACE_IPV6_DUMP"></span>**netsh interface ipv6 dump**
</dt> <dd>

Crea un script que contiene los comandos para crear la configuración actual. Si se guarda en un archivo, este script se puede usar para restaurar la configuración modificada.

</dd> <dt>

<span id="netsh_interface_ipv6_install"></span><span id="NETSH_INTERFACE_IPV6_INSTALL"></span>**netsh interface ipv6 install**
</dt> <dd>

Instala el protocolo IPv6 en el equipo local.

</dd> <dt>

<span id="netsh_interface_ipv6_renew"></span><span id="NETSH_INTERFACE_IPV6_RENEW"></span>**netsh interface ipv6 renew**
</dt> <dd>

Reinicia las interfaces IPv6 en el equipo local.

</dd> <dt>

<span id="netsh_interface_ipv6_reset"></span><span id="NETSH_INTERFACE_IPV6_RESET"></span>**Restablecimiento de ipv6 de la interfaz netsh**
</dt> <dd>

Restablece el estado de configuración de IPv6 en el equipo local.

</dd> <dt>

<span id="netsh_interface_ipv6_show_global"></span><span id="NETSH_INTERFACE_IPV6_SHOW_GLOBAL"></span>**netsh interface ipv6 show global**
</dt> <dd>

Muestra los parámetros de configuración global para IPv6 en el equipo local.

</dd> <dt>

<span id="netsh_interface_ipv6_show_address"></span><span id="NETSH_INTERFACE_IPV6_SHOW_ADDRESS"></span>**netsh interface ipv6 show address**
</dt> <dd>

Muestra todas las direcciones IPv6 o todas las direcciones IPv6 en una interfaz específica del equipo local. Este comando tiene parámetros de subopción que es posible que deban especificarse.

</dd> <dt>

<span id="netsh_interface_ipv6_uninstall"></span><span id="NETSH_INTERFACE_IPV6_UNINSTALL"></span>**netsh interface ipv6 uninstall**
</dt> <dd>

Desinstala el protocolo IPv6 en el equipo local.

</dd> </dl>

## <a name="netsh-commands-for-ipv4"></a>Comandos Netsh para IPv4

Hay comandos netsh similares disponibles para IPv4. En el símbolo del sistema de Windows XP con SP1 y versiones posteriores, hay disponible una lista completa de las opciones de comandos de Netsh para su uso con IPv4. Para ello, escriba lo siguiente:

**netsh interface ip /?**

La documentación sobre todos los comandos netsh para IPv4 también está disponible en línea en Technet. Para más información, consulte [Comandos Netsh para ip de interfaz.](/previous-versions/windows/it-pro/windows-server-2003/cc738592(v=ws.10))

 

 
