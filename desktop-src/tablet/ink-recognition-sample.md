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
# <a name="ink-recognition-sample"></a><span data-ttu-id="614f0-103">Ejemplo de reconocimiento de tinta</span><span class="sxs-lookup"><span data-stu-id="614f0-103">Ink Recognition Sample</span></span>

<span data-ttu-id="614f0-104">Esta aplicación muestra cómo puede compilar una aplicación de reconocimiento de escritura a mano. El SDK de Windows Vista proporciona versiones de este ejemplo en C \# y Visual Basic .net.</span><span class="sxs-lookup"><span data-stu-id="614f0-104">This application demonstrates how you can build a handwriting recognition application.The Windows Vista SDK provides versions of this sample in C\# and Visual Basic .NET, as well.</span></span> <span data-ttu-id="614f0-105">En este tema se hace referencia al ejemplo Visual Basic .NET, pero los conceptos son los mismos entre las distintas versiones.</span><span class="sxs-lookup"><span data-stu-id="614f0-105">This topic refers to the Visual Basic .NET sample, but the concepts are the same between versions.</span></span>

## <a name="access-the-tablet-pc-interfaces"></a><span data-ttu-id="614f0-106">Acceder a las interfaces de Tablet PC</span><span class="sxs-lookup"><span data-stu-id="614f0-106">Access the Tablet PC Interfaces</span></span>

<span data-ttu-id="614f0-107">En primer lugar, haga referencia a la API de Tablet PC, que se instala con el SDK.</span><span class="sxs-lookup"><span data-stu-id="614f0-107">First, reference the Tablet PC API, which are installed with the SDK.</span></span>


```VB
' The Ink namespace, which contains the Tablet PC Platform API
Imports Microsoft.Ink
```



## <a name="initialize-the-inkcollector"></a><span data-ttu-id="614f0-108">Inicializar InkCollector</span><span class="sxs-lookup"><span data-stu-id="614f0-108">Initialize the InkCollector</span></span>

<span data-ttu-id="614f0-109">En el ejemplo se agrega código al controlador de eventos de [carga](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del formulario que sirve para asociar [InkCollector](/previous-versions/ms583683(v=vs.100)), myInkCollector, a la ventana de cuadro de grupo y habilitar InkCollector.</span><span class="sxs-lookup"><span data-stu-id="614f0-109">The sample adds code to the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler that serves to associate the [InkCollector](/previous-versions/ms583683(v=vs.100)), myInkCollector, with the group box window and enable the InkCollector.</span></span>


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



## <a name="recognize-the-strokes"></a><span data-ttu-id="614f0-110">Reconocer los trazos</span><span class="sxs-lookup"><span data-stu-id="614f0-110">Recognize the Strokes</span></span>

<span data-ttu-id="614f0-111">El controlador de eventos [click](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) del objeto de [botón](/dotnet/api/system.windows.forms.button?view=netcore-3.1) comprueba para asegurarse de que el usuario tiene al menos un reconocedor instalado mediante el examen de la propiedad [Count](/previous-versions/ms828521(v=msdn.10)) de la colección [reconocedores](/previous-versions/ms828520(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="614f0-111">The [Button](/dotnet/api/system.windows.forms.button?view=netcore-3.1) object's [Click](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) event handler checks to ensure that the user has at least one recognizer installed by examining the [Count](/previous-versions/ms828521(v=msdn.10)) property of the [Recognizers](/previous-versions/ms828520(v=msdn.10)) collection.</span></span>

<span data-ttu-id="614f0-112">La propiedad [SelectedText](/previous-versions/windows/) del cuadro de texto se establece en la mejor coincidencia para los trazos mediante el método [ToString](/previous-versions/ms827836(v=msdn.10)) en la colección [Strokes](/previous-versions/ms552701(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="614f0-112">The [SelectedText](/previous-versions/windows/) property of the text box is set to the best match for the strokes using the [ToString](/previous-versions/ms827836(v=msdn.10)) method on the [Strokes](/previous-versions/ms552701(v=vs.100)) collection.</span></span> <span data-ttu-id="614f0-113">Una vez reconocidos los trazos, se eliminan.</span><span class="sxs-lookup"><span data-stu-id="614f0-113">After the strokes have been recognized, they are deleted.</span></span> <span data-ttu-id="614f0-114">Por último, el código fuerza el redibujo del área de dibujo y lo borra para su uso posterior de la tinta.</span><span class="sxs-lookup"><span data-stu-id="614f0-114">Finally, the code forces drawing area repaint, clearing it for further ink use.</span></span>


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



## <a name="closing-the-form"></a><span data-ttu-id="614f0-115">Cierre del formulario</span><span class="sxs-lookup"><span data-stu-id="614f0-115">Closing the Form</span></span>

<span data-ttu-id="614f0-116">El método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del formulario desecha el objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="614f0-116">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>

 

 
