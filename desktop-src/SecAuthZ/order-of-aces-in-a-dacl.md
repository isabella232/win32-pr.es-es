---
description: Cuando un proceso intenta acceder a un objeto protegible, el sistema pasa por las entradas de control de acceso (ACE) de la lista de control de acceso discrecional (DACL) de objetos hasta que encuentra las ACE que permiten o deniegan el acceso solicitado.
ms.assetid: fccf043e-e769-4f3f-b18c-252be20190d8
title: Orden de las ACE en una DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b5d017fe6441e90cded6458d8796dee301e3fa0fda01b7d088039abd9834ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907755"
---
# <a name="order-of-aces-in-a-dacl"></a>Orden de las ACE en una DACL

Cuando [](/windows/desktop/SecGloss/p-gly) un proceso intenta acceder a un objeto protegible, el sistema pasa por las entradas de [*control*](/windows/desktop/SecGloss/a-gly) de acceso (ACE) de la lista de [*control*](/windows/desktop/SecGloss/d-gly) de acceso discrecional (DACL) del objeto hasta que encuentra las ACE que permiten o deniegan el acceso solicitado. Los derechos de acceso que una DACL permite a un usuario pueden variar en función del orden de las ACE en la DACL. Por lo tanto, el Windows operativo XP define un orden preferido para las ACE en la DACL de un objeto protegible. El orden preferido proporciona un marco sencillo que garantiza que una ACE con acceso denegado deniegue realmente el acceso. Para obtener más información sobre el algoritmo del sistema para comprobar el acceso, vea Cómo controlan las [DACL el acceso a un objeto](how-dacls-control-access-to-an-object.md).

Para Windows Server 2003 y Windows XP, el orden correcto de las ACE se complica con la introducción de AEE específicas del objeto y la herencia automática.

En los pasos siguientes se describe el orden preferido:

1.  Todas las ACE explícitas se colocan en un grupo antes que las ACE heredadas.
2.  Dentro del grupo de ACE explícitas, las ACE con acceso denegado se colocan antes que las ACE con acceso permitido.
3.  Las ACE heredadas se colocan en el orden en que se heredan. Las ACE heredadas del elemento primario del objeto secundario proceden primero, las AEA heredadas del elemento primario principal, y así sucesivamente en el árbol de objetos.
4.  Para cada nivel de ACE heredadas, las ACE con acceso denegado se colocan antes que las ACE con acceso permitido.

Por supuesto, no todos los tipos ace son necesarios en una ACL.

Funciones como [**AddAccessAllowedAceEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) [**y AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) agregan una ACE al final de una ACL. Es responsabilidad del autor de la llamada asegurarse de que las ACE se agregan en el orden correcto.

 

 
