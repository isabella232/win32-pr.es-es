---
title: Cambio de la propiedad del complemento DSP de audio de ejemplo
description: Cambio de la propiedad del complemento DSP de audio de ejemplo
ms.assetid: 9e742bcd-cff8-422f-ad91-d8d46f15bdc4
keywords:
- Complementos de Windows Media Player, audio DSP
- complementos, DSP de audio
- Complementos de procesamiento de señal digital, propiedades de audio
- Complementos DSP, propiedades de audio
- Complementos DSP de audio, propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc27f58fa8c8903b54f9903797dcc32a7795841
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777719"
---
# <a name="changing-the-sample-audio-dsp-plug-in-property"></a>Cambio de la propiedad del complemento DSP de audio de ejemplo

Probablemente querrá cambiar la propiedad que el Asistente para complementos de Windows Media Player crea de forma predeterminada. En la siguiente lista se detallan los elementos que pueden requerir un cambio:

-   **El recurso de cuadro de diálogo.** Haga clic en la pestaña **ResourceView** en la ventana área de trabajo del proyecto. Expanda la lista de carpetas para abrir la carpeta del cuadro de diálogo. Haga doble clic en el recurso de cuadro de diálogo para abrir el editor de recursos. Puede realizar cambios en el cuadro de diálogo de la página de propiedades para satisfacer sus necesidades. Por ejemplo, puede cambiar el texto de la etiqueta o reemplazar el control de edición por una casilla.
-   **Código del objeto de página de propiedades.** La implementación predeterminada usa una variable de tipo Double para almacenar el factor de escala. Podría requerir un tipo de datos diferente. Esto también requeriría cambiar el código que conserva los datos en el registro y Lee los datos del registro (incluido el código que lee del registro en *CProjectName*::**FinalConstruct**).
-   **Variable miembro que almacena el valor de propiedad.** Esta variable se denomina "m \_ fScaleFactor" y se declara como tipo Double. Puede que desee cambiar el nombre y el tipo de esta variable en todo el proyecto.
-   **Los métodos GET y put de propiedad.** Es posible que desee cambiar los nombres, los parámetros y las implementaciones de estos métodos. No olvide también reflejar los cambios en otros lugares del proyecto. Por ejemplo, el método de **aplicación** de la página de propiedades llama a *CProjectName*::**Put \_ Scale**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementar un complemento de DSP de audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




