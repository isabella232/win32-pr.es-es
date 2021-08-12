---
description: Tipos usados en interfaces de dispensador de recursos com+
ms.assetid: f4b3a828-3d66-455c-9b0c-30086f3ffe23
title: Tipos usados en interfaces de dispensador de recursos com+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e98473ce108ea280532c2188e911b488e42669b98273b14fc229d003905b581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305235"
---
# <a name="types-used-in-com-resource-dispenser-interfaces"></a>Tipos usados en interfaces de dispensador de recursos com+

Los siguientes tipos se usan en las interfaces del dispensador de recursos.



| Tipo           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RESTYPID**   | DWORD **que** identifica un tipo de recurso, no un recurso determinado. Un **RESTYPID** suele ser un puntero a una estructura en la memoria del dispensador que describe el tipo de recurso. El administrador del dispensador no entiende (y no necesita comprender) esta estructura dentro de la memoria del distribuidor de recursos. El administrador del distribuidor usa **RESTYPID solo** para hacer referencia a un tipo de recurso dentro de un dispensador de recursos.                                                                                                                                   |
| **Resnum**      | DWORD **que** identifica un recurso determinado, en lugar de un tipo de recurso. Un **RESID** suele ser ( void _) que apunta a una estructura en la memoria del distribuidor de recursos **que representa el \* *recurso. El administrador del dispensador no necesita comprender esta estructura dentro de la memoria del distribuidor de recursos. El administrador del distribuidor usa _* RESID para** hacer referencia a un recurso determinado dentro de un dispensador de recursos.                                                                                                                                 |
| **SRESID**     | Una versión de cadena Unicode de **RESID**, que se usa en los métodos [**IHolder::TrackResourceS**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-trackresources) [**e IHolder::UntrackResourceS.**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-untrackresources) Las cadenas a veces son útiles cuando solo es necesario registrar una pequeña cantidad de información sobre un recurso y la descripción completa del recurso puede estar contenida en **el SRESID**. En concreto, el uso de **SRESID** a veces puede eliminar la necesidad de un mapa en el distribuidor de recursos cuando el recurso representa una relación entre dos (o más) cosas. |
| **TRANSID**    | Identifica una transacción. Este tipo se puede convertir a la **interfaz ITransaction.**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **TIMEINSECS** | Indica cuánto tiempo puede estar inactivo un recurso antes de que se destruya.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos del distribuidor de recursos com+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Interfaces de dispensador de recursos COM+](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 



