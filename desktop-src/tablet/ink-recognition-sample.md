---
description: Esta aplicación muestra cómo puede crear una aplicación de reconocimiento de escritura a mano. El SDK Windows Vista proporciona también versiones de este ejemplo en C \# y Visual Basic .NET.
ms.assetid: 4b3fc078-731e-4263-8e95-2c273d69a457
title: Ejemplo de reconocimiento de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d97d9d15ef64a3d7a1fe1fc5d45b3cb0454ba7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359654"
---
# <a name="ink-recognition-sample"></a>Ejemplo de reconocimiento de lápiz

Esta aplicación muestra cómo puede crear una aplicación de reconocimiento de escritura a mano. El SDK Windows Vista proporciona también versiones de este ejemplo en C \# y Visual Basic .NET. En este tema se hace referencia Visual Basic ejemplo de .NET, pero los conceptos son los mismos entre versiones.

## <a name="access-the-tablet-pc-interfaces"></a>Acceso a las interfaces de Tablet PC

En primer lugar, haga referencia a la API de Tablet PC, que se instala con el SDK.


```VB
' The Ink namespace, which contains the Tablet PC Platform API
Imports Microsoft.Ink
```



## <a name="initialize-the-inkcollector"></a>Inicialización de InkCollector

El ejemplo agrega código al controlador de eventos [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del formulario que sirve para asociar [InkCollector](/previous-versions/ms583683(v=vs.100)), myInkCollector, con la ventana del cuadro de grupo y habilitar InkCollector.


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



## <a name="recognize-the-strokes"></a>Reconocimiento de los trazos

El [controlador de](/dotnet/api/system.windows.forms.button?view=netcore-3.1) eventos Click del objeto [Button](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) comprueba que el usuario tiene al menos un reconocedor instalado mediante el examen de la propiedad [Count](/previous-versions/ms828521(v=msdn.10)) de la [colección Recognizers.](/previous-versions/ms828520(v=msdn.10))

La [propiedad SelectedText](/previous-versions/windows/) del cuadro de texto se establece en la mejor coincidencia para los trazos mediante el [método ToString](/previous-versions/ms827836(v=msdn.10)) de la [colección Strokes.](/previous-versions/ms552701(v=vs.100)) Una vez que se han reconocido los trazos, se eliminan. Por último, el código fuerza el repintado del área de dibujo y la borra para su uso adicional con lápiz.


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



## <a name="closing-the-form"></a>Cerrar el formulario

El método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del formulario elimina el [objeto InkCollector.](/previous-versions/ms583683(v=vs.100))

 

 
