---
description: Tiempo en los servicios DirectShow edición de datos
ms.assetid: 4e8cc766-97f3-45d5-9c4a-5cd6e9ad9c09
title: Tiempo en los servicios DirectShow edición de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afc99ff2391ea7975daed7b4152e869741f9990561417131942c4d86e904fca8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083635"
---
# <a name="time-in-directshow-editing-services"></a>Tiempo en los servicios DirectShow edición de datos

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Para editar el vídeo, debe trabajar con algunos conceptos de control de tiempo importantes. Por ejemplo:

-   Cada clip tiene una duración.
-   Los clips, transiciones y efectos aparecen en determinados momentos en un proyecto.
-   El vídeo tiene una velocidad de fotogramas, expresada en fotogramas por segundo (fps).

[DirectShow Editing Services](directshow-editing-services.md) (DES) proporciona varios métodos que establecen o recuperan tiempos y velocidades de fotogramas. El significado de estos valores depende del contexto.

**Valores de tiempo**

Cuando un parámetro expresa una hora, son posibles tres significados distintos:

-   *Hora de la* escala de tiempo: hora relativa al principio de la escala de tiempo. Por ejemplo, un clip podría iniciarse 2 segundos en la escala de tiempo o una transición podría producirse 15 segundos en la escala de tiempo. La escala de tiempo determina el proyecto representado final, por lo que también puede pensar en el tiempo de la escala de tiempo como "tiempo del proyecto".
-   *Hora del medio:* punto de un archivo de código fuente relativo al inicio del archivo, como se alcanza durante la reproducción normal. Por ejemplo, si tiene un archivo de vídeo de 10 segundos, el punto medio a través del archivo se produce en 5 segundos, expresado como un tiempo multimedia.
-   *Hora primaria:* hora relativa a un objeto en la escala de tiempo. Por ejemplo, si un objeto comienza en 8 segundos en la escala de tiempo y contiene otro objeto que comienza en 10 segundos en la escala de tiempo, el objeto secundario se inicia en 2 segundos con respecto al elemento primario. Todas las pistas virtuales se inician a la hora cero, en relación con la escala de tiempo. Por lo tanto, para cualquier objeto de una pista virtual, el tiempo primario es igual a la hora de la escala de tiempo.

El tiempo de los medios solo se aplica a los objetos de origen. Cada objeto de origen tiene una hora de inicio de medios y una hora de detenerse de medios. Por ejemplo, supongamos que tiene un clip de vídeo de 10 segundos y solo quiere usar 5 segundos desde el centro del clip, recortando los primeros 2 segundos y los últimos 3 segundos del clip. Si desea que el clip aparezca 20 segundos en el proyecto (y suponiendo una velocidad de reproducción normal), debe especificar las siguientes horas de inicio y de detenerse.

-   Inicio de medios: 2 segundos
-   Media stop: 7 segundos
-   Inicio de la escala de tiempo: 20 segundos
-   Escala de tiempo: 25 segundos

    ![insertar un clip de origen en una escala de tiempo](images/des-time1.png)

**Velocidades de fotogramas**

La velocidad de fotogramas es la "velocidad" de una secuencia multimedia, medida en fotogramas por segundo. Al igual que con los valores de tiempo, el significado de una velocidad de fotogramas depende del contexto:

-   **Velocidad de fotogramas de salida:** Velocidad de fotogramas del proyecto representado final, definido por el grupo. Al representar el proyecto, cada grupo se convierte en un flujo multimedia independiente con su propia velocidad de fotogramas.
-   **Velocidad de fotogramas de origen:** Velocidad de fotogramas en la que se edizó originalmente el archivo de origen. La velocidad de fotogramas autora no tiene que coincidir con la velocidad de fotogramas de salida del grupo. DES actualizará o reduce automáticamente el ejemplo del archivo según sea necesario. Para la mayoría de los formatos multimedia, DES puede determinar la velocidad de fotogramas examinando el formato. Una secuencia DIB es una excepción; debe especificar la velocidad de fotogramas de una secuencia DIB. (Para obtener más información, vea [Trabajar con orígenes).](working-with-sources.md)

**Velocidad de reproducción:** Velocidad aparente de un clip de origen cuando aparece en el proyecto. Por ejemplo, 10 segundos de vídeo pueden caber en 5 segundos en la escala de tiempo. Como resultado, la velocidad del clip aumenta en un factor de 2, como se muestra en el diagrama siguiente.

![hacer que una reproducción de origen sea más rápida](images/des-time2.png)

(Con un origen de audio, el tono también cambiaría). La fórmula siguiente determina la velocidad de reproducción de un clip de origen:

-   Velocidad de reproducción = (Media Stop – Media Start) / (Timeline Stop – Timeline Start)

Tenga en cuenta que cada una de estas tres tarifas es independiente de las demás:

-   Puede acelerar o ralentizar un clip ajustando los tiempos de los medios. esto no afecta a la velocidad de fotogramas de la salida final.
-   Puede aumentar o disminuir la velocidad de fotogramas de salida sin afectar a la rapidez con la que se reproduce un archivo.
-   Puede mezclar, dentro del mismo grupo, los archivos de origen que tienen diferentes velocidades de fotogramas creados, y DES subirá o desmuestreará cada clip para que coincida con la velocidad de fotogramas del grupo.

Cuando se representa un proyecto, todas las veces se redondea al límite de fotogramas más cercano, según lo determinado por la velocidad de fotogramas del grupo. Por ejemplo, suponga que un grupo de vídeo tiene una velocidad de fotogramas de 30 fps. Cada fotograma es aproximadamente de 33 milisegundos (ms). Supongamos que agrega un clip de origen de 1,68 segundos a la escala de tiempo, empezando en el momento cero. El origen no termina exactamente en un límite de marco, por lo que DES redondea el tiempo de detenerse a 1,6666 segundos (50 fotogramas). Si busca 1,68 segundos en el proyecto representado, realmente buscará más allá del final del origen, hasta el marco 51.

Sin embargo, DES no sobrescribe la hora de detenerse del origen. Más adelante, puede cambiar la velocidad de fotogramas del grupo o mover el origen a un nuevo punto de la escala de tiempo donde se redondee de forma diferente. Por lo tanto, DES conserva el tiempo de detenerse original y se redondea solo cuando sea necesario. Para obtener más información, [**vea IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales con DirectShow Editing Services](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



