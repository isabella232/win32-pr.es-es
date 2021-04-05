---
description: Una ACL de objetos puede contener las ACE que heredó de su contenedor primario.
ms.assetid: a9e5ad4d-61c6-43ed-a162-460683bcdb16
title: Herencia ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6462ed9523c94090924981db252b938f2056cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001698"
---
# <a name="ace-inheritance"></a>Herencia ACE

La ACL de un objeto puede contener las ACE que heredó de su contenedor primario. Por ejemplo, una subclave del registro puede heredar las ACE de la clave que se encuentra por encima en la jerarquía del registro. Del mismo modo, un archivo en un sistema de archivos NTFS puede heredar las ACE del directorio que lo contiene.

La estructura de [**\_ encabezado ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) de una ACE contiene un conjunto de marcadores de herencia que controlan la herencia de ACE y el efecto de una ACE en el objeto al que está asociada. El sistema interpreta los marcadores de herencia y otra información de herencia de acuerdo con las [reglas de herencia de ACE](ace-inheritance-rules.md).

Estas reglas se han mejorado con las siguientes características:

-   Compatibilidad con la [propagación automática de ACE heredables](automatic-propagation-of-inheritable-aces.md).
-   Marca que diferencia entre las ACE y ACE heredadas que se aplicaron directamente a un objeto.
-   ACE específicas del objeto que permiten especificar el tipo de objeto secundario que puede heredar la ACE.
-   La capacidad de evitar que una DACL o SACL herede las ACE mediante el establecimiento de los bits protegidos de la DACL de SE \_ \_ protegió o la \_ SACL \_ protegida en los bits de control [*del descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) , excepto para el atributo de recurso del sistema \_ \_ \_ ACE y el identificador de directiva del ámbito del sistema \_ \_ \_ \_ ACE.

 

 
