---
title: Configurar el registro para asignaciones de puerto y enlace selectivo
description: A partir de Windows 2000, se debe usar una utilidad en el kit de recursos de Windows denominada Rpccfg.exe para establecer enlaces. Para obtener más información, consulte el kit de recursos de Windows para conocer la versión del sistema operativo adecuada.
ms.assetid: a33b51e7-2ded-46bd-aadb-27cbd99e1029
keywords:
- RPC llamada a procedimiento remoto, tareas, configurar el registro para asignaciones de puerto y enlace selectivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef1749fab1beb8e637d208a7d7af64577066fe6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103995706"
---
# <a name="configuring-the-registry-for-port-allocations-and-selective-binding"></a>Configurar el registro para asignaciones de puerto y enlace selectivo

A partir de Windows 2000, se debe usar una utilidad en el kit de recursos de Windows denominada Rpccfg.exe para establecer enlaces. Para obtener más información, consulte el kit de recursos de Windows para conocer la versión del sistema operativo adecuada.

En el caso de las versiones de Windows anteriores a Windows 2000, las claves del registro de la tabla siguiente especifican los valores predeterminados del sistema para la asignación dinámica de puertos y para el enlace a NIC en equipos de host múltiple. Primero debe crear estas claves y, a continuación, especificar la configuración adecuada.

El uso de la función [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) afecta a esta configuración. Los desarrolladores deben estar familiarizados con la configuración del registro que se explica en esta sección y la función **RpcServerUseProtseqEx** al administrar las asignaciones de puertos. Un ejemplo con tres aplicaciones hipotéticas sigue la tabla siguiente y muestra cómo interoperan esta configuración y la función **RpcServerUseProtseqEx** .

Si falta una clave o contiene un valor no válido, toda la configuración se marca como no válida y se producirá un error en todas las llamadas a **RpcServerUseProtseq \*** a través de [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) o [**ncadg \_ IP \_ UDP**](/windows/desktop/Midl/ncadg-ip-udp) .

> [!Note]  
> Los puertos asignados a un proceso permanecen asignados hasta que se agota el proceso. Si todos los puertos disponibles están en uso, la función devuelve \_ \_ \_ \_ los recursos de RPC.

 



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Clave de Puerto</th>
<th>Tipo de datos</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               Ports</code></pre></td>
<td><strong>REG_MULTI_SZ</strong></td>
<td>Especifica un conjunto de intervalos de puertos IP que consta de todos los puertos disponibles en Internet o de todos los puertos que no están disponibles en Internet. Cada cadena representa un único puerto o un conjunto inclusivo de puertos (por ejemplo, 1000-1050, 1984). Si alguna entrada está fuera del intervalo comprendido entre 0 y 65535, o si no se puede interpretar una cadena, el tiempo de ejecución de RPC tratará toda la configuración como no válida.</td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               PortsInternetAvailable</code></pre></td>
<td><strong>REG_SZ</strong></td>
<td>Y o N (no distingue entre mayúsculas y minúsculas). Si es Y, los puertos enumerados en la clave puertos son todos los puertos disponibles en Internet de ese equipo. Si es N, los puertos enumerados en la clave de puertos son todos los puertos que no están disponibles en Internet.</td>
</tr>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               UseInternetPorts</code></pre></td>
<td><strong>REG_SZ</strong></td>
<td>Y o N (no distingue entre mayúsculas y minúsculas). Especifica la directiva predeterminada del sistema. Si es Y, los procesos que usan el valor predeterminado serán puertos asignados del conjunto de puertos disponibles para Internet, tal como se ha definido anteriormente. Si es N, los procesos que usan el valor predeterminado serán puertos asignados del conjunto de puertos solo de la intranet.</td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rpc
               Linkage
                  Bind</code></pre></td>
<td><strong>REG_MULTI_SZ</strong></td>
<td>Enumera los nombres de los dispositivos de todas las NIC en las que se va a enlazar de forma predeterminada (por ejemplo, \Device\AMDPCN1). Si la clave no existe, el servidor se enlazará a todas las NIC. Si la clave existe, el servidor se enlazará a las NIC especificadas en la clave, a menos que el campo NICFlags se establezca en RPC_C_BIND_TO_ALL_NICS. Si la clave tiene un valor null ( &quot; &quot; ), la configuración se marcará como no válida y se producirá un error en todas las llamadas a <strong>RpcServerUseProtseq *</strong> en <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong>ncacn_ip_tcp</strong></a> o <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a> .</td>
</tr>
</tbody>
</table>



 

En la tabla siguiente se muestra cómo las tres aplicaciones de ejemplo se ven afectadas por la configuración definida en la tabla anterior, y cómo también se ven afectadas las Configuraciones aplicadas mediante la función [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .

En este ejemplo, se consideran tres aplicaciones hipotéticas:

-   Internetapp: esta aplicación está diseñada para su exposición a Internet y ha especificado el puerto de Internet de RPC \_ C \_ \_ \_ en el miembro **EndpointFlags** de la estructura de la [**\_ Directiva RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) pasada a la función [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .
-   LocalApp: esta aplicación no está pensada para su exposición a Internet y ha especificado RPC \_ C \_ use \_ el \_ Puerto de la intranet en el miembro **EndpointFlags** de la estructura de la [**\_ Directiva RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) pasada a la función [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .
-   DefaultApp: esta aplicación especifica cero en el miembro **EndpointFlags** de la estructura de la [**\_ Directiva RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) pasada a la función [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .

En la tabla siguiente se explica el impacto que estas opciones tienen en función de los valores especificados en las entradas del registro explicadas en la tabla anterior. En el caso de las consideraciones de formato, se asignan los siguientes códigos:

PIA = valor de clave PortsInternetAvailable

UIP = valor de clave UseInternetPorts

En este ejemplo, el valor de la clave ports es 5000-5100 para cada entrada.



| Application | PIA | UIP | Resultado                                  |
|-------------|-----|-----|-----------------------------------------|
| Entre netApp | Y   | Y   | Usa puertos entre 5000 y 5100        |
| LocalApp    | Y   | Y   | Usa un puerto fuera del intervalo de 5000-5100 |
| DefaultApp  | Y   | Y   | Usa puertos entre 5000 y 5100        |
| Entre netApp | Y   | N   | Usa puertos entre 5000 y 5100        |
| LocalApp    | Y   | N   | Usa un puerto fuera del intervalo de 5000-5100 |
| DefaultApp  | Y   | N   | Usa un puerto fuera del intervalo de 5000-5100 |
| Entre netApp | N   | Y   | Usa un puerto fuera del intervalo de 5000-5100 |
| LocalApp    | N   | Y   | Usa puertos entre 5000 y 5100        |
| DefaultApp  | N   | Y   | Usa un puerto fuera del intervalo de 5000-5100 |
| Entre netApp | N   | N   | Usa un puerto fuera del intervalo de 5000-5100 |
| LocalApp    | N   | N   | Usa puertos entre 5000 y 5100        |
| DefaultApp  | N   | N   | Usa puertos entre 5000 y 5100        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**\_Directiva RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)
</dt> <dt>

[**RpcServerUseAllProtseqsEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex)
</dt> <dt>

[**RpcServerUseAllProtseqsIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex)
</dt> <dt>

[**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)
</dt> <dt>

[**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)
</dt> <dt>

[**RpcServerUseProtseqIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqifex)
</dt> <dt>

[**\_TCP IP \_ ncacn**](/windows/desktop/Midl/ncacn-ip-tcp)
</dt> <dt>

[**ncadg \_ IP \_ UDP**](/windows/desktop/Midl/ncadg-ip-udp)
</dt> </dl>

 

 