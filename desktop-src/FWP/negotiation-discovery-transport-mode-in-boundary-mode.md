---
title: Modo de transporte de detección de negociación en modo de límite
description: El modo de transporte de detección de negociación en el escenario de directiva IPsec en modo de límite solicita la protección del modo de transporte IPsec para todo el tráfico correspondiente.
ms.assetid: 36ae74b3-30f5-49bd-8855-6f3c0fb04d70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b647f7a4ddf7b50131d6f84e09bf9fc6dce8f13a8575c6971d65be7caa7464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068865"
---
# <a name="negotiation-discovery-transport-mode-in-boundary-mode"></a>Modo de transporte de detección de negociación en modo de límite

El modo de transporte de detección de negociación en el escenario de directiva IPsec en modo de límite solicita la protección del modo de transporte IPsec para todo el tráfico correspondiente. Si se produce un error en la negociación de IKE/AuthIP, se permite que las conexiones entrantes y salientes usen la reserva para borrar texto.

Esta directiva de IPsec se usa normalmente en las máquinas a las que tienen acceso tanto las máquinas compatibles con IPsec como las que no son compatibles con IPsec.

Un ejemplo de un posible escenario de modo de transporte de detección de negociación es "Proteger todo el tráfico de datos de unidifusión, excepto ICMP, mediante el modo de transporte IPsec y habilitar la detección de negociación en modo de límite".

Para implementar este ejemplo mediante programación, use la siguiente configuración de WFP.

<dl>

**En FWPM \_ LAYER \_ IXTXT \_ V{4 \| 6} configuración de la directiva de negociación mm**  

1.  Agregue uno o ambos de los siguientes contextos de proveedor de directivas MM.  
    -   Para IKE, un contexto de proveedor de directivas de tipo FWPM \_ \_ IPSEC IKE \_ MM \_ CONTEXT.
    -   Para AuthIP, un contexto de proveedor de directivas de tipo FWPM \_ IPSEC \_ AUTHIP \_ MM \_ CONTEXT.

    > [!Note]  
    > Se negociará un módulo de claves común y se aplicará la directiva MM correspondiente. AuthIP es el módulo de claves preferido si se admiten IKE y AuthIP.

     

2.  Para cada uno de los contextos agregados en el paso 1, agregue un filtro con las siguientes propiedades.

    | Propiedad Filter        | Valor                                            |
    |------------------------|--------------------------------------------------|
    | Condiciones de filtrado   | Vacía. Todo el tráfico coincidirá con el filtro.        |
    | **providerContextKey** | GUID del contexto del proveedor mm agregado en el paso 1. |

        

**En FWPM \_ LAYER \_ IPSEC \_ V{4 6} setup QM and EM negotiation policy (Directiva de negociación de QM y EM de FWPM LAYER IPSEC V{4 \| 6} )**  

1.  Agregue uno o ambos de los siguientes contextos de proveedor de directivas de modo de transporte QM y establezca la marca [**IPSEC \_ POLICY FLAG \_ \_ ND \_ BOUNDARY.**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0)  
    -   Para IKE, un contexto de proveedor de directivas de tipo **FWPM \_ \_ IPSEC IKE \_ QM \_ TRANSPORT \_ CONTEXT**.
    -   Para AuthIP, un contexto de proveedor de directivas de tipo **FWPM \_ IPSEC \_ AUTHIP \_ QM \_ TRANSPORT \_ CONTEXT**. Opcionalmente, este contexto puede contener la directiva de negociación del modo extendido AuthIP (EM).

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
    | **action.type**                                                   | **TERMINACIÓN DE LLAMADA \_ \_ DE ACCIÓN \_ FWP**                                                              |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ INBOUND TRANSPORT \_ \_ V{4 \| 6}**                                              |
    | **rawContext**                                                    | [**FWPM \_ CONTEXT \_ IPSEC \_ INBOUND \_ PERSIST \_ CONNECTION \_ SECURITY**](filter-context-identifiers.md) |

        
2.  Excón el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.

    | Propiedad Filter                                                   | Value                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                |
    | **FWPM \_ Condición de \_ filtrado de CONDITION IP \_ PROTOCOL**             | **IPPROTO \_ ICMP{V6}** Estas constantes se definen en winsock2.h.<br/> |
    | **action.type**                                                   | PERMISO DE \_ ACCIÓN FWP \_                                                        |
    | **weight**                                                        | [**EXENCIONES DE IKE DEL INTERVALO DE PESO FWPM \_ \_ \_ \_**](filter-weight-identifiers.md)  |

        

**En FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6} configure las reglas de filtrado de salida por paquete**  

1.  Agregue un filtro con las siguientes propiedades.

    | Propiedad Filter                                                   | Value                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                               |
    | **action.type**                                                   | **TERMINACIÓN DE LLAMADA \_ \_ DE ACCIÓN \_ FWP**                                                     |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6}**                                    |
    | **rawContext**                                                    | [**DESCUCIÓN \_ DE \_ NEGOCIACIÓN SALIENTE DE IPSEC DE CONTEXTO \_ \_ FWPM \_**](filter-context-identifiers.md) |

        
2.  Excón el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.

    | Propiedad Filter                                                   | Valor                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                |
    | **FWPM \_ Condición de \_ filtrado de CONDITION IP \_ PROTOCOL**             | **IPPROTO \_ ICMP{V6}** Estas constantes se definen en winsock2.h.<br/> |
    | **action.type**                                                   | **PERMISO DE \_ ACCIÓN FWP \_**                                                    |
    | **weight**                                                        | **EXENCIONES DE IKE DEL INTERVALO DE PESO FWPM \_ \_ \_ \_**                                   |

        

</dl>

> [!Note]  
> A diferencia del modo de transporte de detección de negociación, para el modo de transporte de detección de negociación en la directiva Detección de límites no es necesario agregar un filtro en las capas **FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}** porque esta directiva permite conexiones entrantes sin texto no protegido.

 

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

[**Filtrar identificadores de capa**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[**TIPO DE CONTEXTO \_ DEL \_ PROVEEDOR \_ FWPM**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

