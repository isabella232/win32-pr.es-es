---
title: Modo de transporte de detección de negociación
description: El escenario de directiva IPsec del modo de transporte de detección de negociación requiere la protección del modo de transporte IPsec para todo el tráfico entrante que coincida y solicita protección de IPsec para buscar coincidencias con el tráfico saliente.
ms.assetid: c08d9d03-7d77-43c2-8468-964b498b45f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990a7f84e20d081933ffa0def9800ff7610a3a0e3a6d01dd3b45fe7c99729ca9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102145"
---
# <a name="negotiation-discovery-transport-mode"></a>Modo de transporte de detección de negociación

El escenario de directiva IPsec del modo de transporte de detección de negociación requiere la protección del modo de transporte IPsec para todo el tráfico entrante que coincida y solicita protección de IPsec para buscar coincidencias con el tráfico saliente. Por lo tanto, las conexiones salientes pueden realizar una reserva en texto no texto sin formato, mientras que las conexiones entrantes no lo están.

Con esta directiva, cuando el equipo host intenta una nueva conexión saliente y no hay ningún SA de IPsec existente que coincida con el tráfico, el host envía simultáneamente los paquetes en texto no cifrado e inicia una negociación IKE o AuthIP. Si la negociación se realiza correctamente, la conexión se actualiza a protegida con IPsec. De lo contrario, la conexión permanece en texto no especificado. Una vez protegida por IPsec, una conexión nunca se puede degradar a texto no cifrado.

El modo de transporte de detección de negociación se usa normalmente en entornos que incluyen máquinas compatibles con IPsec y no compatibles con IPsec.

Un ejemplo de un posible escenario de modo de transporte de detección de negociación es "Proteger todo el tráfico de datos de unidifusión, excepto ICMP, mediante el modo de transporte IPsec y habilitar la detección de negociación".

Para implementar este ejemplo mediante programación, use la siguiente configuración de WFP.

<dl>

**En FWPM \_ LAYER \_ \_ IXTXT V{4 \| 6} configure la directiva de negociación de MM.**  

1.  Agregue uno o ambos de los siguientes contextos de proveedor de directivas MM.  
    -   Para IKE, un contexto de proveedor de directivas de tipo **FWPM \_ \_ IPSEC IKE \_ MM \_ CONTEXT**.
    -   Para AuthIP, un contexto de proveedor de directivas de tipo **FWPM \_ IPSEC \_ AUTHIP \_ MM \_ CONTEXT**.

    > [!Note]  
    > Se negociará un módulo de claves común y se aplicará la directiva MM correspondiente. AuthIP es el módulo de claves preferido si se admiten IKE y AuthIP.

     

2.  Para cada uno de los contextos agregados en el paso 1, agregue un filtro con las siguientes propiedades. 

    | Propiedad Filter        | Value                                            |
    |------------------------|--------------------------------------------------|
    | Condiciones de filtrado   | Vacía. Todo el tráfico coincidirá con el filtro.        |
    | **providerContextKey** | GUID del contexto del proveedor mm agregado en el paso 1. |

        

**En FWPM \_ LAYER \_ IPSEC \_ V{4 \| 6} configure la directiva de negociación de QM y EM.**  

1.  Agregue uno o ambos de los siguientes contextos de proveedor de directivas de modo de transporte QM y establezca la marca SECURE [**\_ \_ \_ ND \_ de**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) la marca DE DIRECTIVA de IPSEC.  
    -   Para IKE, un contexto de proveedor de directivas de tipo FWPM \_ \_ IPSEC IKE \_ QM \_ TRANSPORT \_ CONTEXT.
    -   Para AuthIP, un contexto de proveedor de directivas de tipo FWPM \_ IPSEC \_ AUTHIP \_ QM \_ TRANSPORT \_ CONTEXT. Opcionalmente, este contexto puede contener la directiva de negociación AuthIP Extended Mode (EM).

    > [!Note]  
    > Se negociará un módulo de claves común y se aplicará la directiva QM correspondiente. AuthIP es el módulo de claves preferido si se admiten IKE y AuthIP.

     

2.  Para cada uno de los contextos agregados en el paso 1, agregue un filtro con las siguientes propiedades. 

    | Propiedad Filter        | Value                                            |
    |------------------------|--------------------------------------------------|
    | Condiciones de filtrado   | Vacía. Todo el tráfico coincidirá con el filtro.        |
    | **providerContextKey** | GUID del contexto del proveedor QM agregado en el paso 1. |

        

**En FWPM \_ LAYER \_ INBOUND TRANSPORT \_ \_ V{4 \| 6} configure reglas de filtrado de entrada por paquete**  

1.  Agregue un filtro con las siguientes propiedades. 

    | Propiedad Filter                                                   | Value                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | **action.type**                                                   | **TERMINACIÓN DE \_ LLAMADA \_ DE ACCIÓN \_ FWP**                                                              |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ INBOUND TRANSPORT \_ \_ V{4 \| 6}**                                              |
    | **rawContext**                                                    | [**SEGURIDAD DE CONEXIÓN \_ PERSISTENTE DE ENTRADA DE \_ IPSEC \_ \_ DE \_ \_ CONTEXTO FWPM**](filter-context-identifiers.md) |

        
2.  Exhába el tráfico ICMP de IPsec mediante la adición de un filtro con las siguientes propiedades.

    | Propiedad Filter                                                   | Value                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                |
    | **FWPM \_ Condición \_ de filtrado de CONDITION IP \_ PROTOCOL**             | **IPPROTO \_ ICMP{V6}** Estas constantes se definen en winsock2.h.<br/> |
    | **action.type**                                                   | **FWP \_ ACTION \_ PERMIT**                                                    |
    | **weight**                                                        | [**EXENCIONES \_ DE \_ \_ IKE DE \_ INTERVALO DE PESO FWPM**](filter-weight-identifiers.md)  |

        

**En FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6} configure reglas de filtrado de salida por paquete**  

1.  Agregue un filtro con las siguientes propiedades.

    | Propiedad Filter                                                   | Value                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                               |
    | **action.type**                                                   | **TERMINACIÓN DE \_ LLAMADA \_ DE ACCIÓN \_ FWP**                                                     |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6}**                                    |
    | **rawContext**                                                    | [**DESCUCIÓN DE \_ \_ NEGOCIACIÓN SALIENTE DE IPSEC \_ DE CONTEXTO \_ FWPM \_**](filter-context-identifiers.md) |

        
2.  Exhába el tráfico ICMP de IPsec mediante la adición de un filtro con las siguientes propiedades.

    | Propiedad Filter                                                   | Value                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                |
    | **FWPM \_ Condición \_ de filtrado de CONDITION IP \_ PROTOCOL**             | **IPPROTO \_ ICMP{V6}** Estas constantes se definen en winsock2.h.<br/> |
    | **action.type**                                                   | **FWP \_ ACTION \_ PERMIT**                                                    |
    | **weight**                                                        | **EXENCIONES \_ DE \_ \_ IKE DE \_ INTERVALO DE PESO FWPM**                                   |

        

**En FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6} configure reglas de filtrado de entrada por conexión**  

1.  Agregue un filtro con las siguientes propiedades. Este filtro solo permitirá los intentos de conexión entrantes si están protegidos por IPsec. 

    | Propiedad Filter                                                   | Value                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                  |
    | **action.type**                                                   | **TERMINACIÓN DE \_ LLAMADA \_ DE ACCIÓN \_ FWP**                        |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ INBOUND INITIATE SECURE \_ \_ \_ V{4 \| 6}** |

        
2.  Exhába el tráfico ICMP de IPsec mediante la adición de un filtro con las siguientes propiedades.

    | Propiedad Filter                                                   | Value                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                |
    | **FWPM \_ Condición \_ de filtrado de CONDITION IP \_ PROTOCOL**             | **IPPROTO \_ ICMP{V6}** Estas constantes se definen en winsock2.h.<br/> |
    | **action.type**                                                   | **FWP \_ ACTION \_ PERMIT**                                                    |
    | **weight**                                                        | **EXENCIONES \_ DE \_ \_ IKE DE \_ INTERVALO DE PESO FWPM**                                   |

        

</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Código de ejemplo: Uso del modo de transporte](using-transport-mode.md)
</dt> <dt>

[Capas de ALE](ale-layers.md)
</dt> <dt>

[**Identificadores de llamada integrados**](built-in-callout-identifiers.md)
</dt> <dt>

[Condiciones de filtrado](filtering-conditions.md)
</dt> <dt>

[**Filtrado de identificadores de capa**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[**TIPO DE CONTEXTO \_ DEL \_ PROVEEDOR \_ FWPM**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

