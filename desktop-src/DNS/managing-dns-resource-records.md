---
title: Administración de registros de recursos DNS
description: Un registro de recursos, que normalmente se conoce como un RR, es la unidad de la entrada de información en archivos de zona DNS. Los RRs son los bloques de creación básicos de la información del nombre del host y de la dirección IP, y se usan para resolver todas las consultas DNS.
ms.assetid: ddad5f14-5a2d-4966-87b7-b354666f9e24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99edffa52b5137858468fd64122d2af826a896ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903662"
---
# <a name="managing-dns-resource-records"></a>Administración de registros de recursos DNS

Un registro de recursos, que normalmente se conoce como un RR, es la unidad de la entrada de información en archivos de zona DNS. Los RRs son los bloques de creación básicos de la información del nombre del host y de la dirección IP, y se usan para resolver todas las consultas DNS. Los registros de recursos se incluyen en una variedad bastante extensa de tipos para proporcionar servicios extendidos de resolución de nombres.

Los distintos tipos de RRs tienen formatos diferentes, ya que contienen datos diferentes. Muchos RRs comparten un formato común. Cada servidor DNS contiene RRs para la parte del espacio de nombres para el que es autoritativo.

El proveedor WMI de DNS admite actualmente los siguientes tipos de RR. Haga clic en el nombre del registro de recursos para saltar a su página de referencia.



| Registro de recursos (en el proveedor)                             | Descripción                                                  |
|-----------------------------------------------------------|--------------------------------------------------------------|
| [**MicrosoftDNS \_ AType**](microsoftdns-atype.md)         | Nombre para el registro de asignación de direcciones                               |
| [**MicrosoftDNS \_ AAAAType**](microsoftdns-aaaatype.md)   | Registro de host a dirección IPv6                                  |
| [**MicrosoftDNS \_ AFSDBType**](microsoftdns-afsdbtype.md) | Registro de servidor de base de datos de sistema de archivos Andrew                    |
| [**MicrosoftDNS \_ ATMAType**](microsoftdns-atmatype.md)   | Registro de dirección a nombre de ATM                                   |
| [**MicrosoftDNS \_ CNAMEType**](microsoftdns-cnametype.md) | Registro de [*nombre canónico*](c-gly.md) |
| [**MicrosoftDNS \_ HINFOType**](microsoftdns-hinfotype.md) | Registro de información de host                                      |
| [**MicrosoftDNS \_ ISDNType**](microsoftdns-isdntype.md)   | Registro de red digital de servicios integrados                   |
| [**El \_ KEYType de MicrosoftDNS**](microsoftdns-keytype.md)     | Registro de clave. Consulte RFC 2535                                     |
| [**MicrosoftDNS \_ MBType**](microsoftdns-mbtype.md)       | Registro de buzón                                               |
| [**MicrosoftDNS \_ MDType**](microsoftdns-mdtype.md)       | Agente de correo para el registro de dominio                             |
| [**MicrosoftDNS \_ MFType**](microsoftdns-mftype.md)       | Agente de reenvío de correo para el registro de dominio                  |
| [**MicrosoftDNS \_ MGType**](microsoftdns-mgtype.md)       | Registro de grupo de correo                                            |
| [**MicrosoftDNS \_ MINFOType**](microsoftdns-minfotype.md) | Registro de información de correo                                      |
| [**MicrosoftDNS \_ MRType**](microsoftdns-mrtype.md)       | Registro de cambio de nombre de buzón                                        |
| [**MicrosoftDNS \_ MXType**](microsoftdns-mxtype.md)       | Registro del intercambio de correo                                        |
| [**MicrosoftDNS \_ NSType**](microsoftdns-nstype.md)       | Registro de servidor DNS                                           |
| [**MicrosoftDNS \_ NXTType**](microsoftdns-nxttype.md)     | Siguiente registro                                                  |
| [**MicrosoftDNS \_ PTRType**](microsoftdns-ptrtype.md)     | Registro de asignación de dirección a nombre                               |
| [**MicrosoftDNS \_ RPType**](microsoftdns-rptype.md)       | Registro de persona responsable                                    |
| [**MicrosoftDNS \_ RTType**](microsoftdns-rttype.md)       | Ruta a través del registro                                         |
| [**MicrosoftDNS \_ SIGType**](microsoftdns-sigtype.md)     | Registro de firma                                             |
| [**MicrosoftDNS \_ SOAType**](microsoftdns-soatype.md)     | Inicio de autoridad                                           |
| [**MicrosoftDNS \_ SRVType**](microsoftdns-srvtype.md)     | Registro de servicio                                               |
| [**MicrosoftDNS \_ TXTType**](microsoftdns-txttype.md)     | Registro de texto                                                  |
| [**MicrosoftDNS \_ WINSType**](microsoftdns-winstype.md)   | Registro de servidor WINS                                           |
| [**MicrosoftDNS \_ WINSRType**](microsoftdns-winsrtype.md) | Registro de búsqueda inversa WINS                                   |
| [**MicrosoftDNS \_ WKSType**](microsoftdns-wkstype.md)     | Registro de servicios conocidos                                   |
| [**MicrosoftDNS \_ X25Type**](microsoftdns-x25type.md)     | Registro de asignación de dirección a nombre de X. 121                         |



 

## <a name="administration-steps"></a>Pasos de administración

El proveedor WMI de DNS permite la administración de RRs desde el propio servidor o desde hosts remotos. Los pasos generales necesarios para administrar los RRs mediante el proveedor WMI de DNS son los siguientes:

-   Conexión al proveedor WMI de DNS
-   Obtener una instancia de registro de recursos
-   Enumerar o modificar una propiedad de registro de recursos o usar un método

Las siguientes tareas están vinculadas a sus ejemplos de scripting asociados.

-   [Enumerar tipos de recursos](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Agregar un registro de recursos](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Eliminación de un registro de recursos](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Modificar un registro de recursos](dns-wmi-provider-samples-managing-dns-resource-records.md)

 

 




