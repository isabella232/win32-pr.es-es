---
description: El sistema propaga las entradas de control de acceso (ACE) heredables a objetos secundarios según un conjunto de reglas de herencia.
ms.assetid: 08f76aaa-8379-4ba8-9735-7568001bcd53
title: Reglas de herencia de ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e8c786ebcc8450e8e5da1833f34fc85c37ea9f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073739"
---
# <a name="ace-inheritance-rules"></a>Reglas de herencia de ACE

El sistema propaga las entradas de [*control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) heredables a objetos secundarios según un conjunto de reglas de herencia. El sistema coloca las ACE heredadas en la lista de [*control*](/windows/desktop/SecGloss/d-gly) de acceso discrecional (DACL) del elemento secundario según el orden preferido de las ACE [en una DACL.](order-of-aces-in-a-dacl.md) El sistema establece la marca \_ ACE HEREDADA en todas las ACE heredadas.

Las AEE heredadas por los objetos secundarios contenedor y no contenedor difieren, en función de las combinaciones de marcas de herencia. Estas reglas de herencia funcionan igual para las DACL y las listas de [*control de acceso del sistema*](/windows/desktop/SecGloss/s-gly) (SACL).



| Marca ACE primaria                                  | Efecto en la ACL secundaria                                                                                                                                                                                                                      |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| OBJECT \_ INHERIT ACE only \_ (SOLO ACE DE HERENCIA DE OBJETO)                        | Objetos secundarios que no son contenedores: se heredan como una ACE efectiva. Objetos secundarios de contenedor: los contenedores heredan una ACE de solo herencia a menos que también se establezca la marca de \_ bits NO PROPAGATE INHERIT \_ \_ ACE.<br/>                                       |
| SOLO \_ ACE DE HERENCIA DE \_ CONTENEDOR                     | Objetos secundarios que no son de contenedor: no hay ningún efecto en el objeto secundario. Objetos secundarios de contenedor: el objeto secundario hereda una ACE efectiva. La ACE heredada es heredable a menos que también se establezca la marca de \_ bits NO PROPAGATE INHERIT \_ \_ ACE.<br/> |
| CONTAINER \_ INHERIT ACE y OBJECT INHERIT \_ \_ \_ ACE | Objetos secundarios que no son contenedores: se heredan como una ACE efectiva. Objetos secundarios de contenedor: el objeto secundario hereda una ACE efectiva. La ACE heredada es heredable a menos que también se establezca la marca de \_ bits NO PROPAGATE INHERIT \_ \_ ACE.<br/> |
| Sin marcas de herencia establecidas                         | Ningún efecto en los objetos secundarios de contenedor o no contenedor.                                                                                                                                                                                    |



 

Si una ACE heredada es una ACE efectiva para el objeto secundario, el sistema asigna los derechos genéricos a los derechos específicos del objeto secundario. De forma similar, el sistema asigna identificadores de seguridad [*genéricos*](/windows/desktop/SecGloss/s-gly) (SID), como CREATOR \_ OWNER, al SID adecuado. Si una ACE heredada es una ACE de solo herencia, los derechos genéricos o los SID genéricos se mantienen sin cambios para que se puedan asignar correctamente cuando la ACE la herede la próxima generación de objetos secundarios.

Para un caso en el que un objeto de contenedor hereda una ACE que sea efectiva en el contenedor y que sus descendientes puedan heredar, el contenedor puede heredar dos ACE. Esto sucede si la ACE heredable contiene información genérica. El contenedor hereda una ACE de solo herencia que contiene la información genérica y una ACE de solo eficacia en la que se ha asignado la información genérica.

Una [ACE específica del objeto](object-specific-aces.md) tiene un miembro **InheritedObjectType** que puede contener un GUID para identificar el tipo de objeto que puede heredar la ACE.

Si no se especifica el GUID **InheritedObjectType,** las reglas de herencia de una ACE específica del objeto son las mismas que para una ACE estándar.

Si se especifica el GUID **InheritedObjectType,** la ACE la heredan los objetos que coinciden con el GUID si se establece OBJECT INHERIT ACE y los contenedores que coinciden con el GUID si se establece \_ CONTAINER INHERIT \_ \_ \_ ACE. Tenga en cuenta que actualmente solo los objetos DS admiten AEE específicas del objeto y el DS trata todos los tipos de objetos como contenedores.

 

