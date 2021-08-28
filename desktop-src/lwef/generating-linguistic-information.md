---
title: Generar información lingüística
description: Generar información lingüística
ms.assetid: 903561f0-89dc-4297-8ea0-3fa150f2e6dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38f6f0409280e96ac288992efa560e83abd7c553
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879759"
---
# <a name="generating-linguistic-information"></a>Generar información lingüística

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Después de haber grabado un nuevo archivo de sonido o cargado un archivo de sonido existente, puede generar información fonética y de salto de palabras si escribe texto que se corresponda con el archivo de sonido en el cuadro **Representación** de texto. A continuación, **elija el comando Generar información** lingüística en el **menú** Editar o en la barra de herramientas. El editor de sonido muestra un mensaje de progreso y comienza a procesar el archivo de sonido. Cuando termina de generar información lingüística, muestra una asignación de etiquetas de palabras y ómelos para el archivo de sonido en cuadros del **cuadro Representación de** audio. Tenga en cuenta que **el comando Generar información** lingüística permanece deshabilitado hasta que escriba una representación de texto para el archivo de sonido.

![Captura de pantalla que muestra los paneles "Representación de texto" y "Representación de audio" en la Herramienta de edición de sonidos de información lingüística de Microsoft.](images/f3listlabel.gif)

Si el editor no genera un conjunto aceptable de etiquetas de palabras o grafías, vuelva a elegir el comando **Generar información** lingüística. Si el editor no genera información lingüística, compruebe la representación de texto para asegurarse de que todas las palabras están ordenadas y escritas correctamente, y de que no tiene espacios innecesarios alrededor de la puntuación. A continuación, **vuelva a elegir el** comando Generar información lingüística. Para editar la representación de texto,  seleccione texto en el cuadro de  texto Representación de texto y use los comandos **Cortar,** Copiar y Pegar del **menú** Editar. Si no está seguro de las palabras que incluye el archivo de  sonido, puede reproducir el archivo de sonido eligiendo **Reproducir** en el menú Editar o en la barra de herramientas del editor. Si el editor sigue sin generar etiquetas lingüísticas, intente volver a grabar el archivo de sonido. Es probable que una grabación de baja calidad, especialmente con ruido de fondo excesivo, reduzca la probabilidad de generar información lingüística razonable.

También puede crear manualmente su propia información lingüística seleccionando parte de la representación de audio y seleccionando **Insertar phonema** o **Insertar** palabra en el **menú** Editar. Estos comandos también están disponibles si hace clic con el botón derecho en la selección.

Para ver cómo se podría usar la información lingüística para  la animación de caracteres de sincronización con Microsoft Agent, elija el botón Reproducir de la barra de herramientas y el editor reproducirá el archivo de sonido, animando una imagen de muestreo basada en la información de etiqueta generada.

Puede cambiar la presentación de la etiqueta de phoneme para mostrar las asignaciones de IPA  (Alfabeto fonético internacional) eligiendo el comando **Phoneme Label Display** (Mostrar etiqueta de phonema) en el menú Edición y, a continuación, el comando IPA. Esto muestra el valor de byte del phoneme. Para volver a los nombres descriptivos, vuelva a elegir el comando **Phoneme Label Display (Mostrar** etiqueta de Phoneme) y, a continuación, **elija Name (Nombre).**

### <a name="playing-a-sound-file"></a>Reproducir un archivo de sonido

Puede reproducir archivos de Windows o archivos de sonido mejorados  lingüísticamente si elige el comando Reproducir en el menú **Audio** o en la barra de herramientas del editor. Los **comandos Pausar** **y** Detener permiten pausar o detener la reproducción del archivo de sonido. A medida que se reproduce el archivo, la imagen de muestreo anima para mostrar cómo un carácter de Microsoft Agent puede usar la información de sincronización de archivos.

También puede reproducir una parte seleccionada de un archivo de sonido arrastrando una selección en representación de **audio** o haciendo clic en una palabra o etiqueta de phoneme y, a continuación, **seleccionando Reproducir**. Para ampliar una selección existente, presione MAYÚS y haga clic en , o bien presione MAYÚS y arrastre a la nueva ubicación en **la representación de audio**.

### <a name="editing-linguistic-information"></a>Edición de información lingüística

Puede editar la información lingüística de un archivo de varias maneras. Por ejemplo, puede ajustar el límite de una etiqueta de palabra o phoneme moviendo el puntero al borde del cuadro que define el intervalo de la etiqueta. Cuando el puntero cambie al puntero de movimiento de límite, arrastre a la izquierda o a la derecha. El editor también ajusta automáticamente el límite de la palabra o el phonema adyacentes.

![Captura de pantalla que muestra las ediciones de la información lingüística de un archivo.](images/f4listadj.gif)

El ajuste del límite de una etiqueta de phoneme cambia el tiempo de un phonema cuando se reproduce el audio. En el caso de los caracteres desarrollados para su uso con Microsoft Agent, cambiar el límite de la etiqueta de phoneme puede cambiar el tiempo o la duración de una imagen de la cocina asignada a ese phonema. Al cambiar el límite de una etiqueta de palabra, se cambia el tiempo de la apariencia de la palabra en el globo de palabras del carácter.

También puede reemplazar una asignación de phoneme seleccionando la  etiqueta de phoneme y eligiendo **Reemplazar phoneme** en el menú Edición, o haciendo clic con el botón derecho en la etiqueta de phoneme y eligiendo **Reemplazar phoneme** en el menú emergente. El editor muestra el **cuadro de diálogo Reemplazar phoneme** y resalta la asignación de phoneme actual de la etiqueta. Puede elegir un phoneme de reemplazo seleccionando uno en la lista **de IPA** o eligiendo otra entrada en la **lista Nombre.** Si hay más de una traducción de IPA disponible para ese nombre, elija un elemento en la **lista de IPA.** Para especificar una designación de IPA para un phoneme que no se pueda incluir directamente en el idioma, escriba su valor hexadecimal o varios valores hexadecimales, concatenados con un carácter más (+). Una vez que haya seleccionado la información del phonema de reemplazo, elija **Aceptar** y el editor reemplazará la etiqueta de phoneme que seleccionó.

![Captura de pantalla que muestra el cuadro de diálogo "Reemplazar phonema", con &lt; &gt; "SIL" seleccionado como etiqueta descriptiva.](images/f5listphone.gif)

De forma similar, puede reemplazar una etiqueta de palabra haciendo clic en el cuadro de la etiqueta y eligiendo Reemplazar palabra **,** o haciendo clic con el botón derecho en el cuadro de la etiqueta y eligiendo **Reemplazar** palabra en el menú emergente. El editor muestra el **cuadro de diálogo Reemplazar** palabra . Escriba la palabra de reemplazo y elija **Aceptar.**

![Captura de pantalla que muestra el cuadro de diálogo "Reemplazar palabra" por "sonido" especificado en el cuadro de texto "Texto de word".](images/f6listrep.gif)

En el caso de los caracteres desarrollados para su uso con Microsoft Agent, el reemplazo de una etiqueta de phoneme puede cambiar la imagen de la cocina que se muestra cuando se reproduce el archivo de sonido. Al reemplazar una palabra, se reemplaza el texto que aparece en el globo de palabras del carácter cuando se llama al método [**Speak.**](speak-method.md)

También puede insertar una nueva etiqueta o palabra de phonema si realiza una  selección en  representación de **audio** y elige Insertar **phonema** o Insertar palabra en el menú Edición, o bien haciendo clic con el botón derecho en la selección y eligiendo los comandos en el menú emergente. Estos comandos abren cuadros de  diálogo similares  a los cuadros de diálogo Reemplazar phonema y Reemplazar palabra, salvo que el editor inserta la nueva palabra o phoneme en lugar de reemplazar la información existente.

Por último, puede eliminar un phoneme o una palabra seleccionando su etiqueta y eligiendo **Eliminar phonema** o **Eliminar palabra.** Esto quita su información lingüística del archivo.

 

 




