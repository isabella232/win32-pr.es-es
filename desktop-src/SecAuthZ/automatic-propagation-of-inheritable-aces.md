---
description: Las funciones SetNamedSecurityInfo y SetSecurityInfo admiten la propagación automática de entradas de control de acceso (ACE) heredables.
ms.assetid: 0aa49b9b-13e3-4ef9-921d-ea47a013e5a1
title: Propagación automática de ACE heredables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257c038174549eebb8d960f8f4bc0601f95a928478e2a783f93f4a1444a22d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783722"
---
# <a name="automatic-propagation-of-inheritable-aces"></a>Propagación automática de ACE heredables

Las [**funciones SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) y [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) admiten la propagación automática de entradas de control de acceso (ACE) heredables. [](/windows/desktop/SecGloss/a-gly) Por ejemplo, si usa estas funciones para agregar una ACE heredable a un directorio de ntfs, el sistema aplica la ACE según corresponda a las listas de [*control*](/windows/desktop/SecGloss/a-gly) de acceso (ACL) de los subdirectorios o archivos existentes.

Las ACE aplicadas directamente tienen prioridad sobre las ACE heredadas. El sistema implementa esta prioridad colocando las ACE aplicadas directamente por delante de las ACE heredadas en una lista de [*control*](/windows/desktop/SecGloss/d-gly) de acceso discrecional (DACL). Cuando se llama a las funciones [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) y [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) para establecer la información de seguridad de un objeto, el sistema impone el modelo de herencia actual en las ACL de todos los objetos de la jerarquía debajo del objeto de destino. Para los objetos que se han convertido al modelo de herencia actual, los \_ bits SE DACL AUTO INHERITED y SE \_ \_ \_ SACL AUTO INHERITED \_ \_ [](/windows/desktop/SecGloss/s-gly) se establecen en el campo de control del descriptor de seguridad del objeto.

Cuando se crea un nuevo descriptor de seguridad que refleja el modelo de herencia actual, se tiene cuidado de no cambiar la semántica del descriptor de seguridad. Por lo tanto, permitir y denegar AEA nunca se mueven en relación entre sí. Si este movimiento es necesario (por ejemplo, para colocar todas las ACE no heredadas en la parte delantera de una ACL), la ACL se marca como protegida para evitar el cambio semántico.

El sistema usa las siguientes reglas al propagar las ACE heredadas a objetos secundarios:

-   Si un objeto secundario sin DACL hereda una ACE, el resultado es un objeto secundario con una DACL que contiene solo la ACE heredada.
-   Si un objeto secundario con una DACL vacía hereda una ACE, el resultado es un objeto secundario con una DACL que contiene solo la ACE heredada.
-   Si quita una ACE heredable de un objeto primario, la herencia automática quita las copias de la ACE heredadas por objetos secundarios.
-   Si la herencia automática da como resultado la eliminación de todas las ACE de la DACL de un objeto secundario, el objeto secundario tiene una DACL vacía en lugar de ninguna DACL.

Estas reglas pueden tener el resultado inesperado de convertir un objeto sin DACL en un objeto con una DACL vacía. Un objeto sin DACL permite el acceso completo, pero un objeto con una DACL vacía no permite ningún acceso. Como ejemplo de cómo estas reglas pueden crear una DACL vacía, suponga que agrega una ACE heredable al objeto raíz de un árbol de objetos. La herencia automática propaga la ACE heredable a todos los objetos del árbol. Los objetos secundarios que empezaron sin DACL ahora tienen una DACL con la ACE heredada. Si quita la ACE heredable del objeto raíz, el sistema propaga automáticamente el cambio a los objetos secundarios. Los objetos secundarios que empezaron sin DACL (lo que permite el acceso completo) ahora tienen una DACL vacía (que no permite ningún acceso).

Para asegurarse de que un objeto secundario sin DACL no se ve afectado por las ACE heredables, establezca la marca SE DACL PROTECTED en el descriptor de seguridad \_ \_ del objeto.

Para obtener información sobre cómo crear correctamente una DACL, vea [Crear una DACL.](/windows/desktop/SecBP/creating-a-dacl)

 

 
