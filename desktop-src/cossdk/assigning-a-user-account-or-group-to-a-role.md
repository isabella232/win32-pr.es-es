---
description: Puede usar la herramienta administrativa Servicios de componentes para rellenar un rol con cuentas de usuario o grupos.
ms.assetid: 1cf7dc38-185a-4cc4-8f4c-44b6af4c5f4a
title: Asignación de una cuenta de usuario o un grupo a un rol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d53b37c9f0265e02c7abdf74eeaf81bd0b12e3d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714857"
---
# <a name="assigning-a-user-account-or-group-to-a-role"></a>Asignación de una cuenta de usuario o un grupo a un rol

Puede usar la herramienta administrativa Servicios de componentes para rellenar un rol con cuentas de usuario o grupos. La mejor manera de asignar una cuenta de usuario a un rol es asignar la cuenta de usuario a un grupo y, a continuación, asignar el grupo al rol. El uso de grupos para rellenar roles facilita la administración de un gran número de usuarios. En la ayuda en pantalla de la herramienta administrativa administración de equipos, vea el tema "usuarios y grupos locales" para obtener más información acerca de la creación de grupos o la asignación de una cuenta de usuario a un grupo.

> [!Note]  
> Para permitir que los usuarios de red sin autenticar ejecuten una aplicación COM+, los roles de aplicación deben incluir el usuario anónimo. A partir de Windows Server 2003, de forma predeterminada, el usuario anónimo no se incluye en el grupo todos.

 

Después de asignar la cuenta de usuario al grupo de Windows adecuado, siga estos pasos para asignar el grupo de Windows al rol.

**Para asignar un grupo de Windows a un rol de seguridad**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación COM+ que contiene el rol al que desea agregar la cuenta de usuario o el grupo. Expanda la vista en el árbol de consola hasta que los roles de la aplicación sean visibles.

2.  Busque el rol al que desea agregar la cuenta de usuario o el grupo.

    > [!Note]  
    > Si el rol que está buscando no se encuentra en la carpeta **roles** , el rol no se ha agregado a la aplicación. El desarrollador debe agregarlo a la aplicación antes de poder asignar cuentas de usuario al rol.

     

3.  Haga clic con el botón secundario en la carpeta **usuarios** del rol, elija **nuevo** y, a continuación, haga clic en **usuario**.

4.  En la ventana **Seleccionar usuarios o grupos** , en el panel inferior, escriba el nombre completo del usuario o grupo que desea agregar. Si no conoce el nombre, haga clic en el botón **Opciones avanzadas** y, a continuación, haga clic en **Buscar ahora** para ver una lista de usuarios y grupos del dominio seleccionado. Seleccione un usuario o grupo en la lista **nombre (RDN)** y haga clic en **Aceptar**.

5.  Para agregar más cuentas de usuario o grupos, repita el paso 4.

6.  Cuando haya terminado de agregar cuentas de usuario y grupos al rol, haga clic en **Aceptar**.

Para cada cuenta de usuario o grupo que haya asignado al rol, aparece un icono en la carpeta **usuarios** . La nueva pertenencia al rol surtirá efecto la próxima vez que se inicie la aplicación.

 

 



