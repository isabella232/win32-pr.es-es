---
title: Ventajas del uso de extensiones ADSI
description: La manera en que se implementan los métodos de extensión depende del escritor de extensiones.
ms.assetid: dbd1a203-b94c-4739-8c9d-aed1c9b43426
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a680e1eefbc05dac84b3420bee23287eda2bd02325274532109544b04ff73a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118018148"
---
# <a name="benefits-of-using-adsi-extensions"></a>Ventajas del uso de extensiones ADSI

La manera en que se implementan los métodos de extensión depende del escritor de extensiones. Un escritor de extensiones puede incluso implementar un método completamente fuera del ámbito del directorio. Por ejemplo, un desarrollador de software de copia de seguridad y restauración planea extender un objeto denominado **equipo**. El desarrollador debe crear dos métodos: **BackUp** y **Restore.** Estos métodos funcionan de forma remota en el equipo físico al **que** apunta el objeto de equipo del directorio. Al actuar como una extensión, el componente accede a la infraestructura ADSI y los clientes ADSI lo ven como una parte integral del objeto.

En los escenarios siguientes se describen situaciones en las que la creación de una extensión a ADSI sería ventajosa:

-   Cree una extensión para integrar un componente con el objeto de directorio. Dado que hay un **objeto de** usuario en el directorio, es posible que un desarrollador de RR. UU. quiera crear una extensión ADSI que rellene otros datos en el directorio cuando se **crea** un usuario.
-   Cree una extensión si un componente requiere una búsqueda de directorios. Un componente puede requerir un directorio como punto de partida para una búsqueda. Por ejemplo, al crear una nueva aplicación. Un objeto de aplicación, **ToolApp**, se puede publicar en el directorio . La aplicación puede admitir notificaciones de estado en una colección de servidores de correo. Decide convertir esta aplicación en una extensión ADSI.

    Ahora, un usuario puede buscar todas las instancias de **ToolApp** en el directorio. Para cada objeto devuelto, el usuario puede emitir una llamada a **NotifyNow().** Una aplicación o extensión puede obtener datos de objeto más actuales en el directorio y notificar a cada servidor de forma asincrónica.

-   Cree una extensión como una unión entre los espacios de nombres y los modelos de programación. Por ejemplo, un ISV inventará un nuevo modelo de objetos para los servicios de impresión. El **objeto printQueue** ya está definido en el directorio . El ISV puede crear una extensión ADSI y asociarla al **objeto printQueue.** Los usuarios adsi pueden enlazarse a **un objeto printQueue** y empezar a usar el modelo de objetos para el ISV. Desde la perspectiva del cliente ADSI, este punto de unión es transparente.
-   Cree una extensión para simplificar las tareas. Muchas tareas del directorio se pueden realizar buscando y estableciendo varios atributos en un objeto o en varios objetos. Al crear una sola función para manipular varios atributos, simplifica el desarrollo para los escritores de aplicaciones y scripts.

En el caso de los clientes ADSI, las extensiones enriquecen el entorno de programación ADSI de varias maneras:

-   Los desarrolladores que crean clientes ADSI no tienen que aprender un nuevo modelo de programación. Las extensiones forman parte de ADSI. Usarían el mismo paradigma para buscar, manipular datos y proteger objetos.
-   Los administradores pueden administrar aplicaciones relacionadas habilitadas para directorios mediante extensiones.
-   Los consumidores de extensiones pueden ver un objeto ADSI y una extensión como un objeto integrado.
-   Los componentes existentes se pueden integrar con ADSI, lo que permite que las extensiones aprovechen las inversiones existentes y creen un equilibrio entre los componentes.

Las extensiones ADSI se diseñaron con los siguientes objetivos:

-   Fácil de implementar. Con las tecnologías actuales de Microsoft, Microsoft Visual C++ de desarrollo y el Active Template Library, se puede crear rápidamente una extensión.
-   Los clientes ven un IDispatch. Desde la perspectiva de los escritores de scripts y automation, los métodos de extensión y las propiedades se combinan de forma transparente en un objeto ADSI.
-   Independiente. Los escritores de extensiones pueden extender ADSI de forma independiente sin tener conocimientos previos de las extensiones existentes.

Considere este escenario: un desarrollador corporativo o un ISV debe desarrollar un programa de copia de seguridad. Esta aplicación de copia de seguridad permite a un administrador realizar copias de seguridad de todos los equipos de una unidad organizativa. Con una extensión ADSI, es posible el siguiente script.


```VB
Dim ou
On Error Resume Next
Set ou = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
If Err.Number<>0 Then
    MsgBox("An error has occurred.")
    Err.Clear
    Set ou = Nothing
    Exit Sub
End If

ou.Filter = Array("computer")

For each comp in ou
   Debug.Print comp.Get("networkAddress")
   Debug.Print comp.LastBackUp
   comp.BackUpNow
Next
```



**LastBackUp es** una propiedad y **BackUpNow** es un método que proporciona el escritor de extensiones. El código muestra las ventajas para los consumidores y proveedores de extensiones. El escritor de extensiones no tiene que crear una nueva manera de filtrar, buscar y acceder al directorio. El consumidor de extensiones no tiene que volver a aprender un nuevo paradigma de programación. Los nuevos métodos y propiedades que proporciona el escritor de extensiones se ven como parte de ADSI.

 

 




