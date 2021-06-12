---
title: Administración de registros de recursos DNS
description: Obtenga información sobre la administración de registros de recursos. Un registro de recursos es la unidad de entrada de información en los archivos de zona DNS, que se usa para resolver todas las consultas DNS.
ms.assetid: ddad5f14-5a2d-4966-87b7-b354666f9e24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6c818899414cc541a1c89bfd11747051b2f5f1
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011118"
---
# <a name="managing-dns-resource-records"></a>Administración de registros de recursos DNS

Un registro de recursos, conocido normalmente como RR, es la unidad de entrada de información en los archivos de zona DNS. Los RR son los bloques de creación básicos de la información ip y el nombre de host y se usan para resolver todas las consultas DNS. Los registros de recursos tienen una amplia variedad de tipos para proporcionar servicios extendidos de resolución de nombres.

Los distintos tipos de RR tienen formatos diferentes, ya que contienen datos diferentes. Muchas RR comparten un formato común. Cada servidor DNS contiene RR para la parte del espacio de nombres para el que es autoritativo.

El proveedor WMI de DNS admite actualmente los siguientes tipos RR. Haga clic en el nombre del registro de recursos para saltar a su página de referencia.



| Registro de recursos (en el proveedor)                             | Descripción                                                  |
|-----------------------------------------------------------|--------------------------------------------------------------|
| [**MicrosoftDNS \_ AType**](microsoftdns-atype.md)         | Registro de asignación de nombre a dirección                               |
| [**MicrosoftDNS \_ AAAAType**](microsoftdns-aaaatype.md)   | Hospedar en el registro de direcciones Ipv6                                  |
| [**MicrosoftDNS \_ AFSDBType**](microsoftdns-afsdbtype.md) | Registro del servidor de bases de datos del sistema de archivos Andrew                    |
| [**MicrosoftDNS \_ ATMAType**](microsoftdns-atmatype.md)   | Registro de dirección a nombre de ATM                                   |
| [**MicrosoftDNS \_ CNAMEType**](microsoftdns-cnametype.md) | [*Registro de nombre canónico*](c-gly.md) |
| [**MicrosoftDNS \_ HINFOType**](microsoftdns-hinfotype.md) | Registro de información de host                                      |
| [**MicrosoftDNS \_ ISDNType**](microsoftdns-isdntype.md)   | Registro de red digital de servicios integrados                   |
| [**MicrosoftDNS \_ KEYType**](microsoftdns-keytype.md)     | Registro KEY. Consulte RFC 2535                                     |
| [**MbType de MicrosoftDNS \_**](microsoftdns-mbtype.md)       | Registro de buzón                                               |
| [**MicrosoftDNS \_ MDType**](microsoftdns-mdtype.md)       | Agente de correo para el registro de dominio                             |
| [**MicrosoftDNS \_ MFType**](microsoftdns-mftype.md)       | Agente de reenvío de correo para el registro de dominio                  |
| [**MgType de MicrosoftDNS \_**](microsoftdns-mgtype.md)       | Registro de grupo de correo                                            |
| [**MicrosoftDNS \_ MINFOType**](microsoftdns-minfotype.md) | Registro de información de correo                                      |
| [**MicrosoftDNS \_ MRType**](microsoftdns-mrtype.md)       | Registro de cambio de nombre de buzón                                        |
| [**MxType de MicrosoftDNS \_**](microsoftdns-mxtype.md)       | Registro de exchanger de correo                                        |
| [**MicrosoftDNS \_ NSType**](microsoftdns-nstype.md)       | Registro de servidor DNS                                           |
| [**MicrosoftDNS \_ NXTType**](microsoftdns-nxttype.md)     | Siguiente registro                                                  |
| [**MicrosoftDNS \_ PTRType**](microsoftdns-ptrtype.md)     | Registro de asignación de dirección a nombre                               |
| [**RpType de MicrosoftDNS \_**](microsoftdns-rptype.md)       | Registro de persona responsable                                    |
| [**MicrosoftDNS \_ RTType**](microsoftdns-rttype.md)       | Enrutar a través del registro                                         |
| [**SigType de MicrosoftDNS \_**](microsoftdns-sigtype.md)     | Registro de firma                                             |
| [**MicrosoftDNS \_ SOAType**](microsoftdns-soatype.md)     | Inicio de la autoridad                                           |
| [**MicrosoftDNS \_ SRVType**](microsoftdns-srvtype.md)     | Registro de servicio                                               |
| [**MicrosoftDNS \_ TXTType**](microsoftdns-txttype.md)     | Registro de texto                                                  |
| [**MicrosoftDNS \_ WINSType**](microsoftdns-winstype.md)   | Registro de servidor WINS                                           |
| [**MicrosoftDNS \_ WINSRType**](microsoftdns-winsrtype.md) | Registro de búsqueda inversa WINS                                   |
| [**MicrosoftDNS \_ WKSType**](microsoftdns-wkstype.md)     | Registro de servicios conocidos                                   |
| [**MicrosoftDNS \_ X25Type**](microsoftdns-x25type.md)     | Registro de asignación de dirección a nombre X.121                         |



 

## <a name="administration-steps"></a>Pasos de administración

El proveedor WMI de DNS permite la administración de RR desde el propio servidor o desde hosts remotos. Los pasos generales necesarios para administrar RR mediante el proveedor WMI de DNS son:

-   Conexión al proveedor WMI de DNS
-   Obtención de una instancia de registro de recursos
-   Enumeración o modificación de una propiedad de registro de recursos o mediante un método

Las tareas siguientes están vinculadas a sus ejemplos de scripting asociados.

-   [Enumeración de tipos de recursos](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Agregar un registro de recursos](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Eliminación de un registro de recursos](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Modificar un registro de recursos](dns-wmi-provider-samples-managing-dns-resource-records.md)

 

 




