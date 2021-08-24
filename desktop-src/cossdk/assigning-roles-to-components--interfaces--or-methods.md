---
description: Asignación de roles a componentes, interfaces o métodos
ms.assetid: 687d5692-4a83-4de8-b99d-859aaaddd16d
title: Asignación de roles a componentes, interfaces o métodos
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22fcec11a52182bc0c9ac6f643c6c9cd75cb7b7462c35bbdea1ad0bc401f6ed4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029865"
---
# <a name="assigning-roles-to-components-interfaces-or-methods"></a>Asignación de roles a componentes, interfaces o métodos

Puede asignar explícitamente un rol a cualquier elemento dentro de una aplicación COM+ que sea visible a través de la herramienta administrativa Servicios de componentes. De este modo, se garantiza que a los usuarios que sean miembros del rol se les permitirá el acceso a ese elemento y a cualquier otro elemento que contenga. Por ejemplo, si asigna el rol "Lectores" a un componente, cualquier miembro de "Lectores" tiene permiso de acceso a ese componente y a las interfaces y métodos que expone. "Lectores" se mostrará como un rol heredado para cualquiera de esas interfaces y métodos.

Los autores de la llamada solo pueden acceder a un método si se le asigna un rol, ya sea asignando explícitamente el rol directamente al método o asignando un rol a la interfaz del método o al componente del método, en cuyo caso el rol lo heredará el método. Si no se asigna ningún rol y las comprobaciones de acceso están habilitadas, se producirá un error en todas las llamadas al método.

Para poder asignar un rol, debe [definirlo](defining-roles-for-an-application.md) para la aplicación. Todos los roles definidos para la aplicación aparecerán en la ventana  **Roles** establecidos explícitamente para los elementos seleccionados en la pestaña Seguridad de todos los componentes, métodos e interfaces de la aplicación.

**Para asignar roles a un componente, método o interfaz**

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación COM+ para la que se ha definido el rol. Expanda el árbol para ver los componentes, interfaces o métodos de la aplicación, en función de a qué se asigne el rol.

2.  Haga clic con el botón derecho en el elemento al que desea asignar el rol y, a continuación, haga clic en **Propiedades.**

3.  En el cuadro de diálogo propiedades, haga clic en **la pestaña** Seguridad.

4.  En el **cuadro Roles establecidos explícitamente** para los elementos seleccionados, seleccione los roles que desea asignar al elemento.

5.  Haga clic en **Aceptar**.

Los roles que haya establecido explícitamente para un elemento los heredarán los elementos de nivel inferior que contenga y se mostrarán en la ventana **Roles** heredados por elementos seleccionados para esos elementos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de Role-Based seguridad](configuring-role-based-security.md)
</dt> <dt>

[Definir roles para una aplicación](defining-roles-for-an-application.md)
</dt> <dt>

[Habilitar comprobaciones de acceso para una aplicación](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Habilitar comprobaciones de acceso en el nivel de componente](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Establecer un nivel de seguridad para las comprobaciones de acceso](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



