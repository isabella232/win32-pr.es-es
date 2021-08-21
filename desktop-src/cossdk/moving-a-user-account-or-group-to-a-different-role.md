---
description: Puede quitar cuentas de usuario o grupos de un rol cuando los usuarios o miembros de los grupos ya no deben tener acceso a los recursos de aplicación a los que se asigna el rol.
ms.assetid: d2cfa5cb-a143-41de-9aa2-7af7fce10ed7
title: Mover una cuenta de usuario o un grupo a un rol diferente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea402b6012fa4f6e7769e4bbb29a2a11da6e750636b0c139d5f5d6701a397116
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047343"
---
# <a name="moving-a-user-account-or-group-to-a-different-role"></a>Mover una cuenta de usuario o un grupo a un rol diferente

Puede quitar cuentas de usuario o grupos de un rol cuando los usuarios o miembros de los grupos ya no deben tener acceso a los recursos de aplicación a los que se asigna el rol.

**Para quitar una cuenta de usuario o un grupo de un rol**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación COM+ que contiene el rol que le interesa. Expanda la vista en el árbol de consola hasta que los usuarios del rol estén visibles.

2.  Haga clic con el botón derecho en la cuenta de usuario o el grupo que desea quitar y, a continuación, haga clic **en Eliminar**.

3.  Cuando se le solicite en el **cuadro de diálogo Confirmar eliminación** de elementos, haga clic en **Sí** para eliminar la cuenta de usuario o el grupo.

La cuenta de usuario o el grupo que ha quitado del rol ya no aparece en la **carpeta** Usuarios. La nueva pertenencia a roles se aplica la próxima vez que se inicia la aplicación. Si ha realizado cambios en la aplicación **del** sistema , debe reiniciar el equipo para que los cambios sumen efecto.

 

 



