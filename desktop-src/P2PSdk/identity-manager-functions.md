---
description: La API del administrador de identidades del mismo nivel usa las siguientes funciones.
ms.assetid: 7621d26b-92e3-40c9-b0ce-94647d67f2c4
title: Funciones de Identity Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea56df6500239141038f76ba312b84148581f8f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667426"
---
# <a name="identity-manager-functions"></a>Funciones de Identity Manager

La API del administrador de identidades del mismo nivel usa las siguientes funciones.



| Función                                                           | Descripción                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername)                   | Crea un nuevo nombre basado en el nombre existente de la identidad del mismo nivel y del clasificador especificados. Sin embargo, una llamada a [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername)no crea una nueva identidad.                                                                                                     |
| [**PeerEnumGroups**](/windows/desktop/api/P2P/nf-p2p-peerenumgroups)                           | Crea y devuelve un identificador de enumeración del mismo nivel que se usa para enumerar todos los grupos del mismo nivel asociados a una identidad del mismo nivel específica.                                                                                                                                                                          |
| [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities)                   | Crea y devuelve un identificador de enumeración del mismo nivel que se usa para enumerar todas las identidades del mismo nivel que pertenecen a un usuario específico.                                                                                                                                                                                |
| [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration)                   | Libera una enumeración, por ejemplo, una enumeración de registros o de miembros y cancela la asignación de todos los recursos asociados a la enumeración.                                                                                                                                                                   |
| [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata)                               | Desasigna un bloque de datos y lo devuelve al bloque de memoria.                                                                                                                                                                                                                                         |
| [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount)                       | Devuelve un recuento de los elementos de una enumeración del mismo nivel.                                                                                                                                                                                                                                                    |
| [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem)                         | Devuelve un número específico de elementos de una enumeración del mismo nivel.                                                                                                                                                                                                                                            |
| [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)                   | Crea una nueva identidad del mismo nivel y devuelve su nombre. El nombre de la identidad del mismo nivel debe pasarse en todas las llamadas subsiguientes a las funciones de administrador de identidad del mismo nivel, agrupación del mismo nivel o PNRP que operan en nombre de la identidad del mismo nivel. El nombre de identidad del mismo nivel especifica qué identidad del mismo nivel se está usando. |
| [**PeerIdentityDelete**](/windows/desktop/api/P2P/nf-p2p-peeridentitydelete)                   | Elimina una identidad del mismo nivel. Esto incluye la eliminación de todos los certificados, las claves privadas y toda la información de grupo asociada a una identidad del mismo nivel especificada.                                                                                                                                                   |
| [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport)                   | Permite a un usuario exportar una identidad del mismo nivel. Después, el usuario puede transferir la identidad del mismo nivel a otro equipo.                                                                                                                                                                                       |
| [**PeerIdentityGetCryptKey**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetcryptkey)         | Recupera un identificador de un proveedor de servicios criptográficos (CSP).                                                                                                                                                                                                                                          |
| [**PeerIdentityGetDefault**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetdefault)           | Recupera el nombre de mismo nivel predeterminado establecido para el usuario actual.                                                                                                                                                                                                                                              |
| [**PeerIdentityGetFriendlyName**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetfriendlyname) | Devuelve el nombre descriptivo de la identidad del mismo nivel.                                                                                                                                                                                                                                                        |
| [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml)                   | Devuelve una descripción de la identidad del mismo nivel, que se puede pasar a terceros y usar para invitar una identidad del mismo nivel a un grupo del mismo nivel. Esta información se devuelve como un fragmento XML.                                                                                                           |
| [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)                   | Importa una identidad del mismo nivel. Si la identidad del mismo nivel existe en un equipo, se devuelve **peer \_ E \_ ya \_ existe** .                                                                                                                                                                                        |
| [**PeerIdentitySetFriendlyName**](/windows/desktop/api/P2P/nf-p2p-peeridentitysetfriendlyname) | Modifica el nombre descriptivo de una identidad del mismo nivel especificada. El nombre descriptivo es el nombre legible.                                                                                                                                                                                                |



 

 

 



