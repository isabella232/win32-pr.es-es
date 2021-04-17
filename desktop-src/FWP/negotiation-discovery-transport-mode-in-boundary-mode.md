---
title: Modo de transporte de detección de negociación en modo de límite
description: El escenario de transporte de detección de negociación en modo de límite Directiva de IPsec solicita la protección del modo de transporte de IPsec para todo el tráfico coincidente.
ms.assetid: 36ae74b3-30f5-49bd-8855-6f3c0fb04d70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9f4168eee38165125c2455bc80dae29c1c6794
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487703"
---
# <a name="negotiation-discovery-transport-mode-in-boundary-mode"></a>Modo de transporte de detección de negociación en modo de límite

El escenario de transporte de detección de negociación en modo de límite Directiva de IPsec solicita la protección del modo de transporte de IPsec para todo el tráfico coincidente. Si se produce un error en la negociación de IKE/AuthIP, se permite que las conexiones entrantes y salientes se reproduzcan en texto sin cifrar.

Esta directiva IPsec se usa normalmente en equipos a los que se tiene acceso mediante máquinas con capacidad IPsec y no compatibles con IPsec.

Un ejemplo de un posible escenario de modo de transporte de detección de negociación es "proteger todo el tráfico de datos de unidifusión, excepto ICMP, mediante el modo de transporte de IPsec y habilitar la detección de negociación en el modo límite".

Para implementar este ejemplo mediante programación, utilice la siguiente configuración de WFP.

<dl>

**En la \_ capa FWPM \_ IKEEXT \_ V {4 \| 6} Directiva de negociación del programa de instalación**  

1.  Agregue uno de los siguientes contextos de proveedor de directivas MM o ambos.  
    -   Para IKE, un contexto de proveedor de directivas de tipo FWPM \_ IPSec \_ IKE \_ mm \_ context.
    -   Para AuthIP, un contexto de proveedor de directivas de tipo FWPM \_ IPSec \_ AuthIP \_ mm \_ context.

    > [!Note]  
    > Se negociará un módulo de creación de claves común y se aplicará la Directiva MM correspondiente. AuthIP es el módulo de creación de claves preferido si se admiten IKE y AuthIP.

     

2.  Para cada uno de los contextos agregados en el paso 1, agregue un filtro con las siguientes propiedades.
    | Propiedad Filter        | Value                                            |
    |------------------------|--------------------------------------------------|
    | Condiciones de filtrado   | Vacía. Todo el tráfico coincidirá con el filtro.        |
    | **providerContextKey** | GUID del contexto del proveedor MM agregado en el paso 1. |

        

**En la \_ capa de FWPM \_ IPSec \_ V {4 \| 6} configuración de la Directiva de negociación de QM y em**  

1.  Agregue uno o ambos de los siguientes contextos de proveedor de directivas del modo de transporte de QM y establezca la marca de límite de la [**\_ marca de directiva \_ \_ \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .  
    -   En el caso de IKE, un contexto de proveedor de directivas de tipo **FWPM \_ IPSec \_ IKE del Protocolo de \_ \_ transporte \_**.
    -   Para AuthIP, un contexto de proveedor de directivas de tipo **FWPM \_ IPSec AuthIP en el \_ \_ \_ \_ contexto de transporte**. Este contexto puede contener opcionalmente la Directiva de negociación de modo extendido de AuthIP (EM).

    > [!Note]  
    > Se negociará un módulo de creación de claves común y se aplicará la Directiva de QM correspondiente. AuthIP es el módulo de creación de claves preferido si se admiten IKE y AuthIP.

     

2.  Para cada uno de los contextos agregados en el paso 1, agregue un filtro con las siguientes propiedades.
    | Propiedad Filter        | Value                                            |
    |------------------------|--------------------------------------------------|
    | Condiciones de filtrado   | Vacía. Todo el tráfico coincidirá con el filtro.        |
    | **providerContextKey** | GUID del contexto del proveedor de QM agregado en el paso 1. |

        

**En el nivel de FWPM de \_ \_ transporte de entrada \_ \_ V {4 \| 6} configuración de reglas de filtrado por paquete de entrada**  

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
    | **Action. Type**                                                   | \_permitir acción de FWP \_                                                        |
    | **weight**                                                        | [**\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**](filter-weight-identifiers.md)  |

        

**En el nivel de FWPM de \_ \_ transporte de salida \_ \_ V {4 \| 6} configuración de reglas de filtrado por paquetes salientes**  

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

        

</dl>

> [!Note]  
> En lugar del modo de transporte de detección de negociación, para el modo de transporte de detección de negociación en la Directiva de modo límite, no es necesario agregar un filtro en las capas de FWPM de autenticación Ale de la capa de la **\_ recepción de \_ \_ \_ \_ aceptación \_ V {4 \| 6}** porque esta directiva permite conexiones entrantes sin protección de texto no protegido.

 

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

 

