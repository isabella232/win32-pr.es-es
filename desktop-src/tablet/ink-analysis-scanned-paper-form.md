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
# <a name="ink-analysis-scanned-paper-form"></a>Formulario de papel digitalizado de análisis de tinta

En este ejemplo se muestra cómo utilizar el análisis de tinta para crear una aplicación de rellenado de formularios, donde el formulario se basa en un papel digitalizado.

## <a name="features-demonstrated"></a>Características mostradas

Esta aplicación de ejemplo muestra las siguientes características de la API de análisis de tinta y los controles de entrada de lápiz de Windows Forms:

-   Cargar un formulario de papel digitalizado. En el ejemplo se importa el formulario a partir de una imagen en formato. png.
-   Recopilación y representación de la entrada de lápiz en la parte superior del formulario digitalizado.
-   Usar un objeto [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) para analizar la escritura a mano.
-   Generar objetos [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) para mejorar los resultados de escritura a mano.
-   Rellenar cuadros de texto a partir de sugerencias de análisis.
-   Crear una experiencia de corrección de texto básica.

## <a name="project-references"></a>Referencias del proyecto

El ejemplo está disponible como una aplicación Windows Forms o Windows Presentation Foundation. Las referencias a la versión Windows Forms:

-   Microsoft.Ink.dll
-   Microsoft.Ink.Analysis.dll

La versión Windows Presentation Foundation hace referencia a IAWinFX.dll además de los archivos dll de Windows Presentation Foundation principales.

> [!Note]  
> La versión Windows Presentation Foundation de este ejemplo (que se encuentra en el directorio XAML) requiere que las extensiones de Windows Presentation Foundation para Microsoft Visual Studio 2005 estén instaladas en el sistema.

 

## <a name="user-interface"></a>Interfaz de usuario

La interfaz de usuario de esta aplicación está formada por un [TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) con dos objetos [TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) asociados: formulario de entrada de lápiz y formato de texto convertido. La pestaña formulario de entrada de lápiz contiene

-   Un panel que contiene una imagen de un formulario de papel digitalizado que se usa para realizar mensajes de teléfono.
-   Una casilla que tiene la aplicación muestra los límites de la sugerencia de análisis cuando está seleccionada.
-   Un par de botones, borrar y analizar, que borran la tinta del formulario e inicializan el análisis de tinta.

El formato de texto convertido contiene la misma imagen y es la página en la que la aplicación muestra el texto reconocido. Al hacer clic en analizar, la aplicación realiza el análisis de tinta sincrónicamente y los resultados del reconocimiento aparecen en la pestaña formulario de texto convertido.

## <a name="functionality"></a>Funcionalidad

Esta aplicación utiliza un [InkOverlay](/previous-versions/ms552322(v=vs.100)) para habilitar la escritura. El objeto InkOverlay es idóneo para tomar notas y scribbling básicas. El uso previsto principal de este objeto es mostrar la entrada de lápiz como entrada de lápiz. La clase principal para el análisis de tinta es la clase [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) . Cuando se llama al método [Analyze](/previous-versions/ms568971(v=vs.100)) del objeto InkAnalyzer, el análisis de tinta se produce sincrónicamente.

La aplicación inicializa dos matrices, una de las cadenas y uno de rectángulos. La matriz de cadena, `factoidStrings` , se compone de objetos [Factoid](/previous-versions/ms583657(v=vs.100)) que se pasan a [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) como objetos [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) . Los objetos AnalysisHintNode sesgan el InkAnalyzer de entrada en particular. En este ejemplo se usan las sugerencias de fecha, hora y teléfono, así como otras.

Cada [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) está asociado a un área específica del formulario. La matriz de rectángulos representa las áreas `rects` . Al crear un [cuadro](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) de texto para cada rectángulo, el ejemplo genera el texto reconocido en la ubicación correcta.


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



Después, es simplemente cuestión de crear un controlador de eventos que desencadene el análisis de tinta cuando el usuario haga clic en analizar.


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



 

 
