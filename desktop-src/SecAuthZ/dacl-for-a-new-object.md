---
description: DACL para un nuevo objeto
ms.assetid: ff1146d7-5229-4c75-9768-28c3fab5fcea
title: DACL para un nuevo objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cfd5b8f8c16919260c4dace5394f864fe987885a7f2203b2b41162b7c41e701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782144"
---
# <a name="dacl-for-a-new-object"></a>DACL para un nuevo objeto

El sistema usa el siguiente algoritmo para crear una DACL para la mayoría de los tipos de nuevos objetos protegibles:

1.  La DACL del objeto es la DACL del [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) especificado por el creador del objeto. El sistema combina todas las ACE heredables en la DACL especificada a menos que el SE DACL PROTECTED se establezca en los bits de control del \_ \_ descriptor de seguridad.
2.  Si el creador no especifica un descriptor de seguridad, el sistema compila la DACL del objeto a partir de ACE heredables.
3.  Si no se especifica ningún descriptor de seguridad y no hay ninguna ACE heredable, la DACL del objeto es la DACL predeterminada del token principal o [*de suplantación*](/windows/desktop/SecGloss/i-gly) del creador. [](/windows/desktop/SecGloss/p-gly)
4.  Si no hay ninguna DACL especificada, heredada o predeterminada, el sistema crea el objeto sin DACL, lo que permite a todos acceder al objeto.

El sistema usa un algoritmo diferente para compilar una DACL para un nuevo Active Directory objeto . Para obtener más información, vea [How Security Descriptors are Set on New Directory Objects](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).

 

 
