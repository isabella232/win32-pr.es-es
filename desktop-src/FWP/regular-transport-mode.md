---
title: modo de transporte
description: El escenario de directiva IPsec del modo de transporte requiere protección del modo de transporte IPsec para todo el tráfico correspondiente.
ms.assetid: 303f7cdc-fb7a-4e5c-8291-cadcb45035cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebfb6dad27340bfc72397307c58fddfe2bdf6eeadb65081faa0e1941de2c052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535895"
---
# <a name="transport-mode"></a>modo de transporte

El escenario de directiva IPsec del modo de transporte requiere protección del modo de transporte IPsec para todo el tráfico correspondiente. Cualquier tráfico de texto sin formato que coincida se descarta hasta que la negociación de IKE o AuthIP se haya completado correctamente. Si se produce un error en la negociación, la conectividad con la dirección IP correspondiente permanecerá rota.

Un ejemplo de un posible escenario de modo de transporte es "Proteger todo el tráfico de datos de unidifusión, excepto ICMP, mediante el modo de transporte IPsec".

Para implementar este ejemplo mediante programación, use la siguiente configuración de WFP.

<dl>

**En FWPM \_ LAYER \_ IXTXT \_ V{4 \| 6} setup MM negotiation policy**  

1.  Agregue uno o ambos de los siguientes contextos de proveedor de directivas MM.  
    -   Para IKE, un contexto de proveedor de directivas de tipo **FWPM \_ \_ IPSEC IKE \_ MM \_ CONTEXT**.
    -   Para AuthIP, un contexto de proveedor de directivas de tipo **FWPM \_ IPSEC \_ AUTHIP \_ MM \_ CONTEXT**.

    > [!Note]  
    > Se negociará un módulo de claves común y se aplicará la directiva MM correspondiente. AuthIP es el módulo de claves preferido si se admiten IKE y AuthIP.

     

2.  Para cada uno de los contextos agregados en el paso 1, agregue un filtro con las siguientes propiedades. 

    | Propiedad Filter        | Valor                                            |
    |------------------------|--------------------------------------------------|
    | Condiciones de filtrado   | Vacía. Todo el tráfico coincidirá con el filtro.        |
    | **providerContextKey** | GUID del contexto del proveedor mm agregado en el paso 1. |

        

**En FWPM \_ LAYER \_ IPSEC \_ V{4 \| 6} setup QM and EM negotiation policy**  

1.  Agregue uno o ambos de los siguientes contextos de proveedor de directivas de modo de transporte QM.  
    -   Para IKE, un contexto de proveedor de directivas de tipo **FWPM \_ \_ IPSEC IKE \_ QM \_ TRANSPORT \_ CONTEXT**.
    -   Para AuthIP, un contexto de proveedor de directivas de tipo **FWPM \_ IPSEC \_ AUTHIP \_ QM \_ TRANSPORT \_ CONTEXT**. Opcionalmente, este contexto puede contener la directiva de negociación AuthIP Extended Mode (EM).

    > [!Note]  
    > Se negociará un módulo de claves común y se aplicará la directiva QM correspondiente. AuthIP es el módulo de claves preferido si se admiten IKE y AuthIP.

     

2.  Para cada uno de los contextos agregados en el paso 1, agregue un filtro con las siguientes propiedades. 

    | Propiedad Filter        | Value                                            |
    |------------------------|--------------------------------------------------|
    | Condiciones de filtrado   | Vacía. Todo el tráfico coincidirá con el filtro.        |
    | **providerContextKey** | GUID del contexto del proveedor QM agregado en el paso 1. |

        

**En FWPM \_ LAYER \_ INBOUND TRANSPORT \_ \_ V{4 \| 6} configure las reglas de filtrado de entrada por paquete**  

1.  Agregue un filtro con las siguientes propiedades. 

    | Propiedad Filter                                                   | Value                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | **action.type**                                                   | TERMINACIÓN DE \_ LLAMADA \_ DE ACCIÓN \_ FWP                             |
    | **action.calloutKey**                                             | FWPM \_ CALLOUT \_ IPSEC \_ INBOUND TRANSPORT \_ \_ V{4 \| 6}             |

        
2.  Para excluir el tráfico ICMP de IPsec, agregue un filtro con las siguientes propiedades.

    | Propiedad Filter                                                  | Valor                                                                     |
    |------------------------------------------------------------------|---------------------------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                               |
    | **FWPM \_ Condición \_ de filtrado de CONDITION IP \_ PROTOCOL**            | IPPROTO \_ ICMP{V6}Estas constantes se definen en winsock2.h.<br/>    |
    | **action.type**                                                  | FWP \_ ACTION \_ PERMIT                                                       |
    | **weight**                                                       | [**EXENCIONES \_ DE \_ \_ IKE DE \_ INTERVALO DE PESO FWPM**](filter-weight-identifiers.md) |

        

**En FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6} configure las reglas de filtrado de salida por paquete**  

1.  Agregue un filtro con las siguientes propiedades.

    | Propiedad Filter                                                   | Value                                              |
    |-------------------------------------------------------------------|----------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                        |
    | **action.type**                                                   | **TERMINACIÓN DE \_ LLAMADA \_ DE ACCIÓN \_ FWP**              |
    | **action.calloutKey**                                             | FWPM \_ CALLOUT \_ IPSEC \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6} |

        
2.  Para excluir el tráfico ICMP de IPsec, agregue un filtro con las siguientes propiedades.

    | Propiedad Filter                                                   | Valor                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                            |
    | **FWPM \_ Condición \_ de filtrado de CONDITION IP \_ PROTOCOL**             | IPPROTO \_ ICMP{V6}Estas constantes se definen en winsock2.h.<br/> |
    | **action.type**                                                   | FWP \_ ACTION \_ PERMIT                                                    |
    | **weight**                                                        | EXENCIONES \_ DE \_ \_ IKE DE \_ INTERVALO DE PESO FWPM                                   |

        

</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Código de ejemplo: Uso del modo de transporte](using-transport-mode.md)
</dt> <dt>

[**Filtrado de identificadores de capa**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**Tipos de contexto de proveedor**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> <dt>

[Condiciones de filtrado](filtering-conditions.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[**Identificadores de llamada integrados**](built-in-callout-identifiers.md)
</dt> </dl>

 

