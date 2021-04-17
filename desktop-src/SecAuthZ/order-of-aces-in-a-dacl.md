---
description: Cuando un proceso intenta tener acceso a un objeto protegible, el sistema recorre las entradas de control de acceso (ACE) de la lista de control de acceso discrecional (DACL) de objetos hasta que encuentra ACE que permiten o deniegan el acceso solicitado.
ms.assetid: fccf043e-e769-4f3f-b18c-252be20190d8
title: Orden de ACE en una DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc45d6fd286bb06bd4311a8a02010c68832735ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667921"
---
# <a name="order-of-aces-in-a-dacl"></a>Orden de ACE en una DACL

Cuando un [*proceso*](/windows/desktop/SecGloss/p-gly) intenta tener acceso a un objeto protegible, el sistema recorre las [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) de la lista de control de [*acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) del objeto hasta que encuentra ACE que permiten o deniegan el acceso solicitado. Los derechos de acceso que una DACL permite a un usuario pueden variar en función del orden de las ACE en la DACL. Por lo tanto, el sistema operativo Windows XP define un orden preferido para las ACE en la DACL de un objeto protegible. El orden preferido proporciona un marco de trabajo sencillo que garantiza que una ACE de acceso denegado realmente deniega el acceso. Para obtener más información sobre el algoritmo del sistema para comprobar el acceso, vea [Cómo controlan el acceso a un objeto las DACL](how-dacls-control-access-to-an-object.md).

En Windows Server 2003 y Windows XP, el orden adecuado de las ACE es complicado por la introducción de ACE específicas del objeto y la herencia automática.

En los pasos siguientes se describe el orden preferido:

1.  Todas las ACE explícitas se colocan en un grupo antes de cualquier ACE heredada.
2.  Dentro del grupo de ACE explícitas, las ACE de acceso denegado se colocan antes que las ACE permitidas para acceso.
3.  Las ACE heredadas se colocan en el orden en el que se heredan. Las ACE heredadas del elemento primario del objeto secundario aparecen en primer lugar, a continuación, las ACE heredadas de la primaria y así sucesivamente en el árbol de objetos.
4.  Para cada nivel de ACE heredadas, las ACE de acceso denegado se colocan antes que las ACE permitidas para acceso.

Por supuesto, no todos los tipos ACE son necesarios en una ACL.

Funciones como [**AddAccessAllowedAceEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) y [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) agregan una ACE al final de una ACL. Es responsabilidad del autor de la llamada asegurarse de que las ACE se agreguen en el orden correcto.

 

 
