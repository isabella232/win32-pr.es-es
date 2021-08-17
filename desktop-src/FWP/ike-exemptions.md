---
title: Exenciones de IKE/AuthIP
description: Para poder funcionar Exchange clave de Internet (IKE) y protocolo de Internet autenticado (AuthIP), es necesario excluir el tráfico de red del filtrado de IPsec.
ms.assetid: 365bfebc-250a-440f-8056-ff9601daa030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2963c804c6bd63f191563566bcc99dcf9f0f4a74bb2c844a402adc856dbad3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069065"
---
# <a name="ikeauthip-exemptions"></a>Exenciones de IKE/AuthIP

Los módulos de claves de seguridad de protocolo de Internet (IPsec), Internet Key Exchange (IKE) y protocolo de Internet autenticado (AuthIP), para funcionar, deben excluir su tráfico de red del filtrado de IPsec.

En Windows Filtering Platform (WFP), el motor de filtrado base (BFE) agrega automáticamente filtros de exención de IKE y AuthIP cuando se agrega el primer filtro de directiva de modo principal (MM) de IKE o AuthIP y los elimina cuando se elimina el último filtro de directiva de IKE o AuthIP MM. De este modo, los proveedores de directivas no tienen que administrar las exenciones de filtrado de IKE y AuthIP individualmente.

Un filtro de directiva MM de IKE es un filtro de la capa de motor [**FWPM \_ LAYER \_ IXT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) que hace referencia a un contexto de proveedor de tipo [**FWPM \_ IPSEC \_ IKE \_ MM \_ CONTEXT**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).

Un filtro de directiva AuthIP MM es un filtro de la capa de motor [**FWPM \_ LAYER \_ IXT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) que hace referencia a un contexto de proveedor de tipo [**FWPM \_ IPSEC \_ AUTHIP \_ MM \_ CONTEXT**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).

Un filtro de exención de IKE o AuthIP es un filtro de la capa de motor [**FWPM \_ LAYER INBOUND TRANSPORT \_ \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) o **FWPM LAYER OUTBOUND TRANSPORT \_ \_ \_ \_ V{4 \| 6}** auto-weighted en el intervalo de pesoS DE [**IKE FWPM \_ WEIGHT RANGE \_ \_ IKE \_ EXEMPTIONS.**](filter-weight-identifiers.md)

Las exenciones de IKE y AuthIP implementadas por BFE son las siguientes.

| Versión de la dirección IP      | Port                        | Exención                                                                                                                                                                                                                             |
|-----------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IPv4<br/> | UDP:500 UDP:4500<br/> | Permita el tráfico IKE y AuthIP en la capa de transporte de entrada y en la capa de transporte de salida. <br/> Permita el tráfico IKE y AuthIP en las capas de recepción/aceptación y conexión de ALE, pero restrinja el tráfico al sistema local.<br/> |
| IPv6<br/> | UDP:500<br/>          | Permita el tráfico IKE y AuthIP en la capa de transporte de entrada y en la capa de transporte de salida. <br/> Permita el tráfico IKE y AuthIP en las capas de recepción/aceptación y conexión de ALE, pero restrinja el tráfico al sistema local.<br/> |



 

Los filtros de exención IKE y AuthIP están abiertos a todas las direcciones. Para implementar un firewall con un control más granular, los proveedores de directivas deben agregar filtros en un intervalo de peso superior a LAS EXENCIONES DE [**\_ \_ \_ IKE \_**](filter-weight-identifiers.md)DE FWPM WEIGHT RANGE .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de IPsec](ipsec-configuration.md)
</dt> <dt>

[Asignación del peso del filtro](filter-weight-assignment.md)
</dt> </dl>

 

 





