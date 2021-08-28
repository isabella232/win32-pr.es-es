---
title: Administración de registros de recursos DNS
description: Obtenga información sobre la administración de registros de recursos. Un registro de recursos es la unidad de entrada de información en los archivos de zona DNS, que se usa para resolver todas las consultas DNS.
ms.assetid: ddad5f14-5a2d-4966-87b7-b354666f9e24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61aa9e5c6711d0db763691beafdf8b49a4c3c3e670964e5345b753f91592f826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692985"
---
# <a name="managing-dns-resource-records"></a>Administración de registros de recursos DNS

Un registro de recursos, conocido normalmente como RR, es la unidad de entrada de información en los archivos de zona DNS. Las RR son los bloques de creación básicos de la información ip y el nombre de host y se usan para resolver todas las consultas DNS. Los registros de recursos tienen una variedad bastante amplia de tipos para proporcionar servicios extendidos de resolución de nombres.

Los distintos tipos de RR tienen formatos diferentes, ya que contienen datos diferentes. Muchas RR comparten un formato común. Cada servidor DNS contiene RR para la parte del espacio de nombres para el que es autoritativo.

El proveedor WMI de DNS admite actualmente los siguientes tipos RR. Haga clic en el nombre del registro de recursos para ir a su página de referencia.



| Registro de recursos (en proveedor)                             | Descripción                                                  |
|-----------------------------------------------------------|--------------------------------------------------------------|
| [**MicrosoftDNS \_ AType**](microsoftdns-atype.md)         | Nombre para el registro de asignación de direcciones                               |
| [**MicrosoftDNS \_ AAAAType**](microsoftdns-aaaatype.md)   | Registro de dirección de host a Ipv6                                  |
| [**MicrosoftDNS \_ AFSDBType**](microsoftdns-afsdbtype.md) | Registro del servidor de base de datos del sistema de archivos Andrew                    |
| [**MicrosoftDNS \_ ATMAType**](microsoftdns-atmatype.md)   | Registro de dirección a nombre de ATM                                   |
| [**MicrosoftDNS \_ CNAMEType**](microsoftdns-cnametype.md) | [*Registro de nombre*](c-gly.md) canónico |
| [**MicrosoftDNS \_ HINFOType**](microsoftdns-hinfotype.md) | Registro de información de host                                      |
| [**MicrosoftDNS \_ ISDNType**](microsoftdns-isdntype.md)   | Registro de red digital de servicios integrados                   |
| [**MicrosoftDNS \_ KEYType**](microsoftdns-keytype.md)     | Registro KEY. Consulte RFC 2535.                                     |
| [**MicrosoftDNS \_ MBType**](microsoftdns-mbtype.md)       | Registro de buzón de correo                                               |
| [**MicrosoftDNS \_ MDType**](microsoftdns-mdtype.md)       | Agente de correo para el registro de dominio                             |
| [**MicrosoftDNS \_ MFType**](microsoftdns-mftype.md)       | Agente de reenvío de correo para el registro de dominio                  |
| [**MicrosoftDNS \_ MGType**](microsoftdns-mgtype.md)       | Registro de grupo de correo                                            |
| [**MicrosoftDNS \_ MINFOType**](microsoftdns-minfotype.md) | Registro de información de correo electrónico                                      |
| [**MicrosoftDNS \_ MRType**](microsoftdns-mrtype.md)       | Registro de cambio de nombre de buzón                                        |
| [**MicrosoftDNS \_ MXType**](microsoftdns-mxtype.md)       | Registro de exchanger de correo                                        |
| [**MicrosoftDNS \_ NSType**](microsoftdns-nstype.md)       | Registro de servidor DNS                                           |
| [**MicrosoftDNS \_ NXTType**](microsoftdns-nxttype.md)     | Siguiente registro                                                  |
| [**MicrosoftDNS \_ PTRType**](microsoftdns-ptrtype.md)     | Dirección al registro de asignación de nombres                               |
| [**RpType de MicrosoftDNS \_**](microsoftdns-rptype.md)       | Registro de persona responsable                                    |
| [**MicrosoftDNS \_ RTType**](microsoftdns-rttype.md)       | Enrutar a través del registro                                         |
| [**MicrosoftDNS \_ SIGType**](microsoftdns-sigtype.md)     | Registro de firma                                             |
| [**MicrosoftDNS \_ SOAType**](microsoftdns-soatype.md)     | Inicio de autoridad                                           |
| [**MicrosoftDNS \_ SRVType**](microsoftdns-srvtype.md)     | Registro de servicio                                               |
| [**MicrosoftDNS \_ TXTType**](microsoftdns-txttype.md)     | Registro de texto                                                  |
| [**MicrosoftDNS \_ WINSType**](microsoftdns-winstype.md)   | Registro de servidor WINS                                           |
| [**MicrosoftDNS \_ WINSRType**](microsoftdns-winsrtype.md) | Registro de búsqueda inversa WINS                                   |
| [**MicrosoftDNS \_ WKSType**](microsoftdns-wkstype.md)     | Registro de servicios conocidos                                   |
| [**MicrosoftDNS \_ X25Type**](microsoftdns-x25type.md)     | Registro de asignación de dirección a nombre de X.121                         |



 

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

 

 




