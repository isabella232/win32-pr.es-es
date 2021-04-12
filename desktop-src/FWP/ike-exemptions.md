---
title: Exenciones de IKE/AuthIP
description: Intercambio de claves por red (IKE) y protocolo de Internet autenticado (AuthIP), para poder funcionar, deben eximir el tráfico de red del filtrado IPsec.
ms.assetid: 365bfebc-250a-440f-8056-ff9601daa030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58a6d00ddd337d56c3c00a34b6949213be6ee26
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104420325"
---
# <a name="ikeauthip-exemptions"></a>Exenciones de IKE/AuthIP

Los módulos de creación de claves del Protocolo de seguridad de Internet (IPsec), Intercambio de claves por red (IKE) y protocolo de Internet autenticado (AuthIP), para que funcionen, deben eximir el tráfico de red del filtrado IPsec.

En la plataforma de filtrado de Windows (WFP), el motor de filtrado de base (BFE) agrega automáticamente filtros de exención de IKE y AuthIP cuando se agrega el primer filtro de directiva de modo principal IKE o AuthIP (MM) y los elimina cuando se elimina el último filtro de directiva IKE o AuthIP MM. De esta manera, los proveedores de directivas no tienen que administrar las exenciones de filtrado de IKE y AuthIP de forma individual.

Un filtro de directiva de IKE MM es un filtro en la capa del motor [**FWPM \_ capa \_ \_ \|**](management-filtering-layer-identifiers-.md) de la capa de la capa de la capa de la versión de tipo [**FWPM \_ IPSec \_ IKE \_ mm \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).

Un filtro de directiva de AuthIP MM es un filtro en la capa de motor FWPM de nivel de motor de la capa de sistema [**\_ \_ IKEEXT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) que hace referencia a un contexto de proveedor de tipo [**FWPM de \_ contexto de IPSec \_ AuthIP \_ mm \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).

Un filtro de exención de IKE o AuthIP es un filtro en la capa del motor [**FWPM \_ capa de transporte de \_ entrada \_ \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) o en el **transporte de salida de \_ capa FWPM \_ \_ \_ v {4 \| 6}** ponderado automáticamente en el intervalo de peso de las [**\_ \_ \_ \_ exenciones de IKE del intervalo de ponderación de FWPM**](filter-weight-identifiers.md) .

Las exenciones IKE y AuthIP implementadas por BFE son las siguientes.

| Versión de la dirección IP      | Port                        | Exención                                                                                                                                                                                                                             |
|-----------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IPv4<br/> | UDP: 500 UDP: 4500<br/> | Permita el tráfico de IKE y AuthIP en el nivel de transporte de entrada y en la capa de transporte de salida. <br/> Permita el tráfico de IKE y AuthIP en las capas de recepción y aceptación y conexión de ALE, pero restrinja el sistema local.<br/> |
| IPv6<br/> | UDP: 500<br/>          | Permita el tráfico de IKE y AuthIP en el nivel de transporte de entrada y en la capa de transporte de salida. <br/> Permita el tráfico de IKE y AuthIP en las capas de recepción y aceptación y conexión de ALE, pero restrinja el sistema local.<br/> |



 

Los filtros de exención de IKE y AuthIP están abiertos a todas las direcciones. Para implementar un firewall con un control más granular, los proveedores de directivas deben agregar filtros en un intervalo de peso superior a las [**\_ \_ \_ \_ exenciones IKE del intervalo de peso de FWPM**](filter-weight-identifiers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de IPsec](ipsec-configuration.md)
</dt> <dt>

[Asignación del peso del filtro](filter-weight-assignment.md)
</dt> </dl>

 

 





