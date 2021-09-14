---
description: En este tema se describe el proceso de invitar a un elemento del mismo nivel a unirse a un grupo del mismo nivel mediante las API de agrupación del mismo nivel.
ms.assetid: 6afcbfec-b1df-45cd-8a43-221dfe5d8c33
title: Invitar a un par a un grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68b1e8852f58387d424944d4a8821f56b5e11e8d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069225"
---
# <a name="inviting-a-peer-to-a-group"></a>Invitar a un par a un grupo

En este tema se describe el proceso de invitar a un elemento del mismo nivel a unirse a un grupo del mismo nivel mediante las API de agrupación del mismo nivel.

Un grupo del mismo nivel requiere credenciales válidas para participar. Las credenciales se emiten desde fuera de un grupo en forma de invitaciones o directamente a los miembros de un grupo cuando se necesitan actualizaciones de credenciales.

## <a name="group-member-certificates"></a>Certificados de miembro de grupo

Se crea un grupo del mismo nivel cuando una aplicación realiza una llamada a [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).

Para participar en un grupo del mismo nivel, cada elemento del mismo nivel debe tener una identidad del mismo nivel. Llame [**a PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) hasta que se hayan devuelto todas las identidades del mismo nivel definidas para el mismo nivel y seleccione la que se debe usar. Si no existe una identidad del mismo nivel, cree una llamando a [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).

Cada identidad del mismo nivel está asociada a un conjunto específico de credenciales que se pueden usar para demostrar la pertenencia a grupos del mismo nivel al conectarse, así como al publicar registros o invitar a miembros adicionales. Estas credenciales se representan como cadenas de [certificados X.509 denominados](https://www.ietf.org/rfc/rfc2511.txt) certificados de pertenencia a grupos (GMC).

Para crear el GMC para una identidad del mismo nivel, primero debe obtener su clave pública. Esta clave se obtiene llamando a [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) en el posible invitado y pasando su identidad del mismo nivel. Esta función devuelve un certificado codificado en base 64 (IDC) que contiene la clave pública RSA usada para crear el GMC para la identidad del mismo nivel (entre otras cosas), encapsulado en un blob XML, en el formato siguiente:

``` syntax
<PEERIDENTITYINFO VERSION="1.0">
     <IDC xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
          <!-- Base-64 encoded certificate  -->
     </IDC>
</PEERIDENTITYINFO>
```

Esta cadena se puede pasar a [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation), que devuelve una invitación que contiene el GMC para esa identidad del mismo nivel. La invitación debe pasarse al invitado mediante un proceso diferente, como correo electrónico, FTP o un recurso compartido de archivos seguro.

Como alternativa, el propio IDC se puede colocar en una nueva estructura DE INFORMACIÓN DE [**\_ CREDENCIALES \_**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) DEL MISMO NIVEL y pasarse a [**PeerGroupIssueCredentials,**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)que también genera una invitación.

Tenga en cuenta que las aplicaciones no pueden agregar etiquetas dentro de la **etiqueta PEERIDENTITYINFO** ni modificar este fragmento XML de ninguna manera. Las aplicaciones pueden incorporar este fragmento XML en otros documentos XML, pero deben eliminar todos los XML específicos de la aplicación antes de pasar este fragmento a las funciones [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) o [**PeerGroupIssueCredentials.**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)

Los administradores y el creador del grupo del mismo nivel emiten los GFC de los miembros. Los miembros deben obtener nuevos GFC con duraciones extendidas de sus GFC antes de que transcurra la hora de expiración. El administrador del grupo del mismo nivel emite credenciales actualizadas mediante una llamada [**a PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) con las credenciales existentes para ese elemento del mismo nivel.

La [**estructura PEER \_ CREDENTIAL \_ INFO**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) contiene los datos básicos sobre el estado de pertenencia de un elemento del mismo nivel, incluida la clave pública de su GMC. Las credenciales recién emitidas se pueden publicar en el grupo del mismo nivel estableciendo la marca PEER GROUP STORE CREDENTIALS en la llamada a \_ \_ \_ [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials). Cuando el destinatario de las nuevas credenciales se une al grupo del mismo nivel, la infraestructura de agrupación del mismo nivel actualizará las credenciales existentes.

## <a name="issuing-an-invitation"></a>Emisión de una invitación

Se invita a un miembro a unirse al grupo del mismo nivel de una de las dos maneras siguientes:

-   Un administrador de grupo del mismo nivel llama a [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation), pasando la cadena XML de información de identidad obtenida del posible invitado a través de un mecanismo fuera de banda común, como el correo electrónico o una sesión de mensajería instantánea. La invitación también se pasa a través de algún proceso o mecanismo externo al elemento del mismo nivel, que en última instancia la recibirá como una cadena XML o un archivo de texto.
-   Un administrador de grupo del mismo [**nivel llama a PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials). Para usar esta función, el elemento del mismo nivel debe haber publicado ya la información de pertenencia al grupo del mismo nivel [**(MIEMBRO \_**](/windows/desktop/api/P2P/ns-p2p-peer_member)DEL MISMO NIVEL) o tener una clave pública disponible (del par de claves RSA usado para crear la identidad del sujeto). En el primer caso, la estructura [**PEER \_ CREDENTIAL \_ INFO**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) necesaria para **PeerGroupIssueCredentials** se puede obtener de la estructura **PEER \_ MEMBER;** en el último caso, se puede rellenar una nueva estructura **PEER \_ CREDENTIAL \_ INFO** con la clave pública.

Después de recibir la cadena de invitación, el mismo nivel la pasa a [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) para unirse al grupo del mismo nivel. Si la llamada a **PeerGroupJoin** se realiza correctamente, el mismo nivel puede abrir el grupo del mismo nivel llamando a [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen).

## <a name="parsing-an-invitation"></a>Análisis de una invitación

Opcionalmente, se puede analizar una invitación llamando a [**PeerGroupParseInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation), que devuelve una [**estructura DE INFORMACIÓN DE INVITACIÓN \_ \_ DEL**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) MISMO NIVEL. Los campos de la estructura se pueden obtener fácilmente con fines de presentación.

 

 



