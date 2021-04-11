---
description: Esta aplicación muestra cómo puede compilar una aplicación de reconocimiento de escritura a mano. El SDK de Windows Vista proporciona versiones de este ejemplo en C \# y Visual Basic .net.
ms.assetid: 4b3fc078-731e-4263-8e95-2c273d69a457
title: Ejemplo de reconocimiento de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d97d9d15ef64a3d7a1fe1fc5d45b3cb0454ba7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275362"
---
# <a name="ink-recognition-sample"></a>Ejemplo de reconocimiento de tinta

Esta aplicación muestra cómo puede compilar una aplicación de reconocimiento de escritura a mano. El SDK de Windows Vista proporciona versiones de este ejemplo en C \# y Visual Basic .net. En este tema se hace referencia al ejemplo Visual Basic .NET, pero los conceptos son los mismos entre las distintas versiones.

## <a name="access-the-tablet-pc-interfaces"></a>Acceder a las interfaces de Tablet PC

En primer lugar, haga referencia a la API de Tablet PC, que se instala con el SDK.


```VB
' The Ink namespace, which contains the Tablet PC Platform API
Imports Microsoft.Ink
```



## <a name="initialize-the-inkcollector"></a>Inicializar InkCollector

En el ejemplo se agrega código al controlador de eventos de [carga](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del formulario que sirve para asociar [InkCollector](/previous-versions/ms583683(v=vs.100)), myInkCollector, a la ventana de cuadro de grupo y habilitar InkCollector.


```VB
Private Sub InkRecognition_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load

   ' Create the recognizers collection
    myRecognizers = New Recognizers()

    ' Create an ink collector that uses the group box handle
    myInkCollector = New InkCollector(gbInkArea.Handle)

    ' Turn the ink collector on
    myInkCollector.Enabled = True

End Sub
```



## <a name="recognize-the-strokes"></a>Reconocer los trazos

El controlador de eventos [click](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) del objeto de [botón](/dotnet/api/system.windows.forms.button?view=netcore-3.1) comprueba para asegurarse de que el usuario tiene al menos un reconocedor instalado mediante el examen de la propiedad [Count](/previous-versions/ms828521(v=msdn.10)) de la colección [reconocedores](/previous-versions/ms828520(v=msdn.10)) .

La propiedad [SelectedText](/previous-versions/windows/) del cuadro de texto se establece en la mejor coincidencia para los trazos mediante el método [ToString](/previous-versions/ms827836(v=msdn.10)) en la colección [Strokes](/previous-versions/ms552701(v=vs.100)) . Una vez reconocidos los trazos, se eliminan. Por último, el código fuerza el redibujo del área de dibujo y lo borra para su uso posterior de la tinta.


```VB
Private Sub btnRecognize_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles btnRecognize.Click

    ' Check to ensure that the user has at least one recognizer installed
    ' Note that this is a preventive check - otherwise, an exception 
    ' occurs during recognition
    If 0 = myRecognizers.Count Then
        MessageBox.Show("There are no handwriting recognizers installed.  You need to have at least one in order to run this sample.")
    Else
        ' ...
        txtResults.SelectedText = myInkCollector.Ink.Strokes.ToString

        ' If the mouse is pressed, do not perform the recognition -
        ' this prevents deleting a stroke that is still being drawn
        If Not myInkCollector.CollectingInk Then

            ' Delete the ink from the ink collector
            myInkCollector.Ink.DeleteStrokes(myInkCollector.Ink.Strokes)

            ' Force the Frame to redraw (so the deleted ink goes away)
            gbInkArea.Refresh()

        End If
    End If
End Sub
```



## <a name="closing-the-form"></a>Cierre del formulario

El método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del formulario desecha el objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) .

 

 
