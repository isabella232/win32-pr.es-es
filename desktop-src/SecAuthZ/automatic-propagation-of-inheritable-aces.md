---
description: Las funciones SetNamedSecurityInfo y SetSecurityInfo admiten la propagación automática de entradas de control de acceso (ACE) heredables.
ms.assetid: 0aa49b9b-13e3-4ef9-921d-ea47a013e5a1
title: Propagación automática de ACE heredables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fab03c73a1c926468e46a0d0492e512dab42af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279638"
---
# <a name="automatic-propagation-of-inheritable-aces"></a>Propagación automática de ACE heredables

Las funciones [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) y [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) admiten la propagación automática de entradas de [*control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) heredables. Por ejemplo, si usa estas funciones para agregar una ACE heredable a un directorio de NTFS, el sistema aplica la ACE según corresponda a las [*listas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACL) de cualquier subdirectorio o archivo existente.

Las ACE aplicadas directamente tienen prioridad sobre las ACE heredadas. El sistema implementa esta precedencia colocando directamente las ACE aplicadas antes de las ACE heredadas en una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL). Cuando se llama a las funciones [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) y [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) para establecer la información de seguridad de un objeto, el sistema impone el modelo de herencia actual en las ACL de todos los objetos de la jerarquía por debajo del objeto de destino. En el caso de los objetos que se han convertido en el modelo de herencia actual, los bits heredados automáticos \_ \_ de DACL de se y de SACL automática \_ \_ \_ \_ se establecen en el campo de control del [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) del objeto.

Cuando se crea un nuevo descriptor de seguridad que refleja el modelo de herencia actual, se toma cuidado de no cambiar la semántica del descriptor de seguridad. Como tal, las ACE de permitir y denegar nunca se mueven en relación entre sí. Si se necesita este movimiento (por ejemplo, para colocar todas las ACE no heredadas al principio de una ACL), la ACL se marca como protegida para evitar el cambio semántico.

El sistema utiliza las siguientes reglas al propagar las ACE heredadas a objetos secundarios:

-   Si un objeto secundario sin DACL hereda una ACE, el resultado es un objeto secundario con una DACL que solo contiene la ACE heredada.
-   Si un objeto secundario con una DACL vacía hereda una ACE, el resultado es un objeto secundario con una DACL que solo contiene la ACE heredada.
-   Si quita una ACE heredable de un objeto primario, la herencia automática quita todas las copias de la ACE que heredaron los objetos secundarios.
-   Si la herencia automática da como resultado la eliminación de todas las ACE de la DACL de un objeto secundario, el objeto secundario tiene una DACL vacía en lugar de ninguna DACL.

Estas reglas pueden tener el resultado inesperado de la conversión de un objeto sin DACL a un objeto con una DACL vacía. Un objeto sin DACL permite el acceso total, pero un objeto con una DACL vacía no permite ningún acceso. Como ejemplo de cómo estas reglas pueden crear una DACL vacía, supongamos que agrega una ACE heredable al objeto raíz de un árbol de objetos. La herencia automática propaga la ACE heredable a todos los objetos del árbol. Los objetos secundarios que se iniciaron sin DACL ahora tienen una DACL con la ACE heredada. Si quita la ACE heredable del objeto raíz, el sistema propaga automáticamente el cambio a los objetos secundarios. Los objetos secundarios que se iniciaron sin DACL (que permite el acceso total) tienen ahora una DACL vacía (no se permite el acceso).

Para asegurarse de que un objeto secundario sin DACL no se vea afectado por las ACE que se puedan heredar, establezca la \_ marca de DACL \_ protegida en el descriptor de seguridad del objeto.

Para obtener información sobre cómo crear correctamente una DACL, vea [crear una DACL](/windows/desktop/SecBP/creating-a-dacl).

 

 
