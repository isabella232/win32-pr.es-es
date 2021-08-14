---
title: Generación de información lingüística
description: Generación de información lingüística
ms.assetid: 903561f0-89dc-4297-8ea0-3fa150f2e6dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a068153863236b7096b67a976bbcf0654af9c75df87d2f527027830a4df33eb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479313"
---
# <a name="generating-linguistic-information"></a>Generación de información lingüística

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Después de grabar un nuevo archivo de sonido o de cargar un archivo de sonido existente, puede generar información fonética y de salto de palabras si escribe texto que corresponda al archivo de sonido en el cuadro Representación de **texto.** A continuación, **elija el comando Generar información** lingüística en el **menú** Editar o en la barra de herramientas. El editor de sonido muestra un mensaje de progreso y comienza a procesar el archivo de sonido. Cuando termina de generar información lingüística, muestra una asignación de etiquetas de palabra y phoneme para el archivo de sonido en cuadros del cuadro **Representación de** audio. Tenga en cuenta que **el comando Generar información** lingüística permanece deshabilitado hasta que escriba una representación de texto para el archivo de sonido.

![Captura de pantalla que muestra los paneles "Representación de texto" y "Representación de audio" en la Herramienta de edición de sonido de información lingüística de Microsoft.](images/f3listlabel.gif)

Si el editor no genera un conjunto aceptable de etiquetas de palabras o grafías, elija de nuevo el comando **Generar información** lingüística. Si el editor no genera ninguna información lingüística, compruebe la representación de texto para asegurarse de que todas las palabras están ordenadas y escritas correctamente, y de que no tiene espacios innecesarios alrededor de la puntuación. A continuación, **vuelva a elegir el comando Generar información** lingüística. Para editar la representación de texto, seleccione texto en el cuadro de texto **Representación** **de** texto y use los comandos **Cortar,** **Copiar** y Pegar en el **menú** Editar. Si no está seguro de las palabras que incluye el archivo de  sonido, puede reproducir el archivo de sonido eligiendo **Reproducir** en el menú Editar o en la barra de herramientas del editor. Si el editor sigue sin generar etiquetas lingüísticas, intente volver a grabar el archivo de sonido. Es probable que una grabación de baja calidad, especialmente con un ruido de fondo excesivo, reduzca la probabilidad de generar información lingüística razonable.

También puede crear manualmente su propia información lingüística seleccionando parte de la representación de audio y eligiendo **Insertar phoneme** o **Insertar** palabra en el **menú** Editar. Estos comandos también están disponibles si hace clic con el botón derecho en la selección.

Para ver cómo se podría usar la información lingüística para  la animación de caracteres de sincronización con Microsoft Agent, elija el botón Reproducir de la barra de herramientas y el editor reproducirá el archivo de sonido, animando una imagen de muestra de la muestra basada en la información de etiqueta generada.

Puede cambiar la presentación de la etiqueta de phoneme para mostrar las asignaciones de  IPA (alfabeto fonético internacional). Para ello, elija el comando **Phoneme Label Display** (Mostrar etiqueta telefónica) en el menú Editar y, después, el comando IPA. Esto muestra el valor de byte del phoneme. Para volver a cambiar a los nombres descriptivos, vuelva a elegir el comando **Phoneme Label Display y,** a continuación, **elija Nombre.**

### <a name="playing-a-sound-file"></a>Reproducir un archivo de sonido

Puede reproducir archivos de Windows o archivos de sonido mejorados  lingüísticamente si elige el comando Reproducir en el menú **Audio** o en la barra de herramientas del editor. Los **comandos Pausar** **y** Detener permiten pausar o detener la reproducción del archivo de sonido. A medida que se reproduce el archivo, la imagen de muestra de la cocina se anima para mostrar cómo un carácter de Microsoft Agent podría usar la información de sincronización.

También puede reproducir una parte seleccionada de un archivo de sonido arrastrando una selección en la representación de **audio** o haciendo clic en una etiqueta de palabra o phoneme y, a continuación, **eligiendo Reproducir**. Puede extender una selección existente presionando MAYÚS y haciendo clic en , o presionando MAYÚS y arrastrando hasta la nueva ubicación en la representación **de audio**.

### <a name="editing-linguistic-information"></a>Edición de información lingüística

Puede editar la información lingüística de un archivo de varias maneras. Por ejemplo, puede ajustar el límite de una etiqueta de palabra o phoneme moviendo el puntero al borde del cuadro que define el intervalo de la etiqueta. Cuando el puntero cambie al puntero de movimiento de límite, arrastre a la izquierda o a la derecha. El editor también ajusta automáticamente el límite de palabra o phoneme adyacente.

![Captura de pantalla que muestra las modificaciones en la información lingüística de un archivo.](images/f4listadj.gif)

Ajustar el límite de una etiqueta de phoneme cambia el tiempo de un phoneme cuando se reproduce el audio. En el caso de los caracteres desarrollados para su uso con Microsoft Agent, cambiar el límite de la etiqueta del phoneme puede cambiar el tiempo o la duración de una imagen de cocina asignada a ese phoneme. Cambiar el límite de una etiqueta de palabra cambia el tiempo de la apariencia de la palabra en el globo de palabras del carácter.

También puede reemplazar una asignación de phoneme seleccionando la  etiqueta de phoneme y eligiendo **Reemplazar phoneme** en el menú Editar, o haciendo clic con el botón derecho en la etiqueta del phoneme y eligiendo **Reemplazar phoneme** en el menú emergente. El editor muestra el **cuadro de diálogo Reemplazar phoneme** y resalta la asignación de phoneme actual de la etiqueta. Puede elegir un phoneme de reemplazo seleccionando uno en la lista **IPA** o eligiendo otra entrada en la **lista Nombre.** Si hay más de una traducción de IPA disponible para ese nombre, elija un elemento en la **lista de IPA.** Para especificar una designación de IPA para un phoneme que no se pueda incluir directamente en el idioma, escriba su valor hexadecimal o varios valores hexadecimales, concatenados con un carácter más (+). Una vez que haya seleccionado la información del phoneme de reemplazo, elija **Aceptar** y el editor reemplazará la etiqueta de phoneme que seleccionó.

![Captura de pantalla que muestra el cuadro de diálogo "Reemplazar phoneme", con la opción "<SIL>" seleccionada como etiqueta descriptiva.](images/f5listphone.gif)

De forma similar, puede reemplazar una etiqueta de palabra haciendo clic en el cuadro de la etiqueta y eligiendo Reemplazar **palabra,** o haciendo clic con el botón derecho en el cuadro de la etiqueta y eligiendo **Reemplazar** palabra en el menú emergente. El editor muestra el **cuadro de diálogo Reemplazar** palabra. Escriba la palabra de reemplazo y elija **Aceptar.**

![Captura de pantalla que muestra el cuadro de diálogo "Reemplazar palabra" por "sonido" escrito en el cuadro de texto "Texto de word".](images/f6listrep.gif)

En el caso de los caracteres desarrollados para su uso con Microsoft Agent, reemplazar una etiqueta de phoneme puede cambiar la imagen de cocina que se muestra cuando se reproduce el archivo de sonido. Al reemplazar una palabra, se reemplaza el texto que aparece en el globo de palabras del carácter cuando se llama al método [**Speak.**](speak-method.md)

También puede insertar una nueva etiqueta o palabra de phoneme haciendo una selección en  la representación de **audio** y eligiendo Insertar **phoneme** o **Insertar** palabra en el menú Edición, o bien haciendo clic con el botón derecho en la selección y eligiendo los comandos en el menú emergente. Estos comandos abren cuadros de diálogo similares  a los cuadros de diálogo Reemplazar **phoneme** y Reemplazar palabra, salvo que el editor inserta la nueva palabra o phoneme en lugar de reemplazar la información existente.

Por último, puede eliminar un phoneme o una palabra seleccionando su etiqueta y eligiendo Delete Phoneme (Eliminar **phoneme)** **o Delete Word (Eliminar palabra).** Esto quita su información lingüística del archivo.

 

 




