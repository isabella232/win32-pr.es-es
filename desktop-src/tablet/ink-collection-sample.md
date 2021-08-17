---
description: Esta aplicación se basa en el objeto InkCollector y muestra la colección de entrada de lápiz.
ms.assetid: e799fb16-5a1e-4d57-a033-554f72e2e685
title: Ejemplo de colección de entrada de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5f568abf38abfa31d9374a7a1874f9f73481a799a740c402f3e8f168963c3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718264"
---
# <a name="ink-collection-sample"></a>Ejemplo de colección de entrada de lápiz

Esta aplicación se basa en el [objeto InkCollector](/previous-versions/ms836493(v=msdn.10)) y muestra la colección de entrada de lápiz. La aplicación crea una ventana, adjunta un objeto InkCollector y proporciona al usuario opciones de menú que se pueden usar para cambiar el color de la entrada de lápiz, el ancho de la entrada de lápiz y habilitar y deshabilitar la colección de entrada de lápiz.

> [!Note]  
> La versión que se describe en esta sección es Visual Basic .NET. Los conceptos son los mismos entre otras versiones de lenguaje de la biblioteca de ejemplos.

 

## <a name="declaring-the-inkcollector"></a>Declaración de InkCollector

La aplicación importa primero el espacio [de nombres Microsoft.Ink.](/previous-versions/ms826516(v=msdn.10)) A continuación, la aplicación declara `myInkCollector` , que contiene el objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) para el formulario.


```C++
' The Ink namespace, which contains the Tablet PC Platform APIImports Microsoft.Ink
...
Public Class InkCollection
   Inherits Form
    ' Declare the Ink Collector object
    Private myInkCollector
```



## <a name="setting-things-up"></a>Configuración de las cosas

El método del `InkCollection_Load` formulario controla el evento Load [del](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) formulario. Crea un [objeto InkCollector](/previous-versions/ms836493(v=msdn.10)) asignado al formulario que modifica la propiedad [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) del objeto InkCollector y habilita el objeto InkCollector.


```C++
Private Sub InkCollection_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load

    ' Create an ink collector and assign it to this form's window
    myInkCollector = New InkCollector(Me.Handle)

    ' Set the pen width to be a medium width
    myInkCollector.DefaultDrawingAttributes.Width = MediumInkWidth

    ' If you do not modify the default drawing attributes, the default 
    ' drawing attributes will use the following properties and values:
    ' ...

    ' Turn the ink collector on
    myInkCollector.Enabled = True
End Sub
```



[InkCollector se](/previous-versions/ms836493(v=msdn.10)) asigna a la ventana del formulario mediante la asignación del identificador de ventana del formulario a la propiedad Handle del [objeto](/previous-versions/ms836504(v=msdn.10)) InkCollector. La colección ink se activa estableciendo la propiedad [Enabled](/previous-versions/ms836503(v=msdn.10)) del objeto InkCollector en **TRUE.**

La propiedad [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) del objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) establece los atributos predeterminados que se asignan a un nuevo cursor. Para establecer atributos diferentes en un nuevo cursor, use la [propiedad DrawingAttributes](/previous-versions/ms839523(v=msdn.10)) del [objeto Cursor.](/previous-versions/ms839521(v=msdn.10)) Para cambiar los atributos de dibujo de un solo trazo, use la [propiedad DrawingAttributes](/previous-versions/ms827846(v=msdn.10)) del [objeto Stroke.](/previous-versions/ms827842(v=msdn.10))

## <a name="changing-the-properties"></a>Cambiar las propiedades

El resto de esta sencilla aplicación consta de controladores para las distintas selecciones de menú que el usuario puede realizar. Por ejemplo, cuando el usuario elige cambiar el color de la entrada de lápiz a rojo seleccionando Rojo en el menú Entrada manuscrita, el color cambia mediante la propiedad [Color](/previous-versions/ms837933(v=msdn.10)) de la propiedad [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) del objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) en el controlador de eventos del menú.


```C++
Private Sub miRed_Click(ByVal sender As System.Object, 
                        ByVal e As System.EventArgs) Handles miRed.Click
    myInkCollector.DefaultDrawingAttributes.Color = Color.Red
End Sub
```



## <a name="closing-the-form"></a>Cerrar el formulario

El método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del formulario elimina el [objeto InkCollector,](/previous-versions/ms836493(v=msdn.10)) `myInkCollector` .

 

 
