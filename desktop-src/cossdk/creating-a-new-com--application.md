---
description: Crear una nueva aplicación COM+
ms.assetid: eec4e871-36c2-4e60-9808-1400efcfc60c
title: Crear una nueva aplicación COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c09eb296ad0a5f2326b5d931f59a5075d001d89f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705376"
---
# <a name="creating-a-new-com-application"></a>Crear una nueva aplicación COM+

La creación de una nueva aplicación COM+ requiere dos pasos básicos, como se indica a continuación:

-   Crear una aplicación COM+ vacía (descrita a continuación).
-   Agregar componentes a la aplicación. (Consulte [instalación de nuevos componentes](installing-new-components.md) e [importación de componentes](importing-components.md)).

**Para crear una aplicación COM+ vacía**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, seleccione el equipo en el que desea crear una aplicación.

2.  Seleccione la carpeta **aplicaciones com+** para ese equipo.

3.  En el menú **acción** , seleccione **nuevo** y, a continuación, haga clic en **aplicación**. También puede hacer clic con el botón secundario en la carpeta **aplicaciones com+** , seleccionar **nuevo** y, a continuación, hacer clic en **aplicación**.

4.  En la página **principal** del Asistente para instalación de aplicaciones com+, haga clic en **siguiente** y, en el cuadro de diálogo **instalar o crear una nueva aplicación** , haga clic en **crear una aplicación vacía**.

5.  En el cuadro proporcionado, escriba un nombre para la nueva aplicación. (Tenga en cuenta que los siguientes caracteres especiales no se pueden usar en un nombre de aplicación: \\ ,/, ~,!, @, \# ,%, ^, &, \* , (,), \| ,}, {, \] , \[ , ', ", >, <,.,?,:, y;.) En **tipo de activación**, haga clic en **aplicación de biblioteca** o **aplicación de servidor**. Haga clic en **Next**.

    > [!Note]  
    > Una aplicación de servidor se ejecuta en su propio proceso. Las aplicaciones de servidor pueden admitir todos los servicios COM+. Una aplicación de biblioteca se ejecuta en el proceso del cliente que la crea. Las aplicaciones de biblioteca pueden utilizar la seguridad basada en roles pero no admiten el acceso remoto o los componentes en cola.

     

6.  En el cuadro de diálogo **establecer identidad** de la aplicación, elija una identidad en la que se ejecutará la aplicación. Si selecciona **este usuario**, escriba el nombre de usuario y la contraseña. También debe escribir la contraseña en el cuadro **Confirmar contraseña** . Haga clic en **Next**. (La selección predeterminada de identidad de aplicación es **usuario interactivo**. El usuario interactivo es el usuario que ha iniciado sesión en el equipo servidor en un momento dado. Puede seleccionar un usuario diferente si selecciona **este usuario** y especifica un usuario o grupo específico).

    > [!Note]  
    > El cuadro de diálogo **establecer identidad de aplicación** solo aparece si ha seleccionado **aplicación de servidor** para el tipo de activación de la nueva aplicación en el cuadro de diálogo anterior del Asistente para instalación de aplicaciones com. La propiedad Identity no se utiliza para las aplicaciones de biblioteca.

     

7.  En el cuadro de diálogo **Agregar roles de aplicación** , agregue los roles que desee asociar a la aplicación. De forma predeterminada, solo se define el rol **CreatorOwner** . Para obtener información sobre los roles, consulte [Administración de la seguridad basada en roles](role-based-security-administration.md).

8.  En el cuadro de diálogo **Agregar usuarios a roles** , rellene cada rol que creó en el último paso con los usuarios, grupos o entidades de seguridad integradas a los que desea conceder los privilegios asociados a ese rol. De forma predeterminada, el usuario interactivo se coloca en el rol **CreatorOwner** .

9.  Haga clic en **Finalizar**

La nueva aplicación se mostrará en la carpeta **aplicaciones com+** en el árbol de consola de la herramienta administrativa Servicios de componentes.

> [!Note]  
> A partir de Windows Server 2003, las comprobaciones de acceso están habilitadas de forma predeterminada al crear una aplicación COM+. En versiones anteriores, las comprobaciones de acceso estaban deshabilitadas de forma predeterminada en el nivel de aplicación. El resultado es que, de forma predeterminada, el acceso a una aplicación COM+ solo se permite a los usuarios que están en los roles asociados con la aplicación. (Consulte [Administración de la seguridad basada en roles](role-based-security-administration.md)). Como alternativa, puede permitir el acceso a todos los usuarios deshabilitando las comprobaciones de acceso en una aplicación COM+. (Consulte [habilitación de comprobaciones de acceso para una aplicación](enabling-access-checks-for-an-application.md)).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Copiar componentes](copying-components.md)
</dt> <dt>

[Eliminar una aplicación COM+](deleting-a-com--application.md)
</dt> <dt>

[Importar componentes](importing-components.md)
</dt> <dt>

[Instalación de nuevos componentes](installing-new-components.md)
</dt> <dt>

[Mover componentes](moving-components.md)
</dt> <dt>

[Quitar un componente de una aplicación COM+](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



