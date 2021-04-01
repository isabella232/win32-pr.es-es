---
description: Puede quitar cuentas de usuario o grupos de un rol cuando los usuarios o los miembros de los grupos ya no deben tener acceso a los recursos de la aplicación a los que está asignado el rol.
ms.assetid: d2cfa5cb-a143-41de-9aa2-7af7fce10ed7
title: Mover una cuenta de usuario o un grupo a un rol diferente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2401d792066212269d4eaa4eb11eadfef6e2d73e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153390"
---
# <a name="moving-a-user-account-or-group-to-a-different-role"></a>Mover una cuenta de usuario o un grupo a un rol diferente

Puede quitar cuentas de usuario o grupos de un rol cuando los usuarios o los miembros de los grupos ya no deben tener acceso a los recursos de la aplicación a los que está asignado el rol.

**Para quitar una cuenta de usuario o un grupo de un rol**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación COM+ que contiene el rol que le interesa. Expanda la vista en el árbol de consola hasta que los usuarios del rol sean visibles.

2.  Haga clic con el botón secundario en la cuenta de usuario o el grupo que desea quitar y, a continuación, haga clic en **eliminar**.

3.  Cuando el cuadro de diálogo **Confirmar eliminación de elemento** se lo solicite, haga clic en **sí** para eliminar la cuenta de usuario o el grupo.

La cuenta de usuario o el grupo que ha quitado del rol ya no aparece en la carpeta **usuarios** . La nueva pertenencia al rol surtirá efecto la próxima vez que se inicie la aplicación. Si ha realizado cambios en la **aplicación del sistema**, debe reiniciar el equipo para que los cambios surtan efecto.

 

 



