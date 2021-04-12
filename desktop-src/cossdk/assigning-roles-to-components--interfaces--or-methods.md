---
description: Asignar roles a componentes, interfaces o métodos
ms.assetid: 687d5692-4a83-4de8-b99d-859aaaddd16d
title: Asignar roles a componentes, interfaces o métodos
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5efb66c9de865cbfcdc6e9cb047af92c95f6bc0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423411"
---
# <a name="assigning-roles-to-components-interfaces-or-methods"></a>Asignar roles a componentes, interfaces o métodos

Puede asignar explícitamente un rol a cualquier elemento de una aplicación COM+ que esté visible a través de la herramienta administrativa Servicios de componentes. Esto garantiza que todos los usuarios que sean miembros del rol tendrán acceso a ese elemento y a cualquier otro elemento que contenga. Por ejemplo, si asigna el rol "lectores" a un componente, se permite que cualquier miembro de "lectores" tenga acceso a ese componente y a cualquier interfaz y método que exponga. Los "lectores" se mostrarán como un rol heredado para cualquiera de esas interfaces y métodos.

Solo se puede tener acceso a un método a los llamadores si se le asigna un rol, ya sea asignando explícitamente el rol directamente al método o asignando un rol a la interfaz del método o al componente del método, en cuyo caso el rol lo heredará el método. Si no se asigna ningún rol y las comprobaciones de acceso están habilitadas, se producirá un error en todas las llamadas al método.

Antes de poder asignar un rol, debe [definirlo](defining-roles-for-an-application.md) para la aplicación. Todos los roles definidos para la aplicación aparecerán en los **roles establecidos explícitamente para la ventana elementos seleccionados** en la pestaña **seguridad** para todos los componentes, métodos e interfaces dentro de la aplicación.

**Para asignar roles a un componente, método o interfaz**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación COM+ para la que se ha definido el rol. Expanda el árbol para ver los componentes, las interfaces o los métodos de la aplicación, en función de la asignación de la función.

2.  Haga clic con el botón secundario en el elemento al que desea asignar el rol y, a continuación, haga clic en **propiedades**.

3.  En el cuadro de diálogo Propiedades, haga clic en la pestaña **seguridad** .

4.  En el cuadro los **roles se establecen explícitamente para los elementos seleccionados** , seleccione los roles que desea asignar al elemento.

5.  Haga clic en **OK**.

Cualquier rol que se haya establecido explícitamente para un elemento será heredado por los elementos de nivel inferior que contenga y se mostrará en la ventana de **roles heredados por** los elementos seleccionados para esos elementos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la seguridad de Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Definición de roles para una aplicación](defining-roles-for-an-application.md)
</dt> <dt>

[Habilitación de las comprobaciones de acceso para una aplicación](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Habilitar comprobaciones de acceso en el nivel de componente](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Establecimiento de un nivel de seguridad para las comprobaciones de acceso](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



