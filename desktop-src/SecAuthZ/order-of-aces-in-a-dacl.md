---
description: Cuando un proceso intenta acceder a un objeto protegible, el sistema pasa por las entradas de control de acceso (ACE) de la lista de control de acceso discrecional (DACL) de objetos hasta que encuentra las ACE que permiten o deniegan el acceso solicitado.
ms.assetid: fccf043e-e769-4f3f-b18c-252be20190d8
title: Orden de las ACE en una DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc45d6fd286bb06bd4311a8a02010c68832735ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265479"
---
# <a name="order-of-aces-in-a-dacl"></a>Orden de las ACE en una DACL

Cuando [](/windows/desktop/SecGloss/p-gly) un proceso intenta acceder a un objeto protegible, el sistema pasa por las entradas de [*control*](/windows/desktop/SecGloss/a-gly) de acceso (ACE) de la lista de control de acceso [*discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) del objeto hasta que encuentra las ACE que permiten o deniegan el acceso solicitado. Los derechos de acceso que una DACL permite a un usuario pueden variar en función del orden de las ACE en la DACL. Por lo tanto, Windows sistema operativo XP define un orden preferido para las ACE en la DACL de un objeto protegible. El orden preferido proporciona un marco sencillo que garantiza que una ACE con acceso denegado deniegue realmente el acceso. Para obtener más información sobre el algoritmo del sistema para comprobar el acceso, vea [How DACLs Control Access to an Object](how-dacls-control-access-to-an-object.md).

Para Windows Server 2003 y Windows XP, el orden correcto de las ACE es complicado con la introducción de AEE específicas del objeto y la herencia automática.

En los pasos siguientes se describe el orden preferido:

1.  Todas las ACE explícitas se colocan en un grupo antes de las ACE heredadas.
2.  Dentro del grupo de AEE explícitas, las ACE de acceso denegado se colocan antes que las ACE con acceso permitido.
3.  Las ACE heredadas se colocan en el orden en que se heredan. Las AEE heredadas del elemento primario del objeto secundario proceden primero, después las ACE heredadas del elemento primario principal, y así sucesivamente el árbol de objetos.
4.  Para cada nivel de AEC heredadas, las ACE con acceso denegado se colocan antes que las ACE con acceso permitido.

Por supuesto, no todos los tipos ace son necesarios en una ACL.

Funciones como [**AddAccessAllowedAceEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) [**y AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) agregan una ACE al final de una ACL. Es responsabilidad del autor de la llamada asegurarse de que las ACE se agregan en el orden correcto.

 

 
