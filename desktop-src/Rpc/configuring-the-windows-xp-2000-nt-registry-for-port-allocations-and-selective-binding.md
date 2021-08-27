---
title: Configuración del Registro para asignaciones de puertos y enlace selectivo
description: A partir Windows 2000, se debe usar una utilidad del kit de recursos Windows llamada Rpccfg.exe para establecer enlaces. Para obtener más información, consulte el Windows Resource Kit para obtener la versión adecuada del sistema operativo.
ms.assetid: a33b51e7-2ded-46bd-aadb-27cbd99e1029
keywords:
- Llamada a procedimiento remoto RPC, tareas, configuración del Registro para asignaciones de puertos y enlace selectivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b220e0e3415b7906c847c0f1196fbc815521dee0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465482"
---
# <a name="configuring-the-registry-for-port-allocations-and-selective-binding"></a>Configuración del Registro para asignaciones de puertos y enlace selectivo

A partir Windows 2000, se debe usar una utilidad del kit de recursos Windows llamada Rpccfg.exe para establecer enlaces. Para obtener más información, consulte el Windows Resource Kit para obtener la versión adecuada del sistema operativo.

En el caso de las versiones de ventanas anteriores a Windows 2000, las claves del Registro de la tabla siguiente especifican los valores predeterminados del sistema para la asignación dinámica de puertos y para el enlace a NIC en equipos multihome. Primero debe crear estas claves y, a continuación, especificar la configuración adecuada.

El uso [**de la función RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) afecta a esta configuración. Los desarrolladores deben estar familiarizados con la configuración del Registro que se explica en esta sección y la función **RpcServerUseProtseqEx** al administrar las asignaciones de puertos. En la tabla siguiente se muestra un ejemplo con tres aplicaciones hipotéticas y se muestra cómo interoperan esta configuración y la función **RpcServerUseProtseqEx.**

Si falta una clave o si contiene un valor no válido, toda la configuración se marca como no válida y se producirá un error en todas las llamadas **RpcServerUseProtseq \** _ a [través de _ *ncacn \_ ip \_ tcp* *](/windows/desktop/Midl/ncacn-ip-tcp) o [**ncadg \_ ip \_ udp.**](/windows/desktop/Midl/ncadg-ip-udp)

> [!Note]  
> Los puertos asignados a un proceso permanecen asignados hasta que ese proceso falle. Si todos los puertos disponibles están en uso, la función devuelve RPC \_ S \_ OUT OF \_ \_ RESOURCES.

 




| Clave de puerto | Tipo de datos | Descripción | 
|----------|-----------|-------------|
| <pre data-space="preserve"><code>HKEY_LOCAL_MACHINE   Software      Microsoft         Rpc            Internet               Ports</code></pre> | <strong>REG_MULTI_SZ</strong> | Especifica un conjunto de intervalos de puertos IP que consta de todos los puertos disponibles de Internet o de todos los puertos no disponibles desde Internet. Cada cadena representa un único puerto o un conjunto inclusivo de puertos (por ejemplo, 1000-1050, 1984). Si alguna entrada está fuera del intervalo de 0 a 65535, o si no se puede interpretar alguna cadena, el tiempo de ejecución de RPC tratará toda la configuración como no válida. | 
| <pre data-space="preserve"><code>HKEY_LOCAL_MACHINE   Software      Microsoft         Rpc            Internet               PortsInternetAvailable</code></pre> | <strong>REG_SZ</strong> | Y o N (sin distingue mayúsculas de minúsculas). Si es Y, los puertos enumerados en la clave Puertos son todos los puertos disponibles para Internet en ese equipo. Si es N, los puertos enumerados en la clave Puertos son todos aquellos puertos que no están disponibles para Internet. | 
| <pre data-space="preserve"><code>HKEY_LOCAL_MACHINE   Software      Microsoft         Rpc            Internet               UseInternetPorts</code></pre> | <strong>REG_SZ</strong> | Y o N (sin distingue mayúsculas de minúsculas). Especifica la directiva predeterminada del sistema. Si es Y, a los procesos que usan el valor predeterminado se les asignarán puertos del conjunto de puertos disponibles para Internet, tal y como se definió anteriormente. Si es N, a los procesos que usan el valor predeterminado se les asignarán puertos del conjunto de puertos solo de intranet. | 
| <pre data-space="preserve"><code>HKEY_LOCAL_MACHINE   System      CurrentControlSet         Services            Rpc               Linkage                  Bind</code></pre> | <strong>REG_MULTI_SZ</strong> | Enumera los nombres de dispositivo de todas las NIC en las que se va a enlazar de forma predeterminada (por ejemplo, \Device\AMDPCN1). Si la clave no existe, el servidor se enlazará a todas las NIC. Si la clave existe, el servidor se enlazará a las NIC especificadas en la clave, a menos que el campo NICFlags esté establecido en RPC_C_BIND_TO_ALL_NICS. Si la clave tiene un valor null (""), la configuración se marcará como no válida y todas las llamadas a <strong>RpcServerUseProtseq*</strong> a través de <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong>ncacn_ip_tcp</strong></a> o <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a> producirán un error. | 




 

En la tabla siguiente se muestra cómo tres aplicaciones de ejemplo se ven afectadas por la configuración definida en la tabla anterior y cómo la configuración aplicada mediante la [**función RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) también se ve afectada.

En este ejemplo, se tienen en cuenta tres aplicaciones hipotéticas:

-   InternetApp: esta aplicación está pensada para la exposición a Internet y ha especificado RPC C USE INTERNET PORT en el miembro EndpointFlags de la estructura RPC POLICY pasada a la \_ \_ función \_ \_ [**RpcServerUseProtseqEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) [**\_**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) 
-   LocalApp: esta aplicación no está pensada para la exposición a Internet y ha especificado RPC C USE INTRANET PORT en el miembro EndpointFlags de la estructura RPC POLICY pasada a la \_ \_ función \_ \_ [**RpcServerUseProtseqEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) [**\_**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) 
-   DefaultApp: esta aplicación especifica cero en el miembro **EndpointFlags** de la estructura [**RPC \_ POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) pasada a la [**función RpcServerUseProtseqEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)

En la tabla siguiente se explica el impacto que tienen estas configuraciones en función de los valores especificados en las entradas del Registro que se explican en la tabla anterior. Para las consideraciones de formato, se asignan los códigos siguientes:

PIA = Valor de clave PortsInternetAvailable

UIP = Valor de clave UseInternetPorts

El valor de la clave Ports, en este ejemplo, es 5000-5100 para cada entrada.



| Application | PIA | UIP | Resultado                                  |
|-------------|-----|-----|-----------------------------------------|
| InternetApp | Y   | Y   | Usa puertos entre 5000 y 5100        |
| LocalApp    | Y   | Y   | Usa un puerto fuera del intervalo 5000-5100 |
| DefaultApp  | Y   | Y   | Usa puertos entre 5000 y 5100        |
| InternetApp | Y   | No   | Usa puertos entre 5000 y 5100        |
| LocalApp    | Y   | No   | Usa un puerto fuera del intervalo 5000-5100 |
| DefaultApp  | Y   | No   | Usa un puerto fuera del intervalo 5000-5100 |
| InternetApp | No   | Y   | Usa un puerto fuera del intervalo 5000-5100 |
| LocalApp    | No   | Y   | Usa puertos entre 5000 y 5100        |
| DefaultApp  | No   | Y   | Usa un puerto fuera del intervalo 5000-5100 |
| InternetApp | No   | No   | Usa un puerto fuera del intervalo 5000-5100 |
| LocalApp    | No   | No   | Usa puertos entre 5000 y 5100        |
| DefaultApp  | No   | No   | Usa puertos entre 5000 y 5100        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**DIRECTIVA \_ RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)
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

[**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp)
</dt> <dt>

[**ncadg \_ ip \_ udp**](/windows/desktop/Midl/ncadg-ip-udp)
</dt> </dl>

 

 
