---
description: Una entrada de control de acceso (ACE) es un elemento de una lista de control de acceso (ACL).
ms.assetid: 9cf4d796-3955-456b-9db9-ae9fa83752f6
title: Access Control entradas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fe98cf1c1c4d5fb23091a6539564ff964202cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666987"
---
# <a name="access-control-entries"></a>Access Control entradas

Una [*entrada de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) es un elemento de una [*lista de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACL). Una ACL puede tener cero o más ACE. Cada ACE controla o supervisa el acceso a un objeto por parte de un administrador de confianza especificado. Para obtener información sobre cómo agregar, quitar o cambiar las ACE en las ACL de un objeto, vea [modificar las ACL de un objeto en C++](modifying-the-acls-of-an-object-in-c--.md).

Hay seis tipos de ACE, tres de los cuales son compatibles con todos los objetos protegibles. Los otros tres tipos son [ACE específicas del objeto](object-specific-aces.md) que admiten los objetos de servicio de directorio.

Todos los tipos de ACE contienen la siguiente información de control de acceso:

-   [Identificador de seguridad](security-identifiers.md) (SID) que identifica el [Administrador de confianza](trustees.md) al que se aplica la ACE.
-   Una [*máscara de acceso*](/windows/desktop/SecGloss/a-gly) que especifica los [derechos de acceso](access-rights-and-access-masks.md) controlados por la ACE.
-   Marca que indica el tipo de ACE.
-   Un conjunto de marcas de bits que determinan si los contenedores u objetos secundarios pueden heredar la ACE del objeto principal al que está adjunta la ACL.

En la tabla siguiente se enumeran los tres tipos de ACE admitidos por todos los objetos protegibles.



| Tipo               | Descripción                                                                                                                                                                                                                                      |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACE de acceso denegado  | Se usa en una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) para denegar los derechos de acceso a un administrador de confianza.                                       |
| ACE de acceso permitido | Se usa en una DACL para permitir derechos de acceso a un administrador de confianza.                                                                                                                                                                                              |
| ACE de auditoría del sistema   | Se utiliza en una [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL) para generar un registro de auditoría cuando el administrador de confianza intenta ejercitar los derechos de acceso especificados. |



 

Para obtener una tabla de ACE específicas del objeto, vea [ACE específicas del objeto](object-specific-aces.md).

> [!Note]  
> No se admiten las ACE de objetos de alarma del sistema actualmente.

 

 

 
