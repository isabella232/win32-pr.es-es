---
description: Si un objeto de Windows no tiene una lista de control de acceso discrecional (DACL), el sistema permite que todos los usuarios tengan acceso completo a ella.
ms.assetid: be9633fb-14ef-42d2-9269-84287b35b653
title: DACL y ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28bf351fd59f634a7c7bf960aedac1c76659ad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279001"
---
# <a name="dacls-and-aces"></a>DACL y ACE

Si un objeto de Windows no tiene una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL), el sistema permite que todos los usuarios tengan acceso completo a ella. Si un objeto tiene una DACL, el sistema solo permite el acceso permitido explícitamente por las [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) en la DACL. Si no hay ninguna ACE en la DACL, el sistema no permite el acceso a nadie. Del mismo modo, si una DACL tiene ACE que permiten el acceso a un conjunto limitado de usuarios o grupos, el sistema deniega implícitamente el acceso a todos los que confían no incluidos en las ACE.

En la mayoría de los casos, puede controlar el acceso a un objeto mediante ACE con acceso permitido; no es necesario denegar explícitamente el acceso a un objeto. La excepción es cuando una ACE permite el acceso a un grupo y se desea denegar el acceso a un miembro del grupo. Para ello, coloque una ACE de acceso denegado para el usuario en la DACL por encima de la ACE de acceso permitido para el grupo. Tenga en cuenta que el [orden de las ACE](order-of-aces-in-a-dacl.md) es importante porque el sistema lee las ACE en secuencia hasta que se concede o se deniega el acceso. La ACE de acceso denegado del usuario debe aparecer en primer lugar; de lo contrario, cuando el sistema Lea la ACE de acceso permitido del grupo, se concederá acceso al usuario restringido.

En la ilustración siguiente se muestra una DACL que deniega el acceso a un usuario y concede acceso a dos grupos. Los miembros del grupo A obtienen los derechos de acceso de lectura, escritura y ejecución acumulando los derechos permitidos para agrupar A y los derechos permitidos para todos. La excepción es Andrew, a la que se deniega el acceso mediante la ACE de acceso denegado a pesar de ser miembro del grupo todos.

![DACL que concede derechos de acceso distintos en función de la pertenencia a grupos](images/accctrl1.png)

 

 
