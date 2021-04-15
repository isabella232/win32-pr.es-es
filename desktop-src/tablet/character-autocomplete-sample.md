---
description: En el ejemplo de autocompletar se muestra cómo implementar la función autocompletar de caracteres en japonés mediante las interfaces de programación de aplicaciones (API) de reconocimiento.
ms.assetid: 237e33bc-3708-4128-8749-d3d031f7237a
title: Ejemplo de autocompletar caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4853cdef72a087aff3b9b726f0c83af9038ef5bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539453"
---
# <a name="character-autocomplete-sample"></a><span data-ttu-id="97670-103">Ejemplo de autocompletar caracteres</span><span class="sxs-lookup"><span data-stu-id="97670-103">Character Autocomplete Sample</span></span>

<span data-ttu-id="97670-104">En el ejemplo de autocompletar se muestra cómo implementar la función autocompletar de caracteres en japonés mediante las interfaces de programación de aplicaciones (API) de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="97670-104">The Autocomplete sample demonstrates how to implement character Autocomplete in Japanese by using the recognition application programming interfaces (APIs).</span></span>

<span data-ttu-id="97670-105">En este ejemplo se usan las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="97670-105">The following features are used in this sample:</span></span>

-   <span data-ttu-id="97670-106">Usar un *recolector de tinta*</span><span class="sxs-lookup"><span data-stu-id="97670-106">Using an *ink collector*</span></span>
-   <span data-ttu-id="97670-107">Usar un *contexto de reconocedor*</span><span class="sxs-lookup"><span data-stu-id="97670-107">Using a *recognizer context*</span></span>

## <a name="initializing-the-ink-collector-and-recognizer-context"></a><span data-ttu-id="97670-108">Inicializar el recopilador de tinta y el contexto del reconocedor</span><span class="sxs-lookup"><span data-stu-id="97670-108">Initializing the Ink Collector and Recognizer Context</span></span>

<span data-ttu-id="97670-109">Los objetos [**InkCollector**](inkcollector-class.md) y [**InkRecognizerContext**](inkrecognizercontext-class.md) se declaran como clases que pueden generar eventos.</span><span class="sxs-lookup"><span data-stu-id="97670-109">The [**InkCollector**](inkcollector-class.md) and [**InkRecognizerContext**](inkrecognizercontext-class.md) objects are declared as classes that can raise events.</span></span>


```C++
Dim WithEvents ic As InkCollector
Dim WithEvents rc As InkRecognizerContext
```



<span data-ttu-id="97670-110">El controlador de eventos de carga del formulario crea un recolector de tinta, asocia el recopilador de tinta al cuadro de imagen y habilita la recopilación de entradas de lápiz.</span><span class="sxs-lookup"><span data-stu-id="97670-110">The form's Load event handler creates an ink collector, associates the ink collector to picture box, and enables ink collection.</span></span> <span data-ttu-id="97670-111">A continuación, el controlador de eventos carga el reconocedor japonés predeterminado e inicializa las propiedades de trazo y guía del contexto del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="97670-111">The event handler then loads the default Japanese recognizer, and initializes the recognizer context 's Guide and Strokes properties.</span></span>


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



## <a name="loading-the-default-japanese-recognizer"></a><span data-ttu-id="97670-112">Carga del reconocedor japonés predeterminado</span><span class="sxs-lookup"><span data-stu-id="97670-112">Loading the Default Japanese Recognizer</span></span>

<span data-ttu-id="97670-113">Se llama al método [**GetDefaultRecognizer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-getdefaultrecognizer) de [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) para recuperar el reconocedor predeterminado del idioma japonés.</span><span class="sxs-lookup"><span data-stu-id="97670-113">The [**GetDefaultRecognizer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-getdefaultrecognizer) method of the [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) is called to retrieve the default recognizer for the Japanese language.</span></span> <span data-ttu-id="97670-114">A continuación, se comprueba la propiedad [**idiomas**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) del objeto IInkRecognizer para determinar si el reconocedor admite el idioma japonés.</span><span class="sxs-lookup"><span data-stu-id="97670-114">Next, the IInkRecognizer object's [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) property is checked to determine if the recognizer supports the Japanese language.</span></span> <span data-ttu-id="97670-115">Si es así, el método [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) del reconocedor se usa para generar un contexto de reconocedor para el formulario.</span><span class="sxs-lookup"><span data-stu-id="97670-115">If it does, then the recognizer's [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) method is used to generate a recognizer context for the form.</span></span>


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



## <a name="handling-the-stroke-event"></a><span data-ttu-id="97670-116">Controlar el evento stroke</span><span class="sxs-lookup"><span data-stu-id="97670-116">Handling the Stroke Event</span></span>

<span data-ttu-id="97670-117">El controlador de eventos [**Stroke**](inkcollector-stroke.md) detiene primero el reconocimiento en segundo plano en el contexto del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="97670-117">The [**Stroke**](inkcollector-stroke.md) event handler first halts background recognition on the recognizer context.</span></span> <span data-ttu-id="97670-118">A continuación, agrega el nuevo trazo a la propiedad [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del contexto del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="97670-118">Then, it adds the new stroke to the recognizer context's [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property.</span></span> <span data-ttu-id="97670-119">Por último, establece la propiedad [**InkRecognizerCharacterAutoCompletionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercharacterautocompletionmode) del contexto del reconocedor y llama al método [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) del contexto del reconocedor para cada uno de los tres modos de autocompletar de caracteres.</span><span class="sxs-lookup"><span data-stu-id="97670-119">Finally, it sets the recognizer context's [**InkRecognizerCharacterAutoCompletionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercharacterautocompletionmode) property and calls the recognizer context's [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) method for each of the three character Autocomplete modes.</span></span> <span data-ttu-id="97670-120">El parámetro *CustomData* de la llamada al método **BackgroundRecognizeWithAlternates** se usa para identificar los resultados del reconocimiento que se devuelven en el evento [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="97670-120">The *CustomData* parameter of the **BackgroundRecognizeWithAlternates** method call is used to identify which recognition results are returned in the [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) event.</span></span>


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



## <a name="handling-the-recognition-with-alternates-event"></a><span data-ttu-id="97670-121">Controlar el evento de reconocimiento con alternativas</span><span class="sxs-lookup"><span data-stu-id="97670-121">Handling the Recognition with Alternates Event</span></span>

<span data-ttu-id="97670-122">El controlador del evento [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) comprueba primero el parámetro *RecognitionStatus* .</span><span class="sxs-lookup"><span data-stu-id="97670-122">The handler for the [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) event first checks the *RecognitionStatus* parameter.</span></span> <span data-ttu-id="97670-123">Si hay un error en el reconocimiento, el controlador de eventos omite los resultados del reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="97670-123">If there is an error in recognition, the event handler ignores the recognition results.</span></span> <span data-ttu-id="97670-124">De lo contrario, el controlador de eventos agrega el parámetro *RecognitionResult* al cuadro de imagen adecuado y guarda la cadena de resultado.</span><span class="sxs-lookup"><span data-stu-id="97670-124">Otherwise, the event handler adds the *RecognitionResult* parameter to the appropriate picture box and saves the result string.</span></span> <span data-ttu-id="97670-125">El parámetro *CustomData* se establece en la llamada al método [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) e identifica el modo de autocompletar de caracteres utilizado por el contexto del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="97670-125">The *CustomData* parameter is set in the call to the [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) method and identifies which character Autocomplete mode was used by the recognizer context.</span></span>


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



## <a name="painting-the-form"></a><span data-ttu-id="97670-126">Dibujo del formulario</span><span class="sxs-lookup"><span data-stu-id="97670-126">Painting the Form</span></span>

<span data-ttu-id="97670-127">El controlador de eventos Paint borra los cuadros de imagen de resultados y agrega los resultados de reconocimiento guardados a ellos.</span><span class="sxs-lookup"><span data-stu-id="97670-127">The Paint event handler clears the results picture boxes and adds the saved recognition results to them.</span></span>

## <a name="deleting-the-strokes"></a><span data-ttu-id="97670-128">Eliminar los trazos</span><span class="sxs-lookup"><span data-stu-id="97670-128">Deleting the Strokes</span></span>

<span data-ttu-id="97670-129">El método del formulario `CmdClear_Click` controla el comando CLEAR.</span><span class="sxs-lookup"><span data-stu-id="97670-129">The form's `CmdClear_Click` method handles the Clear command.</span></span> <span data-ttu-id="97670-130">Si [**InkCollector**](inkcollector-class.md) está recopilando actualmente la entrada de lápiz, se muestra un cuadro de mensaje y se omite el comando.</span><span class="sxs-lookup"><span data-stu-id="97670-130">If the [**InkCollector**](inkcollector-class.md) is currently collecting ink, then a message box is displayed and the command is ignored.</span></span> <span data-ttu-id="97670-131">De lo contrario, el controlador de eventos detiene el reconocimiento en segundo plano, borra la propiedad [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del contexto del reconocedor y elimina los trazos del objeto [**InkDisp**](inkdisp-class.md) del formulario.</span><span class="sxs-lookup"><span data-stu-id="97670-131">Otherwise, the event handler stops background recognition, clears the [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property of the recognizer context, and deletes the strokes from the form's [**InkDisp**](inkdisp-class.md) object.</span></span> <span data-ttu-id="97670-132">A continuación, el controlador de eventos vuelve a dibujar el cuadro de imagen al que está asociado el recopilador de tinta y borra las cadenas de reconocimiento y los cuadros de imagen.</span><span class="sxs-lookup"><span data-stu-id="97670-132">Then, the event handler redraws the picture box to which the ink collector is associated, and clears the recognition strings and picture boxes.</span></span>


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



 

 
