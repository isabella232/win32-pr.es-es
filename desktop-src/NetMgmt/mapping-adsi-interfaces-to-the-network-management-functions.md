---
title: Asignación de interfaces ADSI a las funciones de administración de redes
description: Las Active Directory service interfaces (ADSI) son un conjunto de interfaces COM que se usan para acceder a las funcionalidades de los servicios de directorio de diferentes proveedores de red.
ms.assetid: dfa81c58-3ce4-40ee-8bfc-a19a13781992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ed9411989d5db754326a7a89130deada129fa6a58322ddef7e118772960d71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912055"
---
# <a name="mapping-adsi-interfaces-to-the-network-management-functions"></a>Asignación de interfaces ADSI a las funciones de administración de redes

Las Active Directory service interfaces (ADSI) son un conjunto de interfaces COM que se usan para acceder a las funcionalidades de los servicios de directorio de diferentes proveedores de red. ADSI presenta un único conjunto de interfaces de servicio de directorio para administrar recursos de red en un entorno informático distribuido.

Si está programando para Active Directory, es posible que pueda llamar a determinados métodos de interfaz ADSI para lograr la misma funcionalidad que puede lograr mediante una llamada a determinadas funciones de administración de red.

En la tabla siguiente se enumeran las funciones de administración de red y los grupos de funciones, así como las interfaces ADSI a las que se asignan las funciones.



| Functions                                                                  | Interfaces                                                                                             |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum), [ **NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource), [ **IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations) |
| [Netgroup](group-functions.md)\*                                          | [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)                                                                        |
| [NetLocalGroup](local-group-functions.md)\*                               | [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)                                                                        |
| [Netserver](server-functions.md)\*                                        | [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer)                                                                  |
| [NetSession](session-functions.md)\*                                      | [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession), [ **IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)   |
| [NetShare](share-functions.md)\*                                          | [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare)                                                                |
| [NetUser](user-functions.md)\*                                            | [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser), [ **IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer)                                   |
| [NetUserModals](user-modal-functions.md)\*                                | [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain)                                                                      |



 

Para obtener más información sobre los servicios de directorio y la programación con ADSI, [vea Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi). Para obtener información sobre las propiedades personalizadas que el proveedor winNT pone a disposición de la clase User y los métodos de propiedad de la interfaz [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) que el proveedor winNT no admite, consulta [ADSI WinNT Provider](/windows/desktop/ADSI/adsi-winnt-provider).

 

 