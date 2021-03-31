---
description: El sistema propaga entradas de control de acceso (ACE) heredables a objetos secundarios de acuerdo con un conjunto de reglas de herencia.
ms.assetid: 08f76aaa-8379-4ba8-9735-7568001bcd53
title: Reglas de herencia de ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e8c786ebcc8450e8e5da1833f34fc85c37ea9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813297"
---
# <a name="ace-inheritance-rules"></a>Reglas de herencia de ACE

El sistema propaga [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) heredables a objetos secundarios de acuerdo con un conjunto de reglas de herencia. El sistema coloca las ACE heredadas en la [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) del elemento secundario según el [orden preferido de las ACE en una DACL](order-of-aces-in-a-dacl.md). El sistema establece la \_ marca ACE heredada en todas las ACE heredadas.

Las ACE heredadas por objetos secundarios de contenedor y no contenedores difieren en función de las combinaciones de marcadores de herencia. Estas reglas de herencia funcionan igual para las DACL y [*las listas de control de acceso del sistema*](/windows/desktop/SecGloss/s-gly) (SACL).



| Marca ACE principal                                  | Efecto en la ACL secundaria                                                                                                                                                                                                                      |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Solo se hereda ACE del objeto \_                        | Objetos secundarios que no son de contenedor: heredados como una ACE efectiva. Objetos secundarios de contenedor: los contenedores heredan una ACE de solo heredar, a menos que \_ \_ también se establezca la marca de bits no propagar herencia de \_ ACE.<br/>                                       |
| El contenedor \_ hereda \_ solo ACE                     | Objetos secundarios que no son de contenedor: ningún efecto en el objeto secundario. Objetos secundarios de contenedor: el objeto secundario hereda una ACE efectiva. La ACE heredada se puede heredar a menos que \_ \_ \_ también se establezca la marca de bits no propagar herencia de ACE.<br/> |
| La ACE hereda el contenedor y la ACE \_ \_ de herencia de objetos \_ \_ | Objetos secundarios que no son de contenedor: heredados como una ACE efectiva. Objetos secundarios de contenedor: el objeto secundario hereda una ACE efectiva. La ACE heredada se puede heredar a menos que \_ \_ \_ también se establezca la marca de bits no propagar herencia de ACE.<br/> |
| No se ha establecido ningún marcador de herencia                         | Ningún efecto en los objetos contenedor o no contenedores secundarios.                                                                                                                                                                                    |



 

Si una ACE heredada es una ACE efectiva para el objeto secundario, el sistema asigna todos los derechos genéricos a los derechos específicos para el objeto secundario. De forma similar, el sistema asigna los [*identificadores de seguridad*](/windows/desktop/SecGloss/s-gly) genéricos (SID), como Creator \_ Owner, al SID adecuado. Si una ACE heredada es una ACE de solo heredar, los derechos genéricos o los SID genéricos se dejan sin cambios para que se puedan asignar adecuadamente cuando la ACE se herede por la próxima generación de objetos secundarios.

En el caso de que un objeto contenedor herede una ACE que sea efectiva en el contenedor y que hereden sus descendientes, el contenedor puede heredar dos ACE. Esto sucede si la ACE heredable contiene información genérica. El contenedor hereda una ACE de solo heredar que contiene la información genérica y una ACE solo efectiva en la que se ha asignado la información genérica.

Una [ACE específica del objeto](object-specific-aces.md) tiene un miembro **InheritedObjectType** que puede contener un GUID para identificar el tipo de objeto que puede heredar la ACE.

Si no se especifica el GUID de **InheritedObjectType** , las reglas de herencia de una ACE específica del objeto son las mismas que para una ACE estándar.

Si se especifica el GUID de **InheritedObjectType** , los objetos que coinciden con el GUID heredan la ACE si \_ se ha establecido la ACE de herencia de objetos \_ y los contenedores que coinciden con el GUID si \_ \_ se ha establecido la ACE de herencia de contenedor. Tenga en cuenta que actualmente solo los objetos de DS admiten ACE específicas del objeto y el DS trata todos los tipos de objeto como contenedores.

 

