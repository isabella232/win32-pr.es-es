---
title: Modo de transporte de detección de negociación
description: El escenario de directiva IPsec del modo de transporte de detección de negociación requiere la protección del modo de transporte IPsec para todo el tráfico entrante coincidente y solicita protección de IPsec para que coincida con el tráfico saliente.
ms.assetid: c08d9d03-7d77-43c2-8468-964b498b45f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9477d18f2fe478f5c885c071f47d0bf2baaad8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904521"
---
# <a name="negotiation-discovery-transport-mode"></a>Modo de transporte de detección de negociación

El escenario de directiva IPsec del modo de transporte de detección de negociación requiere la protección del modo de transporte IPsec para todo el tráfico entrante coincidente y solicita protección de IPsec para que coincida con el tráfico saliente. Por lo tanto, las conexiones salientes pueden retroceder a texto sin cifrar, mientras que las conexiones entrantes no.

Con esta Directiva, cuando el equipo host intenta una nueva conexión saliente y no hay ninguna SA IPsec existente que coincida con el tráfico, el host envía simultáneamente los paquetes en texto sin cifrar e inicia una negociación IKE o AuthIP. Si la negociación se realiza correctamente, la conexión se actualiza a protegido por IPsec. De lo contrario, la conexión permanece en texto no cifrado. Una vez protegida por IPsec, una conexión nunca se puede degradar a texto sin cifrar.

El modo de transporte de detección de negociación se usa normalmente en entornos que incluyen máquinas compatibles con IPsec y no compatibles con IPsec.

Un ejemplo de un posible escenario de modo de transporte de detección de negociación es "proteger todo el tráfico de datos de unidifusión, excepto ICMP, mediante el modo de transporte IPsec y habilitar la detección de negociaciones".

Para implementar este ejemplo mediante programación, utilice la siguiente configuración de WFP.

<dl>

**En la \_ capa FWPM \_ IKEEXT \_ V {4 \| 6} configuración de la Directiva de negociación mm**  

1.  Agregue uno de los siguientes contextos de proveedor de directivas MM o ambos.  
    -   Para IKE, un contexto de proveedor de directivas de tipo **FWPM \_ IPSec \_ IKE \_ mm \_ Context**.
    -   Para AuthIP, un contexto de proveedor de directivas de tipo **FWPM \_ IPSec \_ AuthIP \_ mm \_ Context**.

    > [!Note]  
    > Se negociará un módulo de creación de claves común y se aplicará la Directiva MM correspondiente. AuthIP es el módulo de creación de claves preferido si se admiten IKE y AuthIP.

     

2.  Para cada uno de los contextos agregados en el paso 1, agregue un filtro con las siguientes propiedades. 
    | Propiedad Filter        | Value                                            |
    |------------------------|--------------------------------------------------|
    | Condiciones de filtrado   | Vacía. Todo el tráfico coincidirá con el filtro.        |
    | **providerContextKey** | GUID del contexto del proveedor MM agregado en el paso 1. |

        

**En el \_ nivel de FWPM \_ IPSec \_ V {4 \| 6} configuración de la Directiva de negociación de QM y em**  

1.  Agregue uno o ambos de los siguientes contextos de proveedor de directivas del modo de transporte de QM y establezca la marca de directiva de IPSec como marca de [**\_ \_ \_ \_ seguridad segura**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .  
    -   En el caso de IKE, un contexto de proveedor de directivas de tipo FWPM \_ IPSec \_ IKE del Protocolo de \_ \_ transporte \_ .
    -   Para AuthIP, un contexto de proveedor de directivas de tipo FWPM \_ IPSec AuthIP en el \_ contexto de \_ \_ transporte \_ . Este contexto puede contener opcionalmente la Directiva de negociación de modo extendido de AuthIP (EM).

    > [!Note]  
    > Se negociará un módulo de creación de claves común y se aplicará la Directiva de QM correspondiente. AuthIP es el módulo de creación de claves preferido si se admiten IKE y AuthIP.

     

2.  Para cada uno de los contextos agregados en el paso 1, agregue un filtro con las siguientes propiedades. 
    | Propiedad Filter        | Value                                            |
    |------------------------|--------------------------------------------------|
    | Condiciones de filtrado   | Vacía. Todo el tráfico coincidirá con el filtro.        |
    | **providerContextKey** | GUID del contexto del proveedor de QM agregado en el paso 1. |

        

**En el \_ transporte de entrada de capa FWPM \_ \_ \_ V {4 \| 6} configurar reglas de filtrado por paquetes entrantes**  

1.  Agregue un filtro con las siguientes propiedades. 
    | Propiedad Filter                                                   | Value                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | **FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | **Action. Type**                                                   | **\_ \_ terminando llamada de acción de FWP \_**                                                              |
    | **Action. calloutKey**                                             | **Llamada de FWPM de \_ \_ transporte de entrada de IPSec \_ \_ \_ V {4 \| 6}**                                              |
    | **rawContext**                                                    | [**contexto de FWPM de \_ \_ \_ seguridad de \_ conexión persistente de entrada IPSec \_ \_**](filter-context-identifiers.md) |

        
2.  Excluya el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.
    | Propiedad Filter                                                   | Value                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición** | NlatUnicast                                                                |
    | **FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**             | **IPPROTO \_ ICMP {V6}** estas constantes se definen en WinSock2. h.<br/> |
    | **Action. Type**                                                   | **\_permitir acción de FWP \_**                                                    |
    | **weight**                                                        | [**\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**](filter-weight-identifiers.md)  |

        

**En \_ el transporte de salida de nivel FWPM \_ \_ \_ V {4 \| 6} configurar reglas de filtrado por paquete de salida**  

1.  Agregue un filtro con las siguientes propiedades.
    | Propiedad Filter                                                   | Value                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | **FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición** | NlatUnicast                                                                               |
    | **Action. Type**                                                   | **\_ \_ terminando llamada de acción de FWP \_**                                                     |
    | **Action. calloutKey**                                             | **Llamada de FWPM de \_ \_ transporte de salida de IPSec \_ \_ \_ V {4 \| 6}**                                    |
    | **rawContext**                                                    | [**FWPM \_ contexto de la detección de \_ \_ negociación saliente de IPSec \_ \_**](filter-context-identifiers.md) |

        
2.  Excluya el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.
    | Propiedad Filter                                                   | Value                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición** | NlatUnicast                                                                |
    | **FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**             | **IPPROTO \_ ICMP {V6}** estas constantes se definen en WinSock2. h.<br/> |
    | **Action. Type**                                                   | **\_permitir acción de FWP \_**                                                    |
    | **weight**                                                        | **\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**                                   |

        

**En el nivel FWPM, se ha \_ \_ \_ \_ aceptado la recepción de autenticación Ale de \_ \_ \| la capa**  

1.  Agregue un filtro con las siguientes propiedades. Este filtro solo permitirá intentos de conexión entrantes si están protegidos por IPsec. 
    | Propiedad Filter                                                   | Value                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | **FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición** | NlatUnicast                                                  |
    | **Action. Type**                                                   | **\_ \_ terminando llamada de acción de FWP \_**                        |
    | **Action. calloutKey**                                             | **Llamada de FWPM de \_ \_ entrada de IPSec \_ \_ iniciar \_ seguridad \_ V {4 \| 6}** |

        
2.  Excluya el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.
    | Propiedad Filter                                                   | Value                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición** | NlatUnicast                                                                |
    | **FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**             | **IPPROTO \_ ICMP {V6}** estas constantes se definen en WinSock2. h.<br/> |
    | **Action. Type**                                                   | **\_permitir acción de FWP \_**                                                    |
    | **weight**                                                        | **\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**                                   |

        

</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Código de ejemplo: uso del modo de transporte](using-transport-mode.md)
</dt> <dt>

[Niveles ALE](ale-layers.md)
</dt> <dt>

[**Identificadores de llamada integrados**](built-in-callout-identifiers.md)
</dt> <dt>

[Condiciones de filtrado](filtering-conditions.md)
</dt> <dt>

[**Filtrado de identificadores de capas**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[**\_tipo de \_ contexto de proveedor de FWPM \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

