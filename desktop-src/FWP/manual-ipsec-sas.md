---
title: SA manual
description: El escenario de la directiva IPsec de la Asociación de seguridad manual (SA) permite que los autores de llamadas omitan los módulos de creación de claves IPsec integrados (IKE y AuthIP) especificando directamente las SA de IPsec para proteger el tráfico de red.
ms.assetid: 2bcc0b40-ca43-43c6-b1e4-b64426ef7ff4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161447ff5cfd98878ab4ee0f4b18cbcc3a53643
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995159"
---
# <a name="manual-sa"></a>SA manual

El escenario de la directiva IPsec de la Asociación de seguridad manual (SA) permite que los autores de llamadas omitan los módulos de creación de claves IPsec integrados (IKE y AuthIP) especificando directamente las SA de IPsec para proteger el tráfico de red.

Un ejemplo de un posible escenario de SA manual es "agregar un par de SA de IPsec para proteger todo el tráfico de datos de unidifusión entre & las direcciones IP de la 2.2.2.2, a excepción de ICMP, mediante el modo de transporte IPsec".

> [!Note]  
> Los siguientes pasos deben ejecutarse en ambos equipos con direcciones IP establecidas correctamente.

 

Para implementar este ejemplo mediante programación, utilice la siguiente configuración de WFP.

<dl>

**En el nivel de FWPM de \_ \_ transporte de entrada \_ \_ V {4 \| 6} configuración de reglas de filtrado por paquete de entrada**  

1.  Agregue un filtro con las siguientes propiedades. 
    | Propiedad Filter                                                   | Value                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | **FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | **\_ \_ \_ dirección local IP de condición FWPM \_**                           | La dirección local adecuada (2.2.2.2).           |
    | **\_ \_ \_ dirección remota IP de condición FWPM \_**                          | La dirección remota adecuada (2.2.2.2).          |
    | **Action. Type**                                                   | **\_ \_ terminando llamada de acción de FWP \_**                         |
    | **Action. calloutKey**                                             | **Llamada de FWPM de \_ \_ transporte de entrada de IPSec \_ \_ \_ V {4 \| 6}**         |

        
2.  Excluya el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades. 
    | Propiedad Filter                                                   | Value                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición** | NlatUnicast                                                                |
    | **FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**             | **IPPROTO \_ ICMP {V6}** estas constantes se definen en WinSock2. h.<br/> |
    | **Action. Type**                                                   | **\_permitir acción de FWP \_**                                                    |
    | **weight**                                                        | [**\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**](filter-weight-identifiers.md)  |

        

**En el nivel de FWPM de \_ \_ transporte de salida \_ \_ V {4 \| 6} configuración de reglas de filtrado por paquetes salientes**  

1.  Agregue un filtro con las siguientes propiedades. 
    | Propiedad Filter                                                   | Value                                                  |
    |-------------------------------------------------------------------|--------------------------------------------------------|
    | **FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición** | NlatUnicast                                            |
    | **FWPM \_ Condición de filtrado de \_ \_ \_ dirección local IP de condición**       | La dirección local adecuada (2.2.2.2).    |
    | **FWPM \_ Condición de filtrado de \_ \_ \_ direcciones remotas IP de condición**      | La dirección remota adecuada (2.2.2.2).   |
    | **Action. Type**                                                   | **\_ \_ terminando llamada de acción de FWP \_**                  |
    | **Action. calloutKey**                                             | **Llamada de FWPM de \_ \_ transporte de salida de IPSec \_ \_ \_ V {4 \| 6}** |

        
2.  Excluya el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades. 
    | Propiedad Filter                                                   | Value                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición** | NlatUnicast                                                                |
    | **FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**             | **IPPROTO \_ ICMP {V6}** estas constantes se definen en WinSock2. h.<br/> |
    | **Action. Type**                                                   | **\_permitir acción de FWP \_**                                                    |
    | **weight**                                                        | **\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**                                   |

        

**Configuración de asociaciones de seguridad entrantes y salientes**

1.  Llame a [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), con el parámetro *outboundTraffic* que contiene las direcciones IP como a la vez & 2.2.2.2 y **ipsecFilterId** como LUID del filtro de llamada IPSec de la capa de transporte saliente agregada anteriormente.
2.  Llame a [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0), con el parámetro *ID* que contiene el ID. de contexto devuelto desde [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), y el parámetro *getSpi* que contiene las direcciones IP como el valor de la enumeración & 2.2.2.2 y **ipsecFilterId** como LUID del filtro de llamada IPSec de la capa de transporte de entrada agregada anteriormente. El valor de SPI devuelto está pensado para que lo use el equipo local y como el SPI de la SA de salida en el equipo remoto correspondiente. Ambos equipos deben usar algunos medios fuera de banda para intercambiar los valores de SPI.
3.  Llame a [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0), con el parámetro *ID* que contiene el identificador de contexto devuelto desde [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), y el parámetro *INBOUNDBUNDLE* que describe las propiedades del paquete SA entrante (por ejemplo, el SPI de SA entrante, el tipo de transformación, los tipos de algoritmo, las claves, etc.).
4.  Llame a [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0), con el parámetro *ID* que contiene el ID. de contexto devuelto desde [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), y el parámetro *OUTBOUNDBUNDLE* que describe las propiedades del paquete SA saliente (como el IRP de salida SA, el tipo de transformación, los tipos de algoritmo, las claves, etc.).

  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Código de ejemplo: creación manual de claves SA](manual-sa-keying.md)
</dt> <dt>

[**Identificadores de llamada integrados**](built-in-callout-identifiers.md)
</dt> <dt>

[**Filtrado de identificadores de capas**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> </dl>

 

