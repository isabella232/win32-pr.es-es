---
description: Para determinar una directiva de seguridad para una aplicación, defina los privilegios de seguridad que requiere.
ms.assetid: 0348684f-aebd-4d2d-a69b-85fea551c0cd
title: Definición de roles para una aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e46eb2cb857a2b2dee2aabe41cb571e12ed98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705268"
---
# <a name="defining-roles-for-an-application"></a>Definición de roles para una aplicación

Para determinar una directiva de seguridad para una aplicación, defina los privilegios de seguridad que requiere. Para ello, declare un nivel simbólico de privilegio como un rol (es decir, defina el rol para la aplicación) y, a continuación, [asigne el rol](assigning-roles-to-components--interfaces--or-methods.md) a recursos específicos dentro de la aplicación. Este diseño se cumple cuando se implementa la aplicación y los administradores del sistema rellenan el rol con usuarios y grupos de usuarios reales. Para obtener más información, consulte [Administración de seguridad basada en roles](role-based-security-administration.md).

**Para agregar un rol a una aplicación**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación COM+ a la que desea agregar el rol. Expanda el árbol para ver las carpetas de la aplicación.

2.  Haga clic con el botón secundario en la carpeta **roles** de la aplicación, seleccione **nuevo** y, a continuación, haga clic en **rol**.

3.  En el cuadro de diálogo **rol**, escriba el nombre del nuevo rol en el cuadro proporcionado.

4.  Haga clic en **OK**.

> [!Note]  
> Después de agregar roles a la aplicación, debe asegurarse de asignar los roles a los componentes, interfaces y métodos adecuados. De lo contrario, si se ha elegido y habilitado la seguridad basada en roles y si se han agregado roles pero no se han asignado, se producirá un error en todas las llamadas a la aplicación. Para obtener más información, vea [asignar roles a componentes, interfaces o métodos](assigning-roles-to-components--interfaces--or-methods.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignar roles a componentes, interfaces o métodos](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Configuración de la seguridad de Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Habilitación de las comprobaciones de acceso para una aplicación](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Habilitar comprobaciones de acceso en el nivel de componente](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Establecimiento de un nivel de seguridad para las comprobaciones de acceso](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



