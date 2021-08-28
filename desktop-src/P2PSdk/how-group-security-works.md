---
description: Los grupos del mismo nivel requieren que cada miembro tenga un certificado específico, que se denomina certificado de miembro de grupo (GMC).
ms.assetid: 3966d4eb-4504-4b1e-9c9f-6eab7751d7ed
title: Funcionamiento de la seguridad de grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0941b4bded19b914218d5c011e8696cdd9c92612a493954dc5dd45d91e59006a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675215"
---
# <a name="how-group-security-works"></a>Funcionamiento de la seguridad de grupo

Los grupos del mismo nivel requieren que cada miembro tenga un certificado específico, que se denomina certificado de miembro de grupo (GMC). El certificado GMC garantiza que todos los registros intercambiados entre pares se firman digitalmente. La clave pública de un elemento del mismo nivel se encuentra en las estructuras que se pasan como parte de la comunicación entre los elementos del mismo nivel, incluida la información [**de credenciales del mismo \_ \_ nivel.**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info)

Un GMC se puede emitir en una cadena. Por ejemplo, un creador puede emitir un GMC al administrador A, que puede emitir un GMC al administrador B, que puede emitir un GMC al miembro M. La cadena GMC resultante es: creator->A->B->M, que tiene una longitud de 4. La longitud de la cadena es importante, ya que no puede ser superior a 24. Si el administrador número 24 de una cadena intenta emitir un GMC a un miembro, [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) o [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) devuelve PEER \_ E CHAIN TOO \_ \_ \_ LONG.

También se puede emitir un GMC llamando a [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials). Un GMC implica la pertenencia de usuarios al grupo para el que se emite el GMC y puede tener una duración finita o infinita. La actividad de miembro de grupo no puede ser mayor que la duración especificada en el GMC.

> [!Note]  
> La duración infinita de GMC está establecida actualmente en 1000 años.

 

La actividad de miembro de grupo está limitada por la duración de GMC e incluye lo siguiente:

-   **Operaciones de registro:** un usuario del mismo nivel no puede publicar información en un grupo después de que expire la pertenencia al grupo ni publicar registros que tengan una duración mayor que la duración de pertenencia a grupos del mismo nivel.
-   **Operaciones de pertenencia:** un administrador de grupo no puede emitir una pertenencia que tenga una duración posterior a la fecha especificada en la pertenencia del administrador del grupo. Por ejemplo, si un administrador tiene 500 horas restantes en su duración de GMC, todas las pertenencias emitidas deben ser inferiores a 500 horas.

Dado que un miembro del grupo no puede tener una duración mayor que el administrador que invita a ese miembro del grupo, se recomienda establecer la duración de GMC de un administrador como infinita o durante una duración muy larga. El creador del grupo tiene una duración infinita de forma predeterminada.

## <a name="renewing-group-membership"></a>Renovación de la pertenencia a grupos

Para renovar las credenciales de un administrador o miembro cuya duración de GMC está lista para expirar, tiene las dos opciones siguientes:

-   Llame [**a PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) y pase la identidad del miembro cuya duración está lista para expirar. Si las credenciales se especifican como **NULL** y la información de pertenencia del mismo nivel está disponible para el grupo, el tiempo de renovación se establece en la misma duración especificada en las credenciales de miembro publicadas anteriormente. Si se debe especificar un período de duración diferente, se debe proporcionar una nueva estructura [**DE \_ \_**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) INFORMACIÓN DE CREDENCIALES DEL MISMO NIVEL que contenga la nueva duración de duración y, a continuación, se publique un nuevo GMC para el miembro.

    La [**función PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) toma opcionalmente la marca PEER GROUP STORE CREDENTIALS, que publica automáticamente las nuevas credenciales del miembro en la base \_ de datos de \_ \_ grupo. Cuando el miembro se conecta al grupo la próxima vez, por primera vez o después de desconectarse, el miembro obtiene el GMC actualizado de la base de datos.

-   Llame [**a PeerGroupCreateInvitation para**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) pasar la identidad del miembro cuya duración de GMC está lista para expirar. Si la expiración especificada en la invitación es **NULL,** la duración del GMC es la misma que la del administrador de GMC que emite la pertenencia. Si el creador especifica la expiración como **NULL,** se emite un GMC con una duración infinita.

    Si se emite un GMC del mismo nivel que expira antes del valor de duración de presencia, las direcciones del mismo nivel no están disponibles en las estructuras [**MEMBER \_**](/windows/desktop/api/P2P/ns-p2p-peer_member) del mismo nivel devueltas en la enumeración iniciada por una llamada a [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers). Esto sucede porque la información de presencia no se publica en este caso, aunque no se establezca la marca PEER \_ DISABLE \_ PRESENCE.

 

 



