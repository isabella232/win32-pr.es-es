---
description: En este tema se de abordan consideraciones de seguridad específicas al usar la infraestructura del mismo nivel.
ms.assetid: 088a2111-f4ee-4bec-98a9-ac138950958b
title: Consideraciones de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd3078834b3a69f988d17e5cbfd5fa1bd1591e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473658"
---
# <a name="security-considerations"></a>Consideraciones de seguridad

En este tema se de abordan consideraciones de seguridad específicas al usar la infraestructura del mismo nivel.

Al desarrollar una aplicación del mismo nivel mediante la infraestructura del mismo nivel, por motivos de seguridad debe tener en cuenta los permisos de directorio, el acceso de invitado a los servicios de red del mismo nivel, la divulgación de información y la implementación del proveedor de servicios de seguridad.

## <a name="directory-permissions"></a>Permisos de directorio

Los servicios de red punto a punto almacenan datos en el árbol de directorios del perfil de usuario de un usuario. Un usuario debe tener permisos de escritura en el subárbol **de datos de** la aplicación del perfil. De forma predeterminada, esta lista de control de acceso (ACL) se establece correctamente, pero un usuario puede cambiarla manualmente.

## <a name="guest-access-to-peer-networking-services"></a>Acceso de invitado a los servicios de redes del mismo nivel

Una cuenta de invitado y los **miembros** del grupo de Seguridad de Windows invitados no tienen acceso a la mayoría de los servicios del mismo nivel. Las aplicaciones deben tener acceso de usuario local o superior.

## <a name="information-disclosure"></a>Divulgación de información

La divulgación de información implica las credenciales de dirección, base de datos e identidad y grupo. En las secciones siguientes se identifica y define la divulgación de información.

**Divulgación de direcciones** El Protocolo de resolución de nombres del mismo nivel (PNRP) es un servicio de resolución de identificadores que permite resolver un identificador de nombre del mismo nivel en una dirección IP. De forma similar a DNS, PNRP publica una dirección IP para que los usuarios que conocen el identificador correspondiente puedan resolverla en esa dirección.

-   La publicación de un identificador en PNRP significa que cualquier usuario puede resolver el identificador en la dirección IP publicada y determinar la dirección IP del servicio PNRP que publicó la identidad.
-   La infraestructura de agrupación del mismo nivel publica automáticamente el nombre del grupo del mismo nivel de la instancia del grupo local en PNRP. Mientras está conectado a un grupo del mismo nivel, cualquier persona que conozca el nombre del mismo nivel para el grupo puede resolver las direcciones de los miembros activos y conoce la dirección actual de cada usuario.

La capacidad de un usuario de conectarse a otros miembros del grupo del mismo nivel o nodos de grafos del mismo nivel mientras ha iniciado sesión es una característica principal de las redes del mismo nivel. Mientras está conectado a un grupo o gráfico del mismo nivel, la dirección IP actual de un usuario se puede publicar en un registro de presencia dentro del grupo o gráfico del mismo nivel. De forma predeterminada, cualquier persona que participe en ese grupo o gráfico del mismo nivel puede enumerar los miembros del grupo o gráfico y determinar las direcciones actuales de los miembros. Esta capacidad es una propiedad configurable Peer Grouping y Peer Graphing.

**Divulgación de bases de datos** Las bases de datos de registro Peer Grouping and Graphing Infrastructures se almacenan en el sistema de archivos local. Cualquier Windows usuario con acceso administrativo al sistema de archivos local (por ejemplo, un administrador local) puede acceder teóricamente a los datos de la base de datos de grupo o gráfico del mismo nivel local. Esto es coherente con la capacidad de los administradores locales de acceder a los datos del equipo local.

**Divulgación de credenciales de identidad y grupo** La agrupación punto a punto requiere que los miembros establezcan conexiones entre sí para autenticarse mediante cadenas de certificados X.509 modificadas. Como parte de la autenticación, se intercambian las cadenas de identidad y certificado de pertenencia a grupos (GMC) correspondientes de cada miembro.

Mientras está conectado a un grupo del mismo nivel, la infraestructura de agrupación del mismo nivel publica el nombre del mismo nivel del grupo con PNRP. Como parte de la operación PNRP normal, la cadena GMC de ese grupo se puede proporcionar a otras instancias pnrp para demostrar la autorización para publicar el nombre del mismo nivel del grupo.

## <a name="security-service-provider-implementation"></a>Implementación del proveedor de servicios de seguridad

La infraestructura de Peer Graphing es tan segura como el proveedor de servicios de seguridad (SSP) que implementa el desarrollador de la aplicación. Entre más fuerte sea el SSP, mayor será la seguridad de la aplicación Peer Graphing.

 

 



