---
description: Esta aplicación se basa en el objeto InkCollector y muestra la colección de entradas de lápiz.
ms.assetid: e799fb16-5a1e-4d57-a033-554f72e2e685
title: Ejemplo de colección de entradas manuscritas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f31ce83a55b6f352d76ad1cb8d184b41618c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154185"
---
# <a name="ink-collection-sample"></a>Ejemplo de colección de entradas manuscritas

Esta aplicación se basa en el objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) y muestra la colección de entradas de lápiz. La aplicación crea una ventana, le adjunta un objeto InkCollector y proporciona al usuario opciones de menú que se pueden usar para cambiar el color de la tinta, el ancho de la tinta y habilitar y deshabilitar la recopilación de entradas manuscritas.

> [!Note]  
> La versión que se describe en esta sección es Visual Basic .NET. Los conceptos son los mismos entre las versiones de otros lenguajes de la biblioteca de ejemplos.

 

## <a name="declaring-the-inkcollector"></a>Declarar InkCollector

En primer lugar, la aplicación importa el espacio de nombres [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) . A continuación, la aplicación declara `myInkCollector` , que contiene el objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) del formulario.


```C++
' The Ink namespace, which contains the Tablet PC Platform APIImports Microsoft.Ink
...
Public Class InkCollection
   Inherits Form
    ' Declare the Ink Collector object
    Private myInkCollector
```



## <a name="setting-things-up"></a>Configuración de elementos

El método del formulario `InkCollection_Load` controla el evento de [carga](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del formulario. Crea un objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) asignado al formulario modifica la propiedad [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) del objeto InkCollector y habilita el objeto InkCollector.


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



[InkCollector](/previous-versions/ms836493(v=msdn.10)) se asigna a la ventana del formulario mediante la asignación del identificador de ventana del formulario a la propiedad [Handle](/previous-versions/ms836504(v=msdn.10)) del objeto InkCollector. La colección de tintas se activa estableciendo la propiedad [Enabled](/previous-versions/ms836503(v=msdn.10)) del objeto InkCollector en **true**.

La propiedad [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) del objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) establece los atributos predeterminados que se asignan a un nuevo cursor. Para establecer atributos diferentes en un nuevo cursor, utilice la propiedad [DrawingAttributes](/previous-versions/ms839523(v=msdn.10)) del objeto [cursor](/previous-versions/ms839521(v=msdn.10)) . Para cambiar los atributos de dibujo de un solo trazo, use la propiedad [DrawingAttributes](/previous-versions/ms827846(v=msdn.10)) del objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) .

## <a name="changing-the-properties"></a>Cambiar las propiedades

El resto de esta aplicación simple consta de controladores para las diversas selecciones de menú que el usuario puede realizar. Por ejemplo, cuando el usuario elige cambiar el color de la tinta a rojo seleccionando rojo en el menú de entrada manuscrita, el color cambia mediante la propiedad [color](/previous-versions/ms837933(v=msdn.10)) de la propiedad [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) del objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) en el controlador de eventos del menú.


```C++
Private Sub miRed_Click(ByVal sender As System.Object, 
                        ByVal e As System.EventArgs) Handles miRed.Click
    myInkCollector.DefaultDrawingAttributes.Color = Color.Red
End Sub
```



## <a name="closing-the-form"></a>Cierre del formulario

El método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del formulario desecha el objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) , `myInkCollector` .

 

 
