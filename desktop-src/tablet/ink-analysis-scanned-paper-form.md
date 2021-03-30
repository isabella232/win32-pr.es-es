---
description: En este ejemplo se muestra cómo utilizar el análisis de tinta para crear una aplicación de rellenado de formularios, donde el formulario se basa en un papel digitalizado.
ms.assetid: 1eae5962-b4e0-4947-a6d2-63713a68198c
title: Formulario de papel digitalizado de análisis de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94d366c77e19bd5c32d3d1e4efa286cb3b089ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275229"
---
# <a name="ink-analysis-scanned-paper-form"></a><span data-ttu-id="21dc5-103">Formulario de papel digitalizado de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="21dc5-103">Ink Analysis Scanned Paper Form</span></span>

<span data-ttu-id="21dc5-104">En este ejemplo se muestra cómo utilizar el análisis de tinta para crear una aplicación de rellenado de formularios, donde el formulario se basa en un papel digitalizado.</span><span class="sxs-lookup"><span data-stu-id="21dc5-104">This sample shows how to use Ink Analysis to create a form-filling application, where the form is based on a scanned paper form.</span></span>

## <a name="features-demonstrated"></a><span data-ttu-id="21dc5-105">Características mostradas</span><span class="sxs-lookup"><span data-stu-id="21dc5-105">Features Demonstrated</span></span>

<span data-ttu-id="21dc5-106">Esta aplicación de ejemplo muestra las siguientes características de la API de análisis de tinta y los controles de entrada de lápiz de Windows Forms:</span><span class="sxs-lookup"><span data-stu-id="21dc5-106">This sample application demonstrates the following features of the Ink Analysis API and the Windows Forms Ink Controls:</span></span>

-   <span data-ttu-id="21dc5-107">Cargar un formulario de papel digitalizado.</span><span class="sxs-lookup"><span data-stu-id="21dc5-107">Loading a scanned paper form.</span></span> <span data-ttu-id="21dc5-108">En el ejemplo se importa el formulario a partir de una imagen en formato. png.</span><span class="sxs-lookup"><span data-stu-id="21dc5-108">The sample imports the form from an image in .png format.</span></span>
-   <span data-ttu-id="21dc5-109">Recopilación y representación de la entrada de lápiz en la parte superior del formulario digitalizado.</span><span class="sxs-lookup"><span data-stu-id="21dc5-109">Collecting and rendering ink on top of the scanned form.</span></span>
-   <span data-ttu-id="21dc5-110">Usar un objeto [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) para analizar la escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="21dc5-110">Using an [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) object to parse handwriting.</span></span>
-   <span data-ttu-id="21dc5-111">Generar objetos [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) para mejorar los resultados de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="21dc5-111">Generating [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) objects to improve handwriting results.</span></span>
-   <span data-ttu-id="21dc5-112">Rellenar cuadros de texto a partir de sugerencias de análisis.</span><span class="sxs-lookup"><span data-stu-id="21dc5-112">Populating text boxes from analysis hints.</span></span>
-   <span data-ttu-id="21dc5-113">Crear una experiencia de corrección de texto básica.</span><span class="sxs-lookup"><span data-stu-id="21dc5-113">Creating a basic text correction experience.</span></span>

## <a name="project-references"></a><span data-ttu-id="21dc5-114">Referencias del proyecto</span><span class="sxs-lookup"><span data-stu-id="21dc5-114">Project References</span></span>

<span data-ttu-id="21dc5-115">El ejemplo está disponible como una aplicación Windows Forms o Windows Presentation Foundation.</span><span class="sxs-lookup"><span data-stu-id="21dc5-115">The sample is available as a Windows Forms or Windows Presentation Foundation application.</span></span> <span data-ttu-id="21dc5-116">Las referencias a la versión Windows Forms:</span><span class="sxs-lookup"><span data-stu-id="21dc5-116">The Windows Forms version references:</span></span>

-   <span data-ttu-id="21dc5-117">Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="21dc5-117">Microsoft.Ink.dll</span></span>
-   <span data-ttu-id="21dc5-118">Microsoft.Ink.Analysis.dll</span><span class="sxs-lookup"><span data-stu-id="21dc5-118">Microsoft.Ink.Analysis.dll</span></span>

<span data-ttu-id="21dc5-119">La versión Windows Presentation Foundation hace referencia a IAWinFX.dll además de los archivos dll de Windows Presentation Foundation principales.</span><span class="sxs-lookup"><span data-stu-id="21dc5-119">The Windows Presentation Foundation version references IAWinFX.dll in addition to the core Windows Presentation Foundation dlls.</span></span>

> [!Note]  
> <span data-ttu-id="21dc5-120">La versión Windows Presentation Foundation de este ejemplo (que se encuentra en el directorio XAML) requiere que las extensiones de Windows Presentation Foundation para Microsoft Visual Studio 2005 estén instaladas en el sistema.</span><span class="sxs-lookup"><span data-stu-id="21dc5-120">The Windows Presentation Foundation version of this sample (found in the XAML directory) requires that the Windows Presentation Foundation extensions for Microsoft Visual Studio 2005 is installed on the system.</span></span>

 

## <a name="user-interface"></a><span data-ttu-id="21dc5-121">Interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="21dc5-121">User Interface</span></span>

<span data-ttu-id="21dc5-122">La interfaz de usuario de esta aplicación está formada por un [TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) con dos objetos [TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) asociados: formulario de entrada de lápiz y formato de texto convertido.</span><span class="sxs-lookup"><span data-stu-id="21dc5-122">The UI for this application consists of a [TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) with two [TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) objects associated with it: Ink Form and Converted Text Form.</span></span> <span data-ttu-id="21dc5-123">La pestaña formulario de entrada de lápiz contiene</span><span class="sxs-lookup"><span data-stu-id="21dc5-123">The Ink Form tab contains</span></span>

-   <span data-ttu-id="21dc5-124">Un panel que contiene una imagen de un formulario de papel digitalizado que se usa para realizar mensajes de teléfono.</span><span class="sxs-lookup"><span data-stu-id="21dc5-124">A panel that contains an image of a scanned paper form used for taking telephone messages.</span></span>
-   <span data-ttu-id="21dc5-125">Una casilla que tiene la aplicación muestra los límites de la sugerencia de análisis cuando está seleccionada.</span><span class="sxs-lookup"><span data-stu-id="21dc5-125">A check box that has the application show the analysis hint bounds when selected.</span></span>
-   <span data-ttu-id="21dc5-126">Un par de botones, borrar y analizar, que borran la tinta del formulario e inicializan el análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="21dc5-126">A pair of buttons, Clear and Analyze, that clear the ink from the form and initialize ink analysis.</span></span>

<span data-ttu-id="21dc5-127">El formato de texto convertido contiene la misma imagen y es la página en la que la aplicación muestra el texto reconocido.</span><span class="sxs-lookup"><span data-stu-id="21dc5-127">The Converted Text Form contains the same image and is the page on which the application displays the recognized text.</span></span> <span data-ttu-id="21dc5-128">Al hacer clic en analizar, la aplicación realiza el análisis de tinta sincrónicamente y los resultados del reconocimiento aparecen en la pestaña formulario de texto convertido.</span><span class="sxs-lookup"><span data-stu-id="21dc5-128">When you click Analyze, the application performs ink analysis synchronously, and the recognition results appear on the Converted Text Form tab.</span></span>

## <a name="functionality"></a><span data-ttu-id="21dc5-129">Funcionalidad</span><span class="sxs-lookup"><span data-stu-id="21dc5-129">Functionality</span></span>

<span data-ttu-id="21dc5-130">Esta aplicación utiliza un [InkOverlay](/previous-versions/ms552322(v=vs.100)) para habilitar la escritura.</span><span class="sxs-lookup"><span data-stu-id="21dc5-130">This application uses an [InkOverlay](/previous-versions/ms552322(v=vs.100)) to enable writing.</span></span> <span data-ttu-id="21dc5-131">El objeto InkOverlay es idóneo para tomar notas y scribbling básicas.</span><span class="sxs-lookup"><span data-stu-id="21dc5-131">The InkOverlay object is well suited for note taking and basic scribbling.</span></span> <span data-ttu-id="21dc5-132">El uso previsto principal de este objeto es mostrar la entrada de lápiz como entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="21dc5-132">The primary intended use of this object is to display ink as ink.</span></span> <span data-ttu-id="21dc5-133">La clase principal para el análisis de tinta es la clase [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="21dc5-133">The main class for ink analysis is the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) class.</span></span> <span data-ttu-id="21dc5-134">Cuando se llama al método [Analyze](/previous-versions/ms568971(v=vs.100)) del objeto InkAnalyzer, el análisis de tinta se produce sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="21dc5-134">When you call the InkAnalyzer object's [Analyze](/previous-versions/ms568971(v=vs.100)) method, the ink analysis occurs synchronously.</span></span>

<span data-ttu-id="21dc5-135">La aplicación inicializa dos matrices, una de las cadenas y uno de rectángulos.</span><span class="sxs-lookup"><span data-stu-id="21dc5-135">The application initializes two arrays, one of strings and one of rectangles.</span></span> <span data-ttu-id="21dc5-136">La matriz de cadena, `factoidStrings` , se compone de objetos [Factoid](/previous-versions/ms583657(v=vs.100)) que se pasan a [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) como objetos [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="21dc5-136">The string array, `factoidStrings`, is made of [Factoid](/previous-versions/ms583657(v=vs.100)) objects that are passed into the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) as [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) objects.</span></span> <span data-ttu-id="21dc5-137">Los objetos AnalysisHintNode sesgan el InkAnalyzer de entrada en particular.</span><span class="sxs-lookup"><span data-stu-id="21dc5-137">The AnalysisHintNode objects bias the InkAnalyzer toward particular input.</span></span> <span data-ttu-id="21dc5-138">En este ejemplo se usan las sugerencias de fecha, hora y teléfono, así como otras.</span><span class="sxs-lookup"><span data-stu-id="21dc5-138">This sample uses the date, time, and telephone hints, as well as some others.</span></span>

<span data-ttu-id="21dc5-139">Cada [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) está asociado a un área específica del formulario.</span><span class="sxs-lookup"><span data-stu-id="21dc5-139">Each [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) is associated with a specific area of the form.</span></span> <span data-ttu-id="21dc5-140">La matriz de rectángulos representa las áreas `rects` .</span><span class="sxs-lookup"><span data-stu-id="21dc5-140">The areas are represented by the array of rectangles, `rects`.</span></span> <span data-ttu-id="21dc5-141">Al crear un [cuadro](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) de texto para cada rectángulo, el ejemplo genera el texto reconocido en la ubicación correcta.</span><span class="sxs-lookup"><span data-stu-id="21dc5-141">By creating a [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) for each rectangle, the sample outputs the recognized text in the correct location.</span></span>


```C++
        private void InitHints()
        {
            // Instantiate the collection of TextBoxes.
            this.textBoxes = new ArrayList();

            // For each Rectangle in Rectangles
            for (int i = 0; i < rects.Length; i++)
            {

                Rectangle rectangle = rects[i];

                // Create an AnalysisHintNode with the bounds of the Rectangle.  The bounds
                // of an AnalysisHintNode gives clues to the handwriting recognizer about
                // the way Strokes are grouped together.
                AnalysisHintNode hint = this.analyzer.CreateAnalysisHint(rectangle);

                // Set the corresponding Factoid on the AnalysisHintNode.  This gives the 
                // recognizer clues about the meaning of the strokes within the 
                // AnalysisHintNode's region.
                hint.Factoid = factoidStrings[i];

                // Create a corresponding TextBox where the results of the analysis
                // associated with this AnalysisHintNode will be displayed.  Store the reference
                // to the TextBox in the textBoxes Collection.
                this.textBoxes.Add(InitTextBox(hint));
            }
        }
```



<span data-ttu-id="21dc5-142">Después, es simplemente cuestión de crear un controlador de eventos que desencadene el análisis de tinta cuando el usuario haga clic en analizar.</span><span class="sxs-lookup"><span data-stu-id="21dc5-142">After that, it is merely a matter of creating an event handler that triggers the ink analysis when the user clicks Analyze.</span></span>


```C++
        private void UpdateTextBoxes()
        {
            // Get the AnalysisHintNodes that we previously added to the InkAnalyzer.
            ContextNodeCollection hints = this.analyzer.GetAnalysisHints();

            for (int i = 0; i < hints.Count; i++)
            {
                // Get the recognized string from the AnalysisHintNode
                string analyzedString = ((AnalysisHintNode)hints[i]).GetRecognizedString();

                // If we found a string, set the contents of the TextBox
                // to that string.
                if (analyzedString != null)
                {
                    ((TextBox)this.textBoxes[i]).Text = analyzedString;
                }
            }
        }
```



 

 
