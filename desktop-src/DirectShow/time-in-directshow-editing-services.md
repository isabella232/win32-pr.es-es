---
description: Tiempo en los servicios de edición de DirectShow
ms.assetid: 4e8cc766-97f3-45d5-9c4a-5cd6e9ad9c09
title: Tiempo en los servicios de edición de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 421831742a2805f58d61c2258dad89d339131f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678537"
---
# <a name="time-in-directshow-editing-services"></a>Tiempo en los servicios de edición de DirectShow

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Para editar vídeo, debe trabajar con algunos conceptos importantes de temporización. Por ejemplo:

-   Cada clip tiene una duración.
-   Los clips, las transiciones y los efectos aparecen en ciertos momentos de un proyecto.
-   El vídeo tiene una velocidad de fotogramas, expresada en fotogramas por segundo (FPS).

Los [servicios de edición de DirectShow](directshow-editing-services.md) (des) proporcionan varios métodos que establecen o recuperan las frecuencias de las horas y los fotogramas. El significado de estos valores depende del contexto.

**Valores de hora**

Cuando un parámetro expresa una hora, se pueden realizar tres significados distintos:

-   *Hora* de la escala de tiempo: la hora relativa al inicio de la escala de tiempo. Por ejemplo, un clip podría comenzar 2 segundos en la escala de tiempo, o una transición podría producirse 15 segundos en la escala de tiempo. La escala de tiempo determina el proyecto representado final, por lo que también puede pensar en el tiempo de la escala de tiempo como "tiempo de proyecto".
-   *Tiempo medio*: punto en un archivo de código fuente relativo al inicio del archivo, como se alcanzó durante la reproducción normal. Por ejemplo, si tiene un archivo de vídeo de 10 segundos, el punto a lo largo del archivo se produce en 5 segundos, expresado como una hora de medio.
-   *Hora primaria*: hora relativa a un objeto de la escala de tiempo. Por ejemplo, si un objeto se inicia en 8 segundos en la escala de tiempo y contiene otro objeto que comienza en 10 segundos en la escala de tiempo, el objeto secundario se inicia en 2 segundos en relación con el elemento primario. Los seguimientos virtuales se inician en cero en el tiempo, con respecto a la escala de tiempo. Por lo tanto, para cualquier objeto de una pista virtual, la hora principal es igual a la hora de la escala de tiempo.

La hora del medio se aplica solo a los objetos de origen. Cada objeto de origen tiene una hora de inicio y una hora de detención del medio. Por ejemplo, supongamos que tiene un clip de vídeo de 10 segundos y desea usar solo 5 segundos desde el centro del clip, recortando los primeros 2 segundos y los últimos 3 segundos del clip. Si desea que el clip muestre 20 segundos en el proyecto (y suponiendo una velocidad de reproducción normal), debe especificar las siguientes horas de inicio y detención.

-   Inicio de medio: 2 segundos
-   Detención de medios: 7 segundos
-   Inicio de la escala de tiempo: 20 segundos
-   Detención de la escala de tiempo: 25 segundos

    ![insertar un clip de origen en una escala de tiempo](images/des-time1.png)

**Velocidades de fotogramas**

La velocidad de fotogramas es la "velocidad" de una secuencia de medios, medida en fotogramas por segundo. Al igual que con los valores de tiempo, el significado de una velocidad de fotogramas depende del contexto:

-   **Velocidad de fotogramas de salida:** Velocidad de fotogramas del proyecto representado final, definido por el grupo. Al representar el proyecto, cada grupo se convierte en una secuencia de medios independiente con su propia velocidad de fotogramas.
-   **Velocidad de fotogramas de origen:** Velocidad de fotogramas en la que se creó originalmente el archivo de código fuente. No es necesario que la velocidad de fotogramas creada coincida con la velocidad de fotogramas de salida del grupo. DES realizará un muestreo automático del archivo, según sea necesario. Para la mayoría de los formatos multimedia, DES puede determinar la velocidad de fotogramas examinando el formato. Una secuencia DIB es una excepción; debe especificar la velocidad de fotogramas de una secuencia DIB. (Para obtener más información, vea [trabajar con orígenes](working-with-sources.md)).

**Velocidad de reproducción:** La velocidad aparente de un clip de origen cuando aparece en el proyecto. Por ejemplo, 10 segundos de vídeo puede ajustarse a 5 segundos en la escala de tiempo. Como resultado, la velocidad del clip aumenta en un factor de 2, como se muestra en el diagrama siguiente.

![realización de una reproducción de origen más rápida](images/des-time2.png)

(Con un origen de audio, el paso también se desplazaría). La fórmula siguiente determina la velocidad de reproducción de un clip de origen:

-   Velocidad de reproducción = (media STOP – media Start)/(detención de la escala de tiempo: Inicio de la escala de tiempo)

Tenga en cuenta que cada una de estas tres tarifas es independiente de las demás:

-   Puede acelerar o ralentizar un clip ajustando las horas del medio. Esto no afecta a la velocidad de fotogramas de la salida final.
-   Puede aumentar o disminuir la velocidad de fotogramas de salida sin que ello afecte a la velocidad con que se reproduce un archivo.
-   Puede mezclar, dentro del mismo grupo, archivos de origen con diferentes velocidades de fotogramas creadas, y DES realizará el muestreo o la resolución de cada clip para que coincida con la velocidad de fotogramas del grupo.

Al representar un proyecto, todas las horas se redondean al límite de fotogramas más cercano, según lo determinado por la velocidad de fotogramas de grupo. Por ejemplo, supongamos que un grupo de vídeos tiene una velocidad de fotogramas de 30 fps. Cada fotograma es aproximadamente de 33 milisegundos (MS). Supongamos que agrega un clip de origen de 1,68 segundos a la escala de tiempo, a partir de cero. El origen no finaliza exactamente en un límite de marco, por lo que DES redondea la hora de detención a 1,6666 segundos (50 fotogramas). Si busca 1,68 segundos en el proyecto representado, buscará más allá del final del origen, hasta el marco número 51.

Sin embargo, DES no sobrescribe la hora de detención del origen. Posteriormente, puede cambiar la velocidad de fotogramas de grupo o trasladar el origen a un nuevo punto de la escala de tiempo donde se redondea de manera diferente. Por lo tanto, DES conserva la hora de detención original y se redondea solo cuando es necesario. Para obtener más información, vea [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con servicios de edición de DirectShow](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



