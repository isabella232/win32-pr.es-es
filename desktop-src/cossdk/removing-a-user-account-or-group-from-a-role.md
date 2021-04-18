---
description: Si cambian los privilegios de los usuarios o si los roles se agregan a una aplicación, puede trasladar una cuenta de un rol a otro.
ms.assetid: 2d81a45a-9762-48b9-8395-3c3a4dcd5e8c
title: Quitar una cuenta de usuario o un grupo de un rol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176272aef16af0d0a65d90f6a1d7628a5af232fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714886"
---
# <a name="removing-a-user-account-or-group-from-a-role"></a>Quitar una cuenta de usuario o un grupo de un rol

Si cambian los privilegios de un usuario o si los roles se agregan a una aplicación, puede trasladar una cuenta de un rol a otro. Para trasladar una cuenta de usuario o un grupo de usuarios de un rol a otro, debe quitar la cuenta de usuario o el grupo de su rol actual y, a continuación, asignarlo al nuevo rol.

**Para trasladar una cuenta de usuario o un grupo de un rol a otro**

1.  Quite la cuenta de usuario o el grupo del rol al que ya no debería pertenecer, como se indica a continuación:

    1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación COM+ que contiene el rol que le interesa. Expanda la vista en el árbol de consola hasta que los usuarios del rol sean visibles.

    2.  Haga clic con el botón secundario en la cuenta de usuario o el grupo que desea quitar y, a continuación, haga clic en **eliminar**.

    3.  Cuando el cuadro de diálogo **Confirmar eliminación de elemento** se lo solicite, haga clic en **sí** para eliminar la cuenta de usuario o el grupo.

    La cuenta de usuario o el grupo que ha quitado del rol ya no aparece en la carpeta **usuarios** .

2.  Asigne la cuenta de usuario o el grupo que ha quitado a los roles a los que se debe asignar el usuario o grupo, como se indica a continuación:

    1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación COM+ que contiene el rol al que desea agregar la cuenta de usuario o el grupo. Expanda la vista en el árbol de consola hasta que los roles de la aplicación sean visibles.

    2.  Busque el rol al que desea agregar la cuenta de usuario o el grupo.

        > [!Note]  
        > Si el rol que está buscando no se encuentra en la carpeta **roles** , el rol no se ha agregado a la aplicación. El desarrollador debe agregarlo a la aplicación antes de poder asignar cuentas de usuario al rol.

         

    3.  Haga clic con el botón secundario en la carpeta **usuarios** del rol, elija **nuevo** y, a continuación, haga clic en **usuario**.

    4.  En la ventana **Seleccionar usuarios o grupos** , en el panel inferior, escriba el nombre completo del usuario o grupo que desea agregar. Si no conoce el nombre, haga clic en el botón **Opciones avanzadas** y, a continuación, haga clic en **Buscar ahora** para ver una lista de usuarios y grupos del dominio seleccionado. Seleccione un usuario o grupo en la lista **nombre (RDN)** y haga clic en **Aceptar**.

    5.  Cuando haya terminado de agregar la cuenta de usuario o el grupo al rol, haga clic en **Aceptar**.

    Para cada cuenta de usuario o grupo que haya asignado al rol, aparece un icono en la carpeta **usuarios** .

La pertenencia al rol modificada para la cuenta de usuario o el grupo surte efecto la próxima vez que se inicia la aplicación.

 

 



