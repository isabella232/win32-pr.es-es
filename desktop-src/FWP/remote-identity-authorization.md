---
title: Autorización de identidad remota
description: El escenario de directiva IPsec de autorización de identidad remota requiere que las conexiones entrantes provienen de un conjunto específico de entidades de seguridad remotas que se especifican en una lista de control de acceso (ACL) del descriptor de seguridad de Windows (SD).
ms.assetid: 4d9f83d6-6f56-4416-8c35-d0260f9e888c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44022c9696dec25e709d9ab1e374ada295893ed
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420563"
---
# <a name="remote-identity-authorization"></a>Autorización de identidad remota

El escenario de directiva IPsec de autorización de identidad remota requiere que las conexiones entrantes provienen de un conjunto específico de entidades de seguridad remotas que se especifican en una lista de control de acceso (ACL) del descriptor de seguridad de Windows (SD). Si la identidad remota (determinada por IPsec) no coincide con el conjunto de identidades permitidas, se quitará la conexión. Esta Directiva debe especificarse junto con una de las opciones de directiva de modo de transporte.

Si se habilita AuthIP, se pueden especificar dos descriptores de seguridad, uno correspondiente al modo principal de AuthIP y el otro correspondiente al modo extendido de AuthIP.

Un ejemplo de un posible escenario de modo de transporte de detección de negociación es "proteger todo el tráfico de datos de unidifusión, a excepción de ICMP, el uso del modo de transporte de IPsec, la habilitación de la detección de negociación y la restricción del acceso de entrada a identidades remotas permitidas según el descriptor de seguridad SD1 (que corresponde al modo principal de IKE/AuthIP) y el descriptor de seguridad SD2 (correspondiente al modo extendido de AuthIP), para todo el tráfico de unidifusión correspondiente 5555

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

1.  Agregue uno o ambos de los siguientes contextos de proveedor de directivas del modo de transporte de QM y establezca la marca de directiva de IPSec como marca de [**\_ \_ \_ \_ seguridad segura**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .  
    -   En el caso de IKE, un contexto de proveedor de directivas de tipo **FWPM \_ IPSec \_ IKE del Protocolo de \_ \_ transporte \_**.
    -   Para AuthIP, un contexto de proveedor de directivas de tipo **FWPM \_ IPSec \_ AuthIP del Protocolo de \_ transporte de QM \_ \_** que contiene la Directiva de negociación de modo extendido de AuthIP (EM).

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
    | Propiedad Filter                                                   | Value                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | **FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición** | NlatUnicast                                                            |
    | **FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**             | IPPROTO \_ ICMP {V6} estas constantes se definen en WinSock2. h.<br/> |
    | **Action. Type**                                                   | **\_permitir acción de FWP \_**                                                |
    | **weight**                                                        | **\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**                               |

        

**En la capa de FWPM, la \_ \_ \_ \_ recepción de autenticación Ale \_ acepta \_ V {4 \| 6} configuración de reglas de filtrado por conexión de entrada**  

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

        
3.  Agregue un filtro con las siguientes propiedades. Este filtro permitirá las conexiones entrantes al puerto TCP 5555 si las identidades remotas correspondientes están permitidas por SD1 y SD2. 
    | Propiedad Filter                                                   | Value                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | **FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición** | NlatUnicast                                                        |
    | **FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**             | **IPPROTO \_ TCP** esta constante se define en WinSock2. h.<br/> |
    | **FWPM \_ Condición de filtrado de \_ \_ \_ puerto local IP de condición**          | 5555                                                               |
    | **\_identificador de \_ \_ máquina remota \_ de Ale de condición FWPM \_**                     | SD1                                                                |
    | **\_ \_ \_ \_ ID. de usuario remoto \_ de la condición FWPM**                        | SD2                                                                |
    | **Action. Type**                                                   | **\_ \_ terminando llamada de acción de FWP \_**                              |
    | **Action. calloutKey**                                             | **Llamada de FWPM de \_ \_ entrada de IPSec \_ \_ iniciar \_ seguridad \_ V {4 \| 6}**       |

        
4.  Agregue un filtro con las siguientes propiedades. Este filtro bloqueará las demás conexiones entrantes al puerto TCP 5555 que no coinciden con el filtro anterior. 
    | Propiedad Filter                                                   | Value                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | **FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición** | NlatUnicast                                                        |
    | **FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**             | **IPPROTO \_ TCP** esta constante se define en WinSock2. h.<br/> |
    | **FWPM \_ Condición de filtrado de \_ \_ \_ puerto local IP de condición**          | 5555                                                               |
    | **Action. Type**                                                   | **\_bloque de acción de FWP \_**                                             |

        

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

 

