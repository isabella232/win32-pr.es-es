---
description: En este tema se describe el proceso de invitar a un elemento del mismo nivel para unirse a un grupo del mismo nivel mediante las API de agrupación del mismo nivel.
ms.assetid: 6afcbfec-b1df-45cd-8a43-221dfe5d8c33
title: Invitar a un elemento del mismo nivel a un grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68b1e8852f58387d424944d4a8821f56b5e11e8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001998"
---
# <a name="inviting-a-peer-to-a-group"></a>Invitar a un elemento del mismo nivel a un grupo

En este tema se describe el proceso de invitar a un elemento del mismo nivel para unirse a un grupo del mismo nivel mediante las API de agrupación del mismo nivel.

Un grupo del mismo nivel requiere credenciales válidas para participar. Las credenciales se emiten desde fuera de un grupo en forma de invitaciones, o directamente a los miembros de un grupo cuando se necesitan actualizaciones de credenciales.

## <a name="group-member-certificates"></a>Certificados de miembros de grupo

Un grupo del mismo nivel se crea cuando una aplicación realiza una llamada a [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).

Para participar en un grupo del mismo nivel, cada elemento del mismo nivel debe tener una identidad del mismo nivel. Llame a [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) hasta que se devuelvan todas las identidades del mismo nivel definidas para el elemento del mismo nivel y seleccione la que se debe usar. Si no existe una identidad del mismo nivel, cree una llamando a [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).

Cada identidad del mismo nivel está asociada a un conjunto específico de credenciales que se pueden usar para demostrar la pertenencia al grupo del mismo nivel al conectarse, así como al publicar registros o invitar a miembros adicionales. Estas credenciales se representan como cadenas de [certificados X. 509](https://www.ietf.org/rfc/rfc2511.txt) denominados certificados de pertenencia a grupos (GMC).

Para crear el GMC para una identidad del mismo nivel, primero debe obtener su clave pública. Esta clave se obtiene llamando a [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) en el invitado potencial y pasando su identidad del mismo nivel. Esta función devuelve un certificado codificado en base 64 (IDC) que contiene la clave pública RSA que se usa para crear GMC para la identidad del mismo nivel (entre otras cosas), encapsulada en un BLOB XML, en el formato siguiente:

``` syntax
<PEERIDENTITYINFO VERSION="1.0">
     <IDC xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
          <!-- Base-64 encoded certificate  -->
     </IDC>
</PEERIDENTITYINFO>
```

Esta cadena se puede pasar a [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation), que devuelve una invitación que contiene el GMC para esa identidad del mismo nivel. La invitación se debe pasar al invitado mediante un proceso diferente, como correo electrónico, FTP o un recurso compartido de archivos seguro.

Como alternativa, el propio IDC se puede colocar en una nueva estructura de [**\_ \_ información de credenciales del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) y pasarse a [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials), que también genera una invitación.

Tenga en cuenta que las aplicaciones no pueden agregar etiquetas dentro de la etiqueta **PEERIDENTITYINFO** o modificar este fragmento XML de ningún modo. Las aplicaciones pueden incorporar este fragmento XML en otros documentos XML, pero deben quitar todos los XML específicos de la aplicación antes de pasar este fragmento a las funciones [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) o [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) .

Los administradores y el creador del grupo del mismo nivel emiten GMCs de miembro. Los miembros deben obtener GMCs nuevos con la duración prolongada de su GMCs antes de que haya transcurrido el tiempo de expiración. El administrador del grupo del mismo nivel emite las credenciales actualizadas llamando a [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) con las credenciales existentes para ese mismo nivel.

La estructura de [**\_ \_ información de credenciales del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) contiene los datos básicos en el estado de pertenencia de un elemento del mismo nivel, incluida la clave pública de sus GMC. Las credenciales recién emitidas se pueden publicar en el grupo del mismo nivel estableciendo la \_ \_ marca de credenciales del almacén de grupo del mismo nivel \_ en la llamada a [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials). Cuando el destinatario de las nuevas credenciales se une al grupo del mismo nivel, la infraestructura de agrupación del mismo nivel actualizará las credenciales existentes.

## <a name="issuing-an-invitation"></a>Emisión de una invitación

Se invita a un miembro a unirse al grupo del mismo nivel de una de las dos maneras siguientes:

-   Un administrador de grupo del mismo nivel llama a [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation), pasando la cadena XML de información de identidad obtenida del posible invitado a través de un mecanismo fuera de banda común, como el correo electrónico o una sesión de mensajería instantánea. La invitación también se pasa a través de algún mecanismo o proceso externo al elemento del mismo nivel, que en última instancia lo recibirá como una cadena o un archivo de texto XML.
-   Un administrador de grupo del mismo nivel llama a [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials). Para usar esta función, el elemento del mismo nivel debe haber publicado ya la información de pertenencia al grupo del mismo nivel ([**\_ miembro del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_member)) o tener una clave pública disponible (del par de claves de RSA que se usa para crear la identidad del firmante). En el primer caso, la estructura de [**\_ \_ información de credenciales del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) necesaria para **PeerGroupIssueCredentials** puede obtenerse a partir de la estructura de **\_ miembro del mismo nivel** ; en el último caso, se puede rellenar una nueva estructura de **\_ \_ información de credenciales del mismo nivel** con la clave pública.

Después de recibir la cadena de invitación, el elemento del mismo nivel lo pasa a [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) para unirse al grupo del mismo nivel. Si la llamada a **PeerGroupJoin** se realiza correctamente, el elemento del mismo nivel puede abrir el grupo del mismo nivel llamando a [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen).

## <a name="parsing-an-invitation"></a>Analizar una invitación

Opcionalmente, se puede analizar una invitación mediante una llamada a [**PeerGroupParseInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation), que devuelve una estructura de [**\_ \_ información de invitación del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) . Los campos de la estructura se pueden obtener fácilmente para fines de presentación.

 

 



