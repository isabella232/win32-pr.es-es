---
description: SACL para un nuevo objeto
ms.assetid: 1d0d6fee-e5ec-4d8f-8ed8-10c725c57a6a
title: SACL para un nuevo objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb5bb5f276a869da3f48776bf96379edbd4af1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652451"
---
# <a name="sacl-for-a-new-object"></a>SACL para un nuevo objeto

El sistema utiliza el siguiente algoritmo para compilar una SACL para la mayoría de los tipos de objetos protegibles nuevos:

1.  La SACL del objeto es la SACL del [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) especificado por el creador del objeto. El sistema combina cualquier ACE heredable en la SACL especificada, a menos que \_ el \_ bit protegido de SACL se establezca en los bits de control del descriptor de seguridad. \_ \_ \_ Las ACE de atributo de recurso del sistema y \_ \_ el ID. de directiva de ámbito del sistema \_ \_ ACE de un objeto primario se combinarán con un nuevo objeto incluso si \_ SE establece el bit protegido de SACL de se \_ .
2.  Si el creador no especifica un descriptor de seguridad, el sistema genera la SACL del objeto a partir de las ACE heredables.
3.  Si no hay ninguna SACL especificada o heredada, el objeto no tiene SACL.

Para especificar una SACL para un nuevo objeto, el creador del objeto debe tener el \_ privilegio de nombre de seguridad se \_ habilitado. [](privileges.md) Si la SACL especificada para un nuevo objeto solo contiene \_ ACE de \_ atributo de recurso del sistema \_ , el \_ privilegio de nombre de seguridad se \_ no es necesario. El creador no necesita este privilegio si la SACL del objeto se crea a partir de las ACE heredadas.

El sistema utiliza un algoritmo diferente para compilar una SACL para un nuevo objeto de Active Directory. Para obtener más información, consulte [cómo se establecen los descriptores de seguridad en los nuevos objetos de directorio](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).

 

 
