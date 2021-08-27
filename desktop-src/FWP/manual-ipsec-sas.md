---
title: Manual SA
description: El escenario de directiva IPsec de asociación de seguridad manual (SA) permite a los autores de la llamada omitir los módulos de clave IPsec integrados (IKE y AuthIP) especificando directamente las SA de IPsec para proteger cualquier tráfico de red.
ms.assetid: 2bcc0b40-ca43-43c6-b1e4-b64426ef7ff4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cdb3d7c67d9cfa513cbdff846c02fd6ba61ebf031672fb86887bc01c90455b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083325"
---
# <a name="manual-sa"></a>Manual SA

El escenario de directiva IPsec de asociación de seguridad manual (SA) permite a los autores de la llamada omitir los módulos de clave IPsec integrados (IKE y AuthIP) especificando directamente las SA de IPsec para proteger cualquier tráfico de red.

Un ejemplo de un posible escenario de SA manual es "Add an IPsec SA pair to secure all uncast data traffic between IP addresses 1.1.1.1 & 2.2.2.2, except ICMP, using IPsec transport mode".

> [!Note]  
> Los pasos siguientes se deben ejecutar en ambas máquinas con las direcciones IP establecidas correctamente.

 

Para implementar este ejemplo mediante programación, use la siguiente configuración de WFP.

<dl>

**En FWPM \_ LAYER \_ INBOUND TRANSPORT \_ \_ V{4 \| 6} configure reglas de filtrado de entrada por paquete**  

1.  Agregue un filtro con las siguientes propiedades. 

    | Propiedad Filter                                                   | Value                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | **DIRECCIÓN LOCAL \_ DE IP DE CONDICIÓN \_ \_ \_ FWPM**                           | Dirección local adecuada (1.1.1.1 o 2.2.2.2).           |
    | **DIRECCIÓN REMOTA \_ IP DE CONDICIÓN \_ \_ \_ FWPM**                          | Dirección remota adecuada (1.1.1.1 o 2.2.2.2).          |
    | **action.type**                                                   | **TERMINACIÓN DE LLAMADA \_ \_ DE ACCIÓN \_ FWP**                         |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ INBOUND TRANSPORT \_ \_ V{4 \| 6}**         |

        
2.  Excón el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades. 

    | Propiedad Filter                                                   | Value                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                |
    | **FWPM \_ Condición de \_ filtrado de CONDITION IP \_ PROTOCOL**             | **IPPROTO \_ ICMP{V6}** Estas constantes se definen en winsock2.h.<br/> |
    | **action.type**                                                   | **PERMISO DE \_ ACCIÓN FWP \_**                                                    |
    | **weight**                                                        | [**EXENCIONES DE IKE DEL INTERVALO DE PESO FWPM \_ \_ \_ \_**](filter-weight-identifiers.md)  |

        

**En FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6} configure las reglas de filtrado de salida por paquete**  

1.  Agregue un filtro con las siguientes propiedades. 

    | Propiedad Filter                                                   | Value                                                  |
    |-------------------------------------------------------------------|--------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                            |
    | **FWPM \_ Condición de \_ filtrado DE DIRECCIÓN LOCAL \_ \_ DE IP** DE CONDICIÓN       | Dirección local adecuada (1.1.1.1 o 2.2.2.2).    |
    | **FWPM \_ Condición de \_ filtrado DE DIRECCIÓN REMOTA \_ \_ DE IP** DE CONDICIÓN      | Dirección remota adecuada (1.1.1.1 o 2.2.2.2).   |
    | **action.type**                                                   | **TERMINACIÓN DE LLAMADA \_ \_ DE ACCIÓN \_ FWP**                  |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6}** |

        
2.  Excón el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades. 

    | Propiedad Filter                                                   | Value                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                |
    | **FWPM \_ Condición de \_ filtrado de CONDITION IP \_ PROTOCOL**             | **IPPROTO \_ ICMP{V6}** Estas constantes se definen en winsock2.h.<br/> |
    | **action.type**                                                   | **PERMISO DE \_ ACCIÓN FWP \_**                                                    |
    | **weight**                                                        | **EXENCIONES DE IKE DEL INTERVALO DE PESO FWPM \_ \_ \_ \_**                                   |

        

**Configuración de asociaciones de seguridad entrantes y salientes**

1.  Llame [**a IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), con el parámetro *outboundTraffic* que contiene las direcciones IP como 1.1.1.1 & 2.2.2.2 e **ipsecFilterId** como el LUID del filtro de llamada IPsec de la capa de transporte saliente agregado anteriormente.
2.  Llame a [**IPsecSaContextGetSpi0,**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)con el parámetro *id* que contiene el identificador de contexto devuelto de [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)y el parámetro *getSpi* que contiene las direcciones IP como 1.1.1.1 & 2.2.2.2 e **ipsecFilterId** como el LUID del filtro de llamada IPsec de la capa de transporte entrante agregado anteriormente. El valor SPI devuelto está pensado para ser utilizado como SPI de SA entrante por la máquina local y como SPI de SA saliente por la máquina remota correspondiente. Ambas máquinas deben usar algún medio fuera de banda para intercambiar los valores SPI.
3.  Llame a [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0), con el parámetro *id* que contiene el identificador de contexto devuelto de [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)y el parámetro *inboundBundle* que describe las propiedades del paquete sa de entrada (por ejemplo, el SPI de SA entrante, el tipo de transformación, los tipos de algoritmo, las claves, etc.).
4.  Llame a [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0), con el parámetro *id* que contiene el identificador de contexto devuelto por [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)y el parámetro *outboundBundle* que describe las propiedades del paquete sa de salida (por ejemplo, el SPI de SA saliente, el tipo de transformación, los tipos de algoritmo, las claves, etc.).

  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Código de ejemplo: Manual SA Keying](manual-sa-keying.md)
</dt> <dt>

[**Identificadores de llamada integrados**](built-in-callout-identifiers.md)
</dt> <dt>

[**Filtrar identificadores de capa**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> </dl>

 

