---
title: Implementación opcional
description: Las siguientes características son opcionales, pero se recomienda
ms.assetid: 6123bdda-06cf-4b8b-b2a8-89882b6341b4
ms.tgt_platform: multiple
keywords:
- ADSI de implementación opcional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043b07f3a9bcfaef4bde8e95458d64828d4e46be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531840"
---
# <a name="optional-implementation"></a>Implementación opcional

Las siguientes características son opcionales, pero se recomienda:

-   La interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) para clientes que no son de automatización. Dado que el proveedor de OLE DB ADSI usa **IDirectorySearch** para presentar las consultas y recopilar los resultados del servicio de directorio subyacente, los proveedores que implementan esta interfaz proporcionan automáticamente acceso a las bases de datos de estilo OLE DB sin tener que implementar ninguna interfaz adicional.
-   Las interfaces [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)y [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) . Se recomienda que los proveedores de servicios de directorio que admiten la seguridad de objetos basada en ACL implementen estas características adicionales.

 

 




