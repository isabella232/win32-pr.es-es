---
description: Puede usar la herramienta administrativa Servicios de componentes para rellenar un rol con cuentas de usuario o grupos.
ms.assetid: 1cf7dc38-185a-4cc4-8f4c-44b6af4c5f4a
title: Asignar una cuenta de usuario o un grupo a un rol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0d2883f9aedb5f3a0edf5dc33de54a03767e53a48f2dd8b9b6ea86c3a6211f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047673"
---
# <a name="assigning-a-user-account-or-group-to-a-role"></a>Asignar una cuenta de usuario o un grupo a un rol

Puede usar la herramienta administrativa Servicios de componentes para rellenar un rol con cuentas de usuario o grupos. La manera preferida de asignar una cuenta de usuario a un rol es asignar la cuenta de usuario a un grupo y, a continuación, asignar el grupo al rol. El uso de grupos para rellenar roles facilita la administración de un gran número de usuarios. En la ayuda en línea de la herramienta administrativa Administración de equipos, vea el tema "Usuarios y grupos locales" para obtener más información sobre cómo crear grupos o asignar una cuenta de usuario a un grupo.

> [!Note]  
> Para permitir que los usuarios de red no autenticados ejecuten una aplicación COM+, los roles de aplicación deben incluir el usuario anónimo. A partir Windows Server 2003, de forma predeterminada, el usuario anónimo no se incluye en el grupo Todos.

 

Después de asignar la cuenta de usuario al grupo de Windows adecuado, siga estos pasos para asignar el grupo de Windows al rol.

**Para asignar un grupo Windows a un rol de seguridad**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación COM+ que contiene el rol al que desea agregar la cuenta de usuario o el grupo. Expanda la vista en el árbol de consola hasta que los roles de la aplicación estén visibles.

2.  Busque el rol al que desea agregar la cuenta de usuario o el grupo.

    > [!Note]  
    > Si el rol que busca no está en la **carpeta Roles,** el rol no se ha agregado a la aplicación. El desarrollador debe agregarlo a la aplicación para poder asignar cuentas de usuario al rol.

     

3.  Haga clic con el botón derecho **en la** carpeta Usuarios del rol, seleccione **Nuevo** y, a continuación, haga clic en **Usuario.**

4.  En la **ventana Seleccionar usuarios o** grupos, en el panel inferior, escriba el nombre completo del usuario o grupo que desea agregar. Si no conoce el nombre,  haga clic en el botón Avanzadas y, a continuación, haga clic en Buscar **ahora** para ver una lista de usuarios y grupos en el dominio seleccionado. Seleccione un usuario o grupo en la **lista Nombre (RDN)** y haga clic **en Aceptar.**

5.  Para agregar más cuentas de usuario o grupos, repita el paso 4.

6.  Cuando haya terminado de agregar cuentas de usuario y grupos al rol, haga clic **en Aceptar.**

Para cada cuenta de usuario o grupo que haya asignado al rol, aparece un icono en la **carpeta** Usuarios. La nueva pertenencia a roles se aplica la próxima vez que se inicia la aplicación.

 

 



