---
title: Ventajas del uso de las extensiones ADSI
description: La forma en que se implementan los métodos de extensión depende del escritor de la extensión.
ms.assetid: dbd1a203-b94c-4739-8c9d-aed1c9b43426
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27e80e6c095fcc02ca02c57b0987d1e6ed410ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075083"
---
# <a name="benefits-of-using-adsi-extensions"></a>Ventajas del uso de las extensiones ADSI

La forma en que se implementan los métodos de extensión depende del escritor de la extensión. Un escritor de extensiones puede incluso implementar un método completamente fuera del ámbito del directorio. Por ejemplo, un desarrollador de software de copia de seguridad y restauración planea ampliar un objeto denominado **equipo**. El desarrollador debe crear dos métodos: **copia de seguridad** y **restauración**. Estos métodos funcionan de forma remota en el equipo físico al que apunta el objeto de **equipo** en el directorio. Al actuar como una extensión, el componente obtiene acceso a la infraestructura ADSI y lo ven los clientes ADSI como parte integral del objeto.

En los siguientes escenarios se describen situaciones en las que la creación de una extensión para ADSI sería ventajosa:

-   Cree una extensión para integrar un componente con el objeto de directorio. Dado que hay un objeto de **usuario** en el directorio, un desarrollador de recursos humanos puede querer crear una extensión ADSI que rellena otros datos en el directorio cuando se crea un **usuario** .
-   Cree una extensión si un componente requiere una búsqueda de directorio. Un componente puede requerir un directorio como punto de partida para una búsqueda. Por ejemplo, al crear una nueva aplicación. Un objeto de aplicación, **ToolApp**, se puede publicar en el directorio. La aplicación puede admitir notificaciones de estado en una colección de servidores de correo. Decide convertir esta aplicación en una extensión ADSI.

    Ahora, un usuario puede buscar todas las instancias de **ToolApp** en el directorio. Para cada objeto devuelto, el usuario puede emitir una llamada a **NotifyNow ()**. Una aplicación o extensión puede obtener más datos de objetos actuales en el directorio y notificar a cada servidor de forma asincrónica.

-   Cree una extensión como unión entre los espacios de nombres y los modelos de programación. Por ejemplo, un ISV invento un nuevo modelo de objetos para servicios de impresión. El objeto **printQueue** ya está definido en el directorio. El ISV puede crear una extensión ADSI y asociarla con el objeto **printQueue** . Los usuarios ADSI pueden enlazar a un objeto **printQueue** y empezar a usar el modelo de objetos para el ISV. Desde la perspectiva del cliente ADSI, este punto de Unión es transparente.
-   Cree una extensión para simplificar las tareas. Muchas tareas en el directorio se pueden realizar mediante la búsqueda y el establecimiento de varios atributos en un objeto o en varios objetos. Al crear una función única para manipular varios atributos, se simplifica el desarrollo para escritores de aplicaciones y scripts.

En el caso de los clientes ADSI, las extensiones enriquecen el entorno de programación ADSI de varias maneras:

-   Los desarrolladores que crean clientes ADSI no tienen que aprender un nuevo modelo de programación. Las extensiones forman parte de ADSI. Usarían el mismo paradigma para la búsqueda, la manipulación de datos y la protección de objetos.
-   Los administradores pueden administrar aplicaciones habilitadas para el uso de directorios con extensiones.
-   Los consumidores de extensión pueden ver un objeto ADSI y una extensión como un objeto integrado.
-   Los componentes existentes se pueden integrar con ADSI, lo que permite que las extensiones aprovechen las inversiones existentes y creen sinergias entre los componentes.

Las extensiones ADSI se diseñaron con los siguientes objetivos:

-   Fácil de implementar. Con las tecnologías actuales existentes de Microsoft, Microsoft Visual C++ sistema de desarrollo y el Active Template Library, se puede crear una extensión rápidamente.
-   Los clientes ven una IDispatch. Desde la perspectiva de los escritores de script y automatización, los métodos de extensión y las propiedades se combinan de manera transparente en un objeto ADSI.
-   Dependiente. Los escritores de extensiones pueden extender de forma independiente ADSI sin conocimiento previo de las extensiones existentes.

Considere este escenario: un desarrollador corporativo o un ISV deben desarrollar un programa de copia de seguridad. Esta aplicación de copia de seguridad permite a un administrador realizar una copia de seguridad de todos los equipos de una unidad organizativa. Con una extensión ADSI, es posible el siguiente script.


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



**LastBackUp** es una propiedad y **BackUpNow** es un método que proporciona el escritor de la extensión. El código muestra las ventajas para los consumidores de extensión y los proveedores. El escritor de la extensión no tiene que crear una nueva forma de filtrar, buscar y tener acceso al directorio. El consumidor de la extensión no tiene que reaprender un nuevo paradigma de programación. Los nuevos métodos y propiedades que proporciona el escritor de extensiones se ven como parte de ADSI.

 

 




