---
description: Los grupos del mismo nivel requieren que cada miembro tenga un certificado específico, que se denomina certificado de miembro de grupo (GMC).
ms.assetid: 3966d4eb-4504-4b1e-9c9f-6eab7751d7ed
title: Cómo funciona la seguridad de grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d272e9a0567c6edc300a52cfa206305253ec5a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909773"
---
# <a name="how-group-security-works"></a>Cómo funciona la seguridad de grupo

Los grupos del mismo nivel requieren que cada miembro tenga un certificado específico, que se denomina certificado de miembro de grupo (GMC). El certificado GMC garantiza que todos los registros intercambiados entre pares están firmados digitalmente. La clave pública de un elemento del mismo nivel está contenida en las estructuras que se pasan como parte de la comunicación entre los elementos del mismo nivel, incluida la [**\_ \_ información de la credencial del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info).

Un GMC se puede emitir en una cadena. Por ejemplo, un creador puede emitir un GMC al administrador a, que puede emitir un GMC al administrador B, que puede emitir un GMC al miembro M. La cadena de GMC resultante es: Creator->A->B->M, que tiene una longitud de 4. La longitud de la cadena es importante, ya que no puede ser superior a 24. Si el vigésimo administrador de una cadena intenta emitir un GMC a un miembro, [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) o [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) devuelve una cadena del mismo nivel \_ \_ \_ demasiado \_ larga.

También se puede emitir un GMC llamando a [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials). Un GMC implica la pertenencia del usuario al grupo para el que se emite el GMC y puede tener una duración finita o infinita. La actividad de miembro de grupo no puede ser mayor que la duración especificada en GMC.

> [!Note]  
> La duración GMC infinita está establecida actualmente en 1000 años.

 

La actividad de miembro de grupo está limitada por la duración de GMC e incluye lo siguiente:

-   **Operaciones de registro** : un elemento del mismo nivel no puede publicar información en un grupo después de que expire la pertenencia al grupo o publicar registros cuya duración es mayor que la duración de la pertenencia a grupos del mismo nivel.
-   **Operaciones de pertenencia** : un administrador de grupo no puede emitir una pertenencia que tenga una duración superior a la especificada en la pertenencia del administrador del grupo. Por ejemplo, si un administrador tiene 500 horas restantes en su duración de GMC, todas las pertenencias emitidas deben ser inferiores a 500 horas.

Dado que un miembro del grupo no puede tener una duración más larga que el administrador que invita a ese miembro del grupo, se recomienda que establezca la duración de GMC de un administrador como infinita o para una duración muy larga. De forma predeterminada, el creador del grupo tiene una duración infinita.

## <a name="renewing-group-membership"></a>Renovación de la pertenencia a grupos

Para renovar las credenciales de un administrador o un miembro cuya vigencia de GMC esté lista para expirar, tiene las dos opciones siguientes:

-   Llame a [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) y pase la identidad del miembro cuya duración está lista para expirar. Si las credenciales se especifican como **null** y la información de pertenencia del mismo nivel está disponible para el grupo, la hora de renovación se establece en la misma duración que se especifica en las credenciales de miembro publicadas anteriormente. Si se debe especificar un período de duración diferente, se debe proporcionar una nueva estructura de [**\_ \_ información de credencial del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) que contenga la nueva duración de la duración y, a continuación, se publica un nuevo GMC para el miembro.

    La función [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) opcionalmente toma la \_ \_ marca de credenciales de almacén de grupo del mismo nivel \_ , que publica automáticamente las nuevas credenciales del miembro en la base de datos del grupo. Cuando el miembro se conecta al grupo la próxima vez, ya sea por primera vez o después de desconectarse, el miembro obtiene el GMC actualizado de la base de datos.

-   Llame a [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) para pasar la identidad del miembro cuya duración de GMC está lista para expirar. Si la fecha de expiración especificada en la invitación es **null**, la duración de la GMC es la misma que la del administrador GMC que emite la pertenencia. Si el creador especifica la expiración como **null**, se emite un GMC con una duración infinita.

    Si un elemento del mismo nivel emite un GMC que expira antes del valor de duración de la presencia, las direcciones del mismo nivel no están disponibles en las estructuras de [**\_ miembro del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_member) devueltas en la enumeración iniciada por una llamada a [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers). Esto sucede porque la información de presencia no se publica en este caso, aunque \_ \_ no se haya establecido la marca de presencia deshabilitar del mismo nivel.

 

 



