---
description: En este tema se describen consideraciones de seguridad específicas al usar la infraestructura del mismo nivel.
ms.assetid: 088a2111-f4ee-4bec-98a9-ac138950958b
title: Consideraciones sobre la seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd3078834b3a69f988d17e5cbfd5fa1bd1591e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911621"
---
# <a name="security-considerations"></a>Consideraciones sobre la seguridad

En este tema se describen consideraciones de seguridad específicas al usar la infraestructura del mismo nivel.

Al desarrollar una aplicación del mismo nivel mediante la infraestructura del mismo nivel, por motivos de seguridad debe tener en cuenta los permisos de directorio, el acceso de invitado a los servicios de red del mismo nivel, la divulgación de información y la implementación del proveedor de servicios de seguridad.

## <a name="directory-permissions"></a>Permisos de directorio

Los servicios de red punto a punto almacenan los datos en el árbol de directorios de Perfil de usuario de un usuario. Un usuario debe tener permisos de escritura en el subárbol de datos de la **aplicación** del perfil. De forma predeterminada, esta lista de control de acceso (ACL) está configurada correctamente, pero un usuario puede cambiarla manualmente.

## <a name="guest-access-to-peer-networking-services"></a>Acceso de invitado a los servicios de red del mismo nivel

Una cuenta de invitado y los miembros del grupo de seguridad de Windows **Guests** no tienen acceso a la mayoría de los servicios del mismo nivel. Las aplicaciones deben tener acceso de usuario local o superior.

## <a name="information-disclosure"></a>Divulgación de información

La divulgación de información implica la dirección, la base de datos, la identidad y las credenciales de grupo. En las secciones siguientes se identifica y se define la divulgación de información.

**Divulgación de direcciones** El protocolo de resolución de nombres de mismo nivel (PNRP) es un servicio de resolución de identificadores que permite resolver un identificador de nombre del mismo nivel en una dirección IP. De forma similar a DNS, PNRP publica una dirección IP para que los usuarios que conocen el identificador correspondiente puedan resolverla en esa dirección.

-   La publicación de un identificador en PNRP significa que cualquier usuario puede resolver el identificador en la dirección IP publicada y determina la dirección IP del servicio PNRP que publicó la identidad.
-   La infraestructura de agrupación del mismo nivel publica automáticamente el nombre de grupo del mismo nivel de la instancia de grupo local en PNRP. Mientras está conectado a un grupo del mismo nivel, cualquier persona que conozca el nombre del mismo nivel para el grupo puede resolver las direcciones de los miembros activos y conoce la dirección actual de cada usuario.

La capacidad de un usuario de conectarse a otros miembros del grupo del mismo nivel o a nodos del grafo del mismo nivel mientras está conectado es una característica principal de las redes del mismo nivel. Mientras está conectado a un grupo o un grafo del mismo nivel, la dirección IP actual de un usuario se puede publicar en un registro de presencia dentro del grupo o del grafo del mismo nivel. De forma predeterminada, cualquier persona que participe en ese grupo o grafo del mismo nivel puede enumerar los miembros del grupo o del gráfico y determinar las direcciones actuales de los miembros. Esta capacidad es una propiedad configurable de agrupación del mismo nivel y de gráficos del mismo nivel.

**Divulgación de bases de datos** Las bases de datos de las infraestructuras de agrupación y de gráficos del mismo nivel se almacenan en el sistema de archivos local. Cualquier usuario de Windows con acceso administrativo al sistema de archivos local (por ejemplo, un administrador local) puede acceder teóricamente a los datos de la base de datos de grupo o del gráfico del mismo nivel local. Esto es coherente con la capacidad de los administradores locales para tener acceso a los datos del equipo local.

**Revelación de credenciales de identidad y grupo** La agrupación punto a punto requiere que los miembros establezcan conexiones entre sí para autenticarse mediante cadenas de certificados X. 509 modificadas. Como parte de la autenticación, se intercambian las cadenas correspondientes de identidad y pertenencia a grupos (GMC) de cada miembro.

Mientras está conectado a un grupo del mismo nivel, la infraestructura de agrupación del mismo nivel publica el nombre del mismo nivel del grupo con PNRP. Como parte de la operación de PNRP normal, se puede proporcionar la cadena GMC para ese grupo a otras instancias de PNRP para probar la autorización para publicar el nombre del mismo nivel del grupo.

## <a name="security-service-provider-implementation"></a>Implementación del proveedor del servicio de seguridad

La infraestructura de gráficos del mismo nivel es tan segura como el proveedor de servicios de seguridad (SSP) que implementa el desarrollador de aplicaciones. Cuanto más fuerte sea el SSP, mayor será la seguridad de la aplicación de gráficos del mismo nivel.

 

 



