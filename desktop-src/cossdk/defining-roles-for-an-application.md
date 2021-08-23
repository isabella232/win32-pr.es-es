---
description: Para determinar una directiva de seguridad para una aplicación, defina los privilegios de seguridad que requiere.
ms.assetid: 0348684f-aebd-4d2d-a69b-85fea551c0cd
title: Definir roles para una aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc4b4fb6aaee557eea69dec405254925cd669d18ac73cdea229f548145d8701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637715"
---
# <a name="defining-roles-for-an-application"></a>Definir roles para una aplicación

Para determinar una directiva de seguridad para una aplicación, defina los privilegios de seguridad que requiere. Para ello, declare un nivel simbólico de privilegios como rol, es decir, defina el rol de la aplicación y, a continuación, asigne el rol a recursos específicos dentro de la aplicación. [](assigning-roles-to-components--interfaces--or-methods.md) Este diseño se cumple cuando se implementa la aplicación y los administradores del sistema rellenan el rol con usuarios y grupos de usuarios reales. Para obtener más detalles, vea [Administración de seguridad basada en roles.](role-based-security-administration.md)

**Para agregar un rol a una aplicación**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación COM+ a la que desea agregar el rol. Expanda el árbol para ver las carpetas de la aplicación.

2.  Haga clic con el botón derecho en la carpeta **Roles** de la aplicación, seleccione **Nuevo** y, a continuación, haga clic **en Rol**.

3.  En el **cuadro de** diálogo Rol , escriba el nombre del nuevo rol en el cuadro proporcionado.

4.  Haga clic en **Aceptar**.

> [!Note]  
> Después de agregar roles a la aplicación, debe asegurarse de asignar los roles a los componentes, interfaces y métodos adecuados. De lo contrario, si se ha elegido y habilitado la seguridad basada en roles y si se han agregado roles pero no se han asignado, se producirá un error en todas las llamadas a la aplicación. Para obtener más información, vea [Asignación de roles a componentes, interfaces o métodos.](assigning-roles-to-components--interfaces--or-methods.md)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de roles a componentes, interfaces o métodos](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Configuración de Role-Based seguridad](configuring-role-based-security.md)
</dt> <dt>

[Habilitar comprobaciones de acceso para una aplicación](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Habilitar comprobaciones de acceso en el nivel de componente](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Establecer un nivel de seguridad para las comprobaciones de acceso](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



