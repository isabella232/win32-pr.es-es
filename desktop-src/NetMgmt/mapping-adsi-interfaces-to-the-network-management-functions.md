---
title: Asignación de interfaces ADSI a las funciones de administración de red
description: Las interfaces de servicio Active Directory (ADSI) son un conjunto de interfaces COM que se usan para tener acceso a las capacidades de los servicios de directorio de proveedores de red diferentes.
ms.assetid: dfa81c58-3ce4-40ee-8bfc-a19a13781992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ec1a1055d3d016bf8b7b1bd3f357810b7ddd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359406"
---
# <a name="mapping-adsi-interfaces-to-the-network-management-functions"></a>Asignación de interfaces ADSI a las funciones de administración de red

Las interfaces de servicio Active Directory (ADSI) son un conjunto de interfaces COM que se usan para tener acceso a las capacidades de los servicios de directorio de proveedores de red diferentes. ADSI presenta un único conjunto de interfaces de servicios de directorio para administrar los recursos de red en un entorno de computación distribuida.

Si programa para Active Directory, es posible que pueda llamar a determinados métodos de la interfaz ADSI para lograr la misma funcionalidad que puede lograr mediante una llamada a determinadas funciones de administración de red.

En la tabla siguiente se enumeran las funciones de administración de red y los grupos de funciones, y las interfaces ADSI a las que se asignan las funciones.



| Functions                                                                  | Interfaces                                                                                             |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum), [ **NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource), [ **IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations) |
| [Netgroups](group-functions.md)\*                                          | [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)                                                                        |
| [NetLocalGroup](local-group-functions.md)\*                               | [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)                                                                        |
| [NetServer](server-functions.md)\*                                        | [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer)                                                                  |
| [NetSession](session-functions.md)\*                                      | [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession), [ **IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)   |
| [NetShare](share-functions.md)\*                                          | [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare)                                                                |
| [NetUser](user-functions.md)\*                                            | [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser), [ **IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer)                                   |
| [NetUserModals](user-modal-functions.md)\*                                | [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain)                                                                      |



 

Para obtener más información acerca de los servicios de directorio y la programación con ADSI, consulte [Active Directory interfaces de servicio](/windows/desktop/ADSI/active-directory-service-interfaces-adsi). Para obtener información acerca de las propiedades personalizadas que el proveedor de WinNT pone a disposición de la clase de usuario y los métodos de propiedad de la interfaz [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) que el proveedor de WinNT no admite, vea [proveedor WinNT de ADSI](/windows/desktop/ADSI/adsi-winnt-provider).

 

 