---
title: Cambio de la propiedad del complemento DSP de audio de ejemplo
description: Cambio de la propiedad del complemento DSP de audio de ejemplo
ms.assetid: 9e742bcd-cff8-422f-ad91-d8d46f15bdc4
keywords:
- Reproductor de Windows Media complementos, DSP de audio
- complementos, DSP de audio
- complementos de procesamiento de señal digital, propiedades de audio
- Complementos de DSP, propiedades de audio
- complementos de DSP de audio, propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8aac1cf385f41e966bec51f19454308cf52697c995db4962a45486999ebae9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342628"
---
# <a name="changing-the-sample-audio-dsp-plug-in-property"></a>Cambio de la propiedad del complemento DSP de audio de ejemplo

Probablemente quiera cambiar la propiedad que el Asistente para Reproductor de Windows Media complementos crea de forma predeterminada. En la lista siguiente se detallan los elementos que pueden requerir un cambio:

-   **Recurso de diálogo.** Haga clic en **la pestaña ResourceView** en la Project Área de trabajo. Expanda la lista de carpetas para abrir la carpeta Diálogo. Haga doble clic en el recurso de cuadro de diálogo para abrir el editor de recursos. Puede realizar cambios en el cuadro de diálogo de la página de propiedades para satisfacer sus necesidades. Por ejemplo, puede cambiar el texto de la etiqueta o reemplazar el control de edición por una casilla.
-   **Código de objeto de la página de propiedades.** La implementación predeterminada usa una variable de tipo double para almacenar el factor de escala. Es posible que necesite otro tipo de datos. Esto también requeriría cambiar el código que conserva los datos en el registro y lee los datos del registro (incluido el código que lee del registro en *CProjectName*::**FinalConstruct**).
-   **Variable miembro que almacena el valor de propiedad.** Esta variable se denomina "m \_ fScaleFactor" y se declara como tipo double. Es posible que quiera cambiar el nombre y el tipo de esta variable en todo el proyecto.
-   **Métodos get y property put de la propiedad .** Es posible que quiera cambiar los nombres, parámetros e implementaciones de estos métodos. No olvide reflejar también esos cambios en otra parte del proyecto. Por ejemplo, la página de propiedades **Apply** method llama *a CProjectName*::**put \_ scale**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de un complemento DSP de audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




