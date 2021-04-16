---
title: Generar información lingüística
description: Generar información lingüística
ms.assetid: 903561f0-89dc-4297-8ea0-3fa150f2e6dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23fb99a5139e287e07e353791ce776b8a04dd8d2
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104563468"
---
# <a name="generating-linguistic-information"></a>Generar información lingüística

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Después de grabar un nuevo archivo de sonido, o de cargar un archivo de sonido existente, puede generar información fonética y de separación de palabras escribiendo texto que se corresponda con el archivo de sonido en el cuadro **representación de texto** . A continuación, elija el comando **generar información lingüística** en el menú **edición** o en la barra de herramientas. El editor de sonidos muestra un mensaje de progreso y comienza a procesar el archivo de sonido. Cuando finaliza la generación de información lingüística, se muestra una asignación de etiquetas de palabra y fonema para el archivo de sonido en los cuadros del cuadro **representación de audio** . Tenga en cuenta que el comando **generar información lingüística** permanece deshabilitado hasta que escriba una representación de texto para el archivo de sonido.

![Captura de pantalla que muestra los paneles "representación de texto" y "representación de audio" en la herramienta de edición de sonido lingüístico de Microsoft.](images/f3listlabel.gif)

Si el editor no produce un conjunto aceptable de etiquetas de palabra o fonema, elija de nuevo el comando **generar información lingüística** . Si el editor no genera ninguna información lingüística, compruebe su representación de texto para asegurarse de que todas las palabras están ordenadas y escritas correctamente, y de que no tiene espacios innecesarios en torno a la puntuación. A continuación, elija de nuevo el comando **generar información lingüística** . Para editar la representación de texto, seleccione texto en el cuadro de texto **representación de texto** y use los comandos **cortar**, **copiar** y **pegar** del menú **edición** . Si no está seguro de las palabras que incluye el archivo de sonido, puede reproducir el archivo de sonido eligiendo **reproducir** en el menú **edición** o en la barra de herramientas del editor. Si el editor todavía no puede generar etiquetas lingüísticas, intente grabar de nuevo el archivo de sonido. Un registro de mala calidad, especialmente con un ruido de fondo excesivo, es probable que reduzca la probabilidad de generar información lingüística razonable.

También puede crear manualmente su propia información lingüística seleccionando parte de la representación de audio y eligiendo **Insertar fonema** o **Insertar palabra** en el menú **edición** . Estos comandos también están disponibles si hace clic con el botón secundario en la selección.

Para ver cómo se podría usar la información lingüística para la animación de caracteres de sincronización de Lip con Microsoft Agent, elija el botón **reproducir** de la barra de herramientas y el editor reproducirá el archivo de sonido, animando una imagen de la boca de ejemplo en función de la información de la etiqueta generada.

Puede cambiar la presentación de la etiqueta del fonema para mostrar las asignaciones del IPA (alfabeto fonético internacional) eligiendo el comando de **visualización de etiqueta del fonema** en el menú **edición** y, a continuación, el comando IPA. Esto muestra el valor de bytes del fonema. Para volver a cambiar a los nombres descriptivos, vuelva a elegir el comando de **visualización de etiqueta del fonema** y, a continuación, elija **nombre**.

### <a name="playing-a-sound-file"></a>Reproducir un archivo de sonido

Puede reproducir archivos de sonido de Windows estándar o archivos de sonido lingüísticamente mejorados; para ello, elija el comando **reproducir** en el menú **audio** o en la barra de herramientas del editor. Los comandos **pausar** y **detener** permiten pausar o detener la reproducción del archivo de sonido. A medida que reproduce el archivo, la imagen de la boca de ejemplo se anima para mostrar cómo un carácter de agente de Microsoft podría usar la información de sincronización de Lip.

También puede reproducir una parte seleccionada de un archivo de sonido arrastrando una selección en la **representación de audio** o haciendo clic en una etiqueta de palabra o fonema y, a continuación, eligiendo **reproducir**. Puede extender una selección existente presionando MAYÚS y haciendo clic, o presionando MAYÚS y arrastrándola a la nueva ubicación en la **representación de audio**.

### <a name="editing-linguistic-information"></a>Edición de la información lingüística

Puede editar la información lingüística de un archivo de varias maneras. Por ejemplo, puede ajustar el límite de la etiqueta de una palabra o un fonema moviendo el puntero al borde del cuadro que define el intervalo de la etiqueta. Cuando el puntero cambie al puntero de movimiento del límite, arrástrelo hacia la izquierda o hacia la derecha. El editor ajusta automáticamente también el límite de la palabra o el fonema adyacente.

![Captura de pantalla que muestra las modificaciones de la información lingüística de un archivo.](images/f4listadj.gif)

El ajuste del límite de una etiqueta de fonema cambia la temporización de un fonema cuando se reproduce el audio. En el caso de los caracteres desarrollados para su uso con el agente de Microsoft, el cambio del límite de la etiqueta del fonema puede cambiar el tiempo o la duración de una imagen de boca asignada a ese fonema. Cambiar el límite de una etiqueta de palabra cambia el tiempo de la apariencia de la palabra en el globo de palabras del carácter.

También puede reemplazar una asignación de fonema seleccionando la etiqueta del fonema y eligiendo **reemplazar fonema** en el menú **edición** , o haciendo clic con el botón derecho en la etiqueta del fonema y eligiendo **reemplazar fonema** en el menú emergente. El editor muestra el cuadro de diálogo **reemplazar fonema** y resalta la asignación actual del fonema de la etiqueta. Para elegir un fonema de reemplazo, seleccione uno en la lista **IPA** o elija otra entrada en la lista **nombre** . Si hay más de una traducción del IPA disponible para ese nombre, elija un elemento en la lista **IPA** . Para especificar una designación de IPA para un fonema que puede no estar directamente incluida en el idioma, escriba su valor hexadecimal o varios valores hexadecimales, concatenados con un signo más (+). Una vez que haya seleccionado la información de reemplazo de fonema, elija **Aceptar** y el editor reemplazará la etiqueta de fonema seleccionada.

![Captura de pantalla que muestra el cuadro de diálogo ' reemplazar fonema ', con ' <SIL> ' seleccionado como etiqueta descriptiva.](images/f5listphone.gif)

Del mismo modo, puede reemplazar una etiqueta de palabra haciendo clic en el cuadro de la etiqueta y eligiendo **reemplazar palabra**, o haciendo clic con el botón secundario en el cuadro de la etiqueta y eligiendo **reemplazar palabra** en el menú emergente. El editor muestra el cuadro de diálogo **reemplazar palabra** . Escriba la palabra de reemplazo y elija **Aceptar**.

![Captura de pantalla que muestra el cuadro de diálogo ' reemplazar palabra ' con ' sonido ' escrito en el cuadro de texto ' texto de palabra '.](images/f6listrep.gif)

En el caso de los caracteres desarrollados para su uso con el agente de Microsoft, el reemplazo de una etiqueta de fonema puede cambiar la imagen de boca que se muestra cuando se reproduce el archivo de sonido. Al reemplazar una palabra, se reemplaza el texto que aparece en el globo de palabras del carácter cuando se llama al método [**Speak**](speak-method.md) .

También puede insertar una nueva etiqueta o palabra de fonema si realiza una selección en la **representación de audio** y elige **Insertar fonema** o **Insertar palabra** en el menú **edición** , o hacer clic con el botón derecho en la selección y elegir los comandos en el menú emergente. Estos comandos activan cuadros de diálogo similares a los cuadros de diálogo **reemplazar fonema** y **reemplazar palabra** , salvo que el editor inserta la nueva palabra o el fonema en lugar de reemplazar la información existente.

Por último, puede eliminar un fonema o una palabra seleccionando su etiqueta y eligiendo **eliminar fonema** o **eliminar palabra**. Esto quita su información lingüística del archivo.

 

 




