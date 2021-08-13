---
description: En este ejemplo se muestra cómo usar Análisis de entrada de lápiz para crear una aplicación de relleno de formularios, donde el formulario se basa en un formulario de papel digitalizado.
ms.assetid: 1eae5962-b4e0-4947-a6d2-63713a68198c
title: Formulario de papel digitalizado de análisis de entrada de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4069efd5ba8763e00e9b3170ffb0a39a4a70c4d66d07d3c8bf08bc3688f57ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718651"
---
# <a name="ink-analysis-scanned-paper-form"></a>Formulario de papel digitalizado de análisis de entrada de lápiz

En este ejemplo se muestra cómo usar Análisis de entrada de lápiz para crear una aplicación de relleno de formularios, donde el formulario se basa en un formulario de papel digitalizado.

## <a name="features-demonstrated"></a>Características demostradas

En esta aplicación de ejemplo se muestran las siguientes características de Ink Analysis API y Windows Forms Ink Controls:

-   Carga de un formulario de papel digitalizado. El ejemplo importa el formulario de una imagen en .png formato.
-   Recopilar y representar la entrada manuscrita sobre el formulario digitalizado.
-   Usar un [objeto InkAnalyzer](/previous-versions/ms583671(v=vs.100)) para analizar la escritura a mano.
-   Generar objetos [AnalysisHintNode para](/previous-versions/ms573018(v=vs.100)) mejorar los resultados de escritura a mano.
-   Rellenar cuadros de texto a partir de sugerencias de análisis.
-   Crear una experiencia básica de corrección de texto.

## <a name="project-references"></a>Referencias del proyecto

El ejemplo está disponible como una aplicación Windows Forms o Windows Presentation Foundation aplicación. La versión Windows Forms hace referencia a:

-   Microsoft.Ink.dll
-   Microsoft.Ink.Analysis.dll

La Windows Presentation Foundation hace referencia a IAWinFX.dll además de los archivos DLL Windows Presentation Foundation principales.

> [!Note]  
> La Windows Presentation Foundation de este ejemplo (que se encuentra en el directorio XAML) requiere que las extensiones de Windows Presentation Foundation para Microsoft Visual Studio 2005 se instalen en el sistema.

 

## <a name="user-interface"></a>Interfaz de usuario

La interfaz de usuario de esta aplicación consta de [un TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) con dos objetos [TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) asociados: Ink Form y Converted Text Form. La pestaña Formulario de entrada manuscrita contiene

-   Panel que contiene una imagen de un formulario de papel digitalizado que se usa para tomar mensajes telefónicos.
-   Una casilla que tiene la aplicación muestra los límites de la sugerencia de análisis cuando se selecciona.
-   Un par de botones, Borrar y Analizar, que borran la entrada de lápiz del formulario e inicializan el análisis de entrada de lápiz.

El formulario de texto convertido contiene la misma imagen y es la página en la que la aplicación muestra el texto reconocido. Al hacer clic en Analizar, la aplicación realiza el análisis de entrada de lápiz sincrónicamente y los resultados del reconocimiento aparecen en la pestaña Formulario de texto convertido .

## <a name="functionality"></a>Funcionalidad

Esta aplicación usa [inkOverlay para](/previous-versions/ms552322(v=vs.100)) habilitar la escritura. El objeto InkOverlay es adecuado para la toma de notas y la transcripción básica. El uso previsto principal de este objeto es mostrar la entrada de lápiz como entrada de lápiz. La clase principal para el análisis de entrada de lápiz es [la clase InkAnalyzer.](/previous-versions/ms583671(v=vs.100)) Cuando se llama al método Analyze [](/previous-versions/ms568971(v=vs.100)) del objeto InkAnalyzer, el análisis de entrada de lápiz se produce sincrónicamente.

La aplicación inicializa dos matrices, una de cadenas y otra de rectángulos. La matriz de cadenas, , se convierte en objetos Factoid que se pasan a `factoidStrings` [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) como [objetos AnalysisHintNode.](/previous-versions/ms573018(v=vs.100)) [](/previous-versions/ms583657(v=vs.100)) Los objetos AnalysisHintNode sesgados por InkAnalyzer hacia una entrada determinada. En este ejemplo se usan las sugerencias de fecha, hora y teléfono, así como otras.

Cada [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) está asociado a un área específica del formulario. Las áreas se representan mediante la matriz de rectángulos, `rects` . Al crear un [TextBox para](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) cada rectángulo, el ejemplo genera el texto reconocido en la ubicación correcta.


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



Después de eso, se trata simplemente de crear un controlador de eventos que desencadena el análisis de entrada de lápiz cuando el usuario hace clic en Analizar.


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



 

 
