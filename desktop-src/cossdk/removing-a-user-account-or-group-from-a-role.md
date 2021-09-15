---
description: Si cambian los privilegios de un usuario o si se agregan roles a una aplicación, puede mover una cuenta de un rol a otro.
ms.assetid: 2d81a45a-9762-48b9-8395-3c3a4dcd5e8c
title: Quitar una cuenta de usuario o un grupo de un rol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176272aef16af0d0a65d90f6a1d7628a5af232fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465771"
---
# <a name="removing-a-user-account-or-group-from-a-role"></a>Quitar una cuenta de usuario o un grupo de un rol

Si cambian los privilegios de un usuario o si se agregan roles a una aplicación, puede mover una cuenta de un rol a otro. Para mover una cuenta de usuario o un grupo de usuarios de un rol a otro, debe quitar la cuenta de usuario o el grupo de su rol actual y, a continuación, asignarla al nuevo rol.

**Para mover una cuenta de usuario o un grupo de un rol a otro**

1.  Quite la cuenta de usuario o el grupo del rol al que ya no debe pertenecer, como se muestra a continuación:

    1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación COM+ que contiene el rol que le interesa. Expanda la vista en el árbol de consola hasta que los usuarios del rol estén visibles.

    2.  Haga clic con el botón derecho en la cuenta de usuario o el grupo que desea quitar y, a continuación, haga clic **en Eliminar**.

    3.  Cuando se le solicite en el **cuadro de diálogo Confirmar eliminación** de elementos, haga clic en **Sí** para eliminar la cuenta de usuario o el grupo.

    La cuenta de usuario o el grupo que ha quitado del rol ya no aparece en la **carpeta** Usuarios.

2.  Asigne la cuenta de usuario o el grupo que ha quitado a los roles a los que se debe asignar el usuario o grupo, como se muestra a continuación:

    1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación COM+ que contiene el rol al que desea agregar la cuenta de usuario o el grupo. Expanda la vista en el árbol de consola hasta que los roles de la aplicación estén visibles.

    2.  Busque el rol al que desea agregar la cuenta de usuario o el grupo.

        > [!Note]  
        > Si el rol que busca no está en la **carpeta Roles,** el rol no se ha agregado a la aplicación. El desarrollador debe agregarlo a la aplicación para poder asignar cuentas de usuario al rol.

         

    3.  Haga clic con el botón derecho **en la** carpeta Usuarios del rol, seleccione **Nuevo** y, a continuación, haga clic en **Usuario.**

    4.  En la **ventana Seleccionar usuarios o** grupos, en el panel inferior, escriba el nombre completo del usuario o grupo que desea agregar. Si no conoce el nombre,  haga clic  en el botón Avanzadas y, a continuación, haga clic en Buscar ahora para ver una lista de usuarios y grupos en el dominio seleccionado. Seleccione un usuario o grupo en la **lista Nombre (RDN) y** haga clic en **Aceptar.**

    5.  Cuando haya terminado de agregar la cuenta de usuario o el grupo al rol, haga clic en **Aceptar.**

    Para cada cuenta de usuario o grupo que haya asignado al rol, aparecerá un icono en la **carpeta** Usuarios.

La pertenencia al rol cambiado para la cuenta de usuario o el grupo se aplica la próxima vez que se inicia la aplicación.

 

 



