---
description: Tipos usados en las interfaces del dispensador de recursos COM+
ms.assetid: f4b3a828-3d66-455c-9b0c-30086f3ffe23
title: Tipos usados en las interfaces del dispensador de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c4d0f62ec7c61a9bc0f189c1ee02d1868a3242
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807633"
---
# <a name="types-used-in-com-resource-dispenser-interfaces"></a>Tipos usados en las interfaces del dispensador de recursos COM+

Los tipos siguientes se usan en las interfaces dispensadoras de recursos.



| Tipo           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RESTYPID**   | **DWORD** que identifica un tipo de recurso, no un recurso determinado. Un **RESTYPID** suele ser un puntero a una estructura en la memoria del dispensador que describe el tipo de recurso. El administrador dispensador no entiende (y no necesita comprender) esta estructura dentro de la memoria del dispensador de recursos. El gestor dispensador solo usa **RESTYPID** para hacer referencia a un tipo de recurso dentro de un dispensador de recursos.                                                                                                                                   |
| **RESID**      | **DWORD** que identifica un recurso determinado, en lugar de un tipo de recurso. Un **Resid** suele ser (**void \* *_ _) que apunta a una estructura en la memoria del dispensador de recursos que representa el recurso. No es necesario que el administrador dispensador entienda esta estructura dentro de la memoria del dispensador de recursos. El gestor dispensador utiliza _* Resid** para hacer referencia a un recurso determinado dentro de un dispensador de recursos.                                                                                                                                 |
| **SRESID**     | Una versión de cadena Unicode de **Resid**, que se usa en los métodos [**IHolder:: TrackResourceS**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-trackresources) y [**IHolder:: UntrackResourceS**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-untrackresources) . Las cadenas a veces son útiles cuando solo es necesario registrar una pequeña cantidad de información sobre un recurso y toda la descripción del recurso puede estar contenida en el **SRESID**. En concreto, el uso de **SRESID** a veces puede eliminar la necesidad de una asignación en el dispensador de recursos cuando el recurso representa una relación entre dos (o más) cosas. |
| **TRANSID**    | Identifica una transacción. Este tipo se puede convertir a la interfaz **ITransaction** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **TIMEINSECS** | Indica cuánto tiempo puede estar inactivo un recurso antes de que se destruya.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos del dispensador de recursos COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Interfaces dispensadoras de recursos COM+](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 



