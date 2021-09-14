---
description: En el ejemplo autocompletar se muestra cómo implementar la función Autocompletar de caracteres en japonés mediante las interfaces de programación de aplicaciones (API) de reconocimiento.
ms.assetid: 237e33bc-3708-4128-8749-d3d031f7237a
title: Ejemplo de autocompletar de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4853cdef72a087aff3b9b726f0c83af9038ef5bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360339"
---
# <a name="character-autocomplete-sample"></a>Ejemplo de autocompletar de caracteres

En el ejemplo autocompletar se muestra cómo implementar la función Autocompletar de caracteres en japonés mediante las interfaces de programación de aplicaciones (API) de reconocimiento.

En este ejemplo se usan las siguientes características:

-   Uso de un *recopilador de entrada de lápiz*
-   Uso de un *contexto de reconocedor*

## <a name="initializing-the-ink-collector-and-recognizer-context"></a>Inicialización del recopilador de lápiz y el contexto del reconocedor

Los [**objetos InkCollector**](inkcollector-class.md) y [**InkRecognizerContext**](inkrecognizercontext-class.md) se declaran como clases que pueden generar eventos.


```C++
Dim WithEvents ic As InkCollector
Dim WithEvents rc As InkRecognizerContext
```



El controlador de eventos Load del formulario crea un recopilador de entrada de lápiz, asocia el recopilador de lápiz al cuadro de imagen y habilita la recopilación de lápiz. A continuación, el controlador de eventos carga el reconocedor japonés predeterminado e inicializa las propiedades Guide y Strokes del contexto del reconocedor.


```C++
Private Sub Form_Load()
   ' Set the ink collector to work in the small frame window
    Set ic = New InkCollector    ic.hWnd = fraBox.hWnd    ic.Enabled = True
    
    ' Get the Japanese recognizer
    LoadRecognizer

    ' Initialize the recognizer context
    Dim Guide As New InkRecognizerGuide
    Dim FrameRectangle As New InkRectangle
    Dim Top As Long
    Dim Bottom As Long
    Dim Left As Long
    Dim Right As Long
    Top = 0
    Left = 0
    Bottom = fraBox.ScaleHeight
    Right = fraBox.ScaleWidth
    ic.Renderer.PixelToInkSpace Me.hdc, Top, Left
    ic.Renderer.PixelToInkSpace Me.hdc, Bottom, Right
    FrameRectangle.Bottom = Bottom
    FrameRectangle.Top = Top
    FrameRectangle.Left = Left
    FrameRectangle.Right = Right
    Guide.Columns = 1
    Guide.Rows = 1
    Guide.Midline = -1 ' Do not use midline
    Guide.DrawnBox = FrameRectangle
    Guide.WritingBox = FrameRectangle
    Set rc.Guide = Guide
    
    ' Set the strokes collection on the recognizer context
    Set ink = ic.ink    Set rc.Strokes = ic.ink.Strokes
End Sub
```



## <a name="loading-the-default-japanese-recognizer"></a>Carga del reconocedor japonés predeterminado

Se [**llama al método GetDefaultRecognizer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-getdefaultrecognizer) de [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) para recuperar el reconocedor predeterminado para el idioma japonés. A continuación, se comprueba la propiedad [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) del objeto IInkRecognizer para determinar si el reconocedor admite el idioma japonés. Si es así, se usa el método [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) del reconocedor para generar un contexto de reconocedor para el formulario.


```C++
Private Sub LoadRecognizer()
    On Error GoTo NoRecognizer
    ' Get a Japanese recognizer context
    Dim recos As New InkRecognizers
    Dim JapaneseReco As IInkRecognizer
    Set JapaneseReco = recos.GetDefaultRecognizer(&H411)
    If JapaneseReco Is Nothing Then
        MsgBox "Japanese Recognizers are not installed on this system. Exiting."
        End
    End If
    
    ' Check that this is indeed a Japanese recognizer
    Dim IsJapanese As Boolean
    Dim lan As Integer
    IsJapanese = False
    For lan = LBound(JapaneseReco.Languages) To UBound(JapaneseReco.Languages)
        If JapaneseReco.Languages(lan) = &H411 Then
            IsJapanese = True
        End If
    Next lan
    If Not IsJapanese Then
        MsgBox "Japanese Recognizers are not installed on this system. Exiting."
        End
    End If
    Set rc = JapaneseReco.CreateRecognizerContext
    Exit Sub
NoRecognizer:
    MsgBox "Japanese Recognizers are not installed on this system. Exiting."
    End
End Sub
```



## <a name="handling-the-stroke-event"></a>Controlar el evento de trazo

El [**controlador de**](inkcollector-stroke.md) eventos Stroke detiene primero el reconocimiento en segundo plano en el contexto del reconocedor. A continuación, agrega el nuevo trazo a la propiedad [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del contexto del reconocedor. Por último, establece la propiedad [**InkRecognizerCharacterAutoCompletionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercharacterautocompletionmode) del contexto del reconocedor y llama al método [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) del reconocedor para cada uno de los tres modos de autocompletar de tres caracteres. El *parámetro CustomData* de la llamada al método **BackgroundRecognizeWithAlternates** se usa para identificar qué resultados de reconocimiento se devuelven en el [**evento RecognitionWithAlternates.**](inkrecognizercontext-recognitionwithalternates.md)


```C++
Private Sub ic_Stroke(ByVal Cursor As MSINKAUTLib.IInkCursor, ByVal Stroke As MSINKAUTLib.IInkStrokeDisp, Cancel As Boolean)

    ' Stop the unfinished recognition processes
    rc.StopBackgroundRecognition

    ' Add the new stroke
    rc.Strokes.Add Stroke

    ' Get a result for all three CAC modes
    rc.CharacterAutoCompletionMode = IRCACM_Full rc.BackgroundRecognizeWithAlternates 0 rc.CharacterAutoCompletionMode = IRCACM_Prefix rc.BackgroundRecognizeWithAlternates 1 rc.CharacterAutoCompletionMode = IRCACM_Random rc.BackgroundRecognizeWithAlternates 2
End Sub
```



## <a name="handling-the-recognition-with-alternates-event"></a>Controlar el evento de reconocimiento con alternativas

El controlador del evento [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) comprueba primero el *parámetro RecognitionStatus.* Si se produce un error en el reconocimiento, el controlador de eventos omite los resultados del reconocimiento. De lo contrario, el controlador de eventos agrega el *parámetro RecognitionResult* al cuadro de imagen adecuado y guarda la cadena de resultado. El *parámetro CustomData* se establece en la llamada al método [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) e identifica qué carácter usó el contexto del reconocedor.


```C++
Private Sub rc_RecognitionWithAlternates(ByVal RecognitionResult As MSINKAUTLib.IInkRecognitionResult, ByVal vCustomParam As Variant, ByVal RecognitionStatus As MSINKAUTLib.InkRecognitionStatus)
    ' Get the alternates from the recognition result
    ' and display them in the right place
    Dim ResultString As String
    Dim alts As IInkRecognitionAlternates
    Dim alt As IInkRecognitionAlternate
        
    On Error GoTo EndFunc

    If RecognitionStatus = IRS_NoError Then
        ' Fill a string with all the characters for this CAC mode
        Set alts = RecognitionResult.AlternatesFromSelection
        For Each alt In alts
            ResultString = ResultString + alt.String
        Next alt
        ' Display the string
        Dim r As RECT
        r.Left = 0
        r.Top = 0
        r.Right = 1000
        r.Bottom = 1000
        PctResult(vCustomParam).Cls
        DrawText PctResult(vCustomParam).hdc, StrPtr(ResultString), Len(ResultString), r, 0
        If vCustomParam = 0 Then
            FullCACText = ResultString
        Else
            If vCustomParam = 1 Then
                PrefixCACText = ResultString
            Else
                If vCustomParam = 2 Then
                    RandomCACText = ResultString
                End If
            End If
        End If
    End If
    Exit Sub
EndFunc:
    MsgBox Err.Description
End Sub
```



## <a name="painting-the-form"></a>Pintar el formulario

El Paint de eventos borra los cuadros de imagen de resultados y les agrega los resultados de reconocimiento guardados.

## <a name="deleting-the-strokes"></a>Eliminación de los trazos

El método del formulario `CmdClear_Click` controla el comando Clear. Si [**InkCollector**](inkcollector-class.md) está recopilando actualmente entrada de lápiz, se muestra un cuadro de mensaje y se omite el comando. De lo contrario, el controlador de eventos detiene el reconocimiento en segundo plano, borra la propiedad [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del contexto del reconocedor y elimina los trazos del objeto [**InkDisp del**](inkdisp-class.md) formulario. A continuación, el controlador de eventos vuelve a dibujar el cuadro de imagen al que está asociado el recopilador de lápiz y borra las cadenas de reconocimiento y los cuadros de imagen.


```C++
If Not (ic.CollectingInk) Then

    ' Stop the unfinished recognition processes
    rc.StopBackgroundRecognition

    ' ...
    Set rc.Strokes = Nothing

    ' Delete all the strokes from the ink object
    ic.Ink.DeleteStrokes strokesToDelete

    ' Refresh the window
    fraBox.Refresh

    ' refresh the recognizer context
    Set rc.Strokes = ic.Ink.Strokes

    ' Clear the result strings
    FullCACText = ""
    PrefixCACText = ""
    RandomCACText = ""

    ' Clear the result windows
    PctResult(0).Cls
    PctResult(1).Cls
    PctResult(2).Cls

Else
    MsgBox "Cannot clear ink while the ink collector is busy."
End If
```



 

 
