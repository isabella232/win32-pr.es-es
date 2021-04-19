---
title: modo de transporte
description: El escenario de la directiva IPsec del modo de transporte requiere protección del modo de transporte IPsec para todo el tráfico coincidente.
ms.assetid: 303f7cdc-fb7a-4e5c-8291-cadcb45035cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8335854c80850e44b860530bbebab05aa3f14273
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314938"
---
# <a name="transport-mode"></a>modo de transporte

El escenario de la directiva IPsec del modo de transporte requiere protección del modo de transporte IPsec para todo el tráfico coincidente. Cualquier tráfico de texto no cifrado coincidente se quita hasta que la negociación IKE o AuthIP se ha completado correctamente. Si se produce un error en la negociación, la conectividad con la dirección IP correspondiente permanecerá rota.

Un ejemplo de posible escenario de modo de transporte es "proteger todo el tráfico de datos de unidifusión, excepto ICMP, mediante el modo de transporte de IPsec".

Para implementar este ejemplo mediante programación, utilice la siguiente configuración de WFP.

<dl>

**En la \_ capa FWPM \_ IKEEXT \_ V {4 \| 6} Directiva de negociación del programa de instalación**  

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

        

**En la \_ capa de FWPM \_ IPSec \_ V {4 \| 6} configuración de la Directiva de negociación de QM y em**  

1.  Agregue uno o ambos de los siguientes contextos de proveedor de directivas de modo de transporte de QM.  
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

    | Propiedad Filter                                                   | Value                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | **FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | **Action. Type**                                                   | \_ \_ terminando llamada de acción de FWP \_                             |
    | **Action. calloutKey**                                             | Llamada de FWPM de \_ \_ transporte de entrada de IPSec \_ \_ \_ V {4 \| 6}             |

        
2.  Excluya el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.

    | Propiedad Filter                                                  | Value                                                                     |
    |------------------------------------------------------------------|---------------------------------------------------------------------------|
    | **FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición** | NlatUnicast                                                               |
    | **FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**            | IPPROTO \_ ICMP {V6} estas constantes se definen en WinSock2. h.<br/>    |
    | **Action. Type**                                                  | \_permitir acción de FWP \_                                                       |
    | **weight**                                                       | [**\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**](filter-weight-identifiers.md) |

        

**En el nivel de FWPM de \_ \_ transporte de salida \_ \_ V {4 \| 6} configuración de reglas de filtrado por paquetes salientes**  

1.  Agregue un filtro con las siguientes propiedades.

    | Propiedad Filter                                                   | Value                                              |
    |-------------------------------------------------------------------|----------------------------------------------------|
    | **FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición** | NlatUnicast                                        |
    | **Action. Type**                                                   | **\_ \_ terminando llamada de acción de FWP \_**              |
    | **Action. calloutKey**                                             | Llamada de FWPM de \_ \_ transporte de salida de IPSec \_ \_ \_ V {4 \| 6} |

        
2.  Excluya el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.

    | Propiedad Filter                                                   | Value                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | **FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición** | NlatUnicast                                                            |
    | **FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**             | IPPROTO \_ ICMP {V6} estas constantes se definen en WinSock2. h.<br/> |
    | **Action. Type**                                                   | \_permitir acción de FWP \_                                                    |
    | **weight**                                                        | \_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_                                   |

        

</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Código de ejemplo: uso del modo de transporte](using-transport-mode.md)
</dt> <dt>

[**Filtrado de identificadores de capas**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**Tipos de contexto de proveedor**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> <dt>

[Condiciones de filtrado](filtering-conditions.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[**Identificadores de llamada integrados**](built-in-callout-identifiers.md)
</dt> </dl>

 

