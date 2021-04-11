---
description: DACL para un nuevo objeto
ms.assetid: ff1146d7-5229-4c75-9768-28c3fab5fcea
title: DACL para un nuevo objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01d1ec8e92d4d56f977d4454b9a67df0a9bd489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155096"
---
# <a name="dacl-for-a-new-object"></a>DACL para un nuevo objeto

El sistema utiliza el siguiente algoritmo para crear una DACL para la mayoría de los tipos de objetos protegibles nuevos:

1.  La DACL del objeto es la DACL del [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) especificado por el creador del objeto. El sistema combina cualquier ACE heredable en la DACL especificada, a menos que \_ el \_ bit protegido de DACL se establezca en los bits de control del descriptor de seguridad.
2.  Si el creador no especifica un descriptor de seguridad, el sistema crea la DACL del objeto a partir de las ACE heredables.
3.  Si no se especifica ningún descriptor de seguridad y no hay ACE heredables, la DACL del objeto es la DACL predeterminada del [*token de suplantación*](/windows/desktop/SecGloss/i-gly) o [*principal*](/windows/desktop/SecGloss/p-gly) del creador.
4.  Si no hay ninguna DACL especificada, heredada o predeterminada, el sistema crea el objeto sin DACL, lo que permite que todos los usuarios tengan acceso total al objeto.

El sistema utiliza un algoritmo diferente para crear una DACL para un nuevo objeto de Active Directory. Para obtener más información, consulte [cómo se establecen los descriptores de seguridad en los nuevos objetos de directorio](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).

 

 
