---
title: Implementación opcional
description: Las siguientes características son opcionales, pero recomendadas
ms.assetid: 6123bdda-06cf-4b8b-b2a8-89882b6341b4
ms.tgt_platform: multiple
keywords:
- ADSI de implementación opcional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3074f3ef6b4d36713d483937ad0f6ef10167777a7c36f8d21427d7df2b0485a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838955"
---
# <a name="optional-implementation"></a>Implementación opcional

Las siguientes características son opcionales, pero se recomiendan:

-   Interfaz [**IDirectorySearch para**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) clientes que no son de Automation. Dado que el proveedor de OLE DB ADSI usa **IDirectorySearch** para presentar consultas y recopilar resultados del servicio de directorio subyacente, los proveedores que implementan esta interfaz proporcionan automáticamente acceso a bases de datos de estilo OLE DB sin tener que implementar ninguna interfaz adicional.
-   Interfaces [**IADsSecurityDescriptor,**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)e [**IADsAccessControlEntry.**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) Se recomienda que los proveedores de servicios de directorio que admiten la seguridad de objetos basada en ACL implementen estas características adicionales.

 

 




