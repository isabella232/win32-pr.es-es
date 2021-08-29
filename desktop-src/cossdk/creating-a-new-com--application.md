---
description: Creación de una nueva aplicación COM+
ms.assetid: eec4e871-36c2-4e60-9808-1400efcfc60c
title: Creación de una nueva aplicación COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93a899a1ab5a3680ab87d194c6fcb01a6b09bd8e063957fc79e251c874cb40ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070795"
---
# <a name="creating-a-new-com-application"></a>Creación de una nueva aplicación COM+

La creación de una nueva aplicación COM+ requiere dos pasos básicos, como se muestra a continuación:

-   Creación de una aplicación COM+ vacía (que se describe a continuación).
-   Agregar componentes a la aplicación. (Consulte [Instalación de nuevos componentes](installing-new-components.md) e importación de [componentes).](importing-components.md)

**Para crear una aplicación COM+ vacía**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, seleccione el equipo en el que desea crear una aplicación.

2.  Seleccione la **carpeta Aplicaciones COM+** para ese equipo.

3.  En el **menú Acción,** seleccione **Nuevo y,** a continuación, haga clic en **Aplicación.** También puede hacer clic con el botón derecho en la **carpeta Aplicaciones COM+,** seleccionar **Nuevo** y, a continuación, hacer clic en **Aplicación**.

4.  En la **página principal** del Asistente para instalación de aplicaciones COM+, haga clic en Siguiente y, **a** continuación, en el cuadro de diálogo Instalar o crear una nueva aplicación , haga clic en Crear una **aplicación vacía.**

5.  En el cuadro proporcionado, escriba un nombre para la nueva aplicación. (Tenga en cuenta que los siguientes caracteres especiales no se pueden usar en un nombre de aplicación: \\ , /, ~, !, \# @, %, ^, &, \* , (, ), , \| }, {, \] , \[ ', ", >, <, ., ?, :, y ;).) En **Tipo de activación ,** haga clic en Aplicación de **biblioteca** o Aplicación **de servidor.** Haga clic en **Next**.

    > [!Note]  
    > Una aplicación de servidor se ejecuta en su propio proceso. Las aplicaciones de servidor pueden admitir todos los servicios COM+. Una aplicación de biblioteca se ejecuta en el proceso del cliente que la crea. Las aplicaciones de biblioteca pueden usar la seguridad basada en roles, pero no admiten el acceso remoto ni los componentes en cola.

     

6.  En el **cuadro de diálogo Establecer identidad** de aplicación , elija una identidad con la que se ejecutará la aplicación. Si selecciona Este **usuario,** escriba el nombre de usuario y la contraseña. También debe volver a escribir la contraseña en el **cuadro Confirmar** contraseña. Haga clic en **Next**. (La selección predeterminada para la identidad de la aplicación es **Usuario interactivo**. El usuario interactivo es el usuario que inició sesión en el equipo servidor en un momento dado. Puede seleccionar otro usuario seleccionando Este **usuario** y especificando un usuario o grupo específico).

    > [!Note]  
    > El **cuadro de diálogo Establecer** identidad  de aplicación solo aparece si seleccionó Aplicación de servidor para el tipo de activación de la nueva aplicación en el cuadro de diálogo anterior del Asistente para instalación de aplicaciones COM. La propiedad identity no se usa para las aplicaciones de biblioteca.

     

7.  En el **cuadro de diálogo Agregar roles** de aplicación , agregue los roles que quiera asociar a la aplicación. De forma predeterminada, solo se define el rol **CreatorOwner.** Para obtener información sobre los roles, vea [Administración de seguridad basada en roles.](role-based-security-administration.md)

8.  En el cuadro de diálogo Agregar usuarios a **roles** , rellene cada rol que creó en el último paso con los usuarios, grupos o entidades de seguridad integradas a los que desea conceder los privilegios asociados a ese rol. De forma predeterminada, el usuario interactivo se coloca en el **rol CreatorOwner.**

9.  Haga clic en **Finalizar**

La nueva aplicación se mostrará ahora en la carpeta **Aplicaciones COM+** en el árbol de consola de la herramienta administrativa Servicios de componentes.

> [!Note]  
> A partir Windows Server 2003, las comprobaciones de acceso están habilitadas de forma predeterminada al crear una aplicación COM+. En versiones anteriores, las comprobaciones de acceso se deshabilitaban de forma predeterminada en el nivel de aplicación. El resultado es que, de forma predeterminada, el acceso a una aplicación COM+ solo se permite a los usuarios que se encuentran en los roles asociados a la aplicación. (Vea [Administración de seguridad basada en roles).](role-based-security-administration.md) Como alternativa, puede permitir el acceso a todos los usuarios deshabilitando las comprobaciones de acceso en una aplicación COM+. (Consulte [Habilitación de comprobaciones de acceso para una aplicación).](enabling-access-checks-for-an-application.md)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Copiar componentes](copying-components.md)
</dt> <dt>

[Eliminación de una aplicación COM+](deleting-a-com--application.md)
</dt> <dt>

[Importar componentes](importing-components.md)
</dt> <dt>

[Instalación de nuevos componentes](installing-new-components.md)
</dt> <dt>

[Mover componentes](moving-components.md)
</dt> <dt>

[Quitar un componente de una aplicación COM+](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



