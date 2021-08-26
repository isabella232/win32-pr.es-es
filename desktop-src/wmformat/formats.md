---
title: Formatos
description: Formatos
ms.assetid: 7c602643-f1fc-4fbd-a739-4296dc758bc9
keywords:
- Windows SDK de formato multimedia, entradas
- Windows SDK de formato multimedia, secuencias
- Windows SDK de formato multimedia, salidas
- Windows SDK de formato multimedia, formatos
- Formato de sistemas avanzados (ASF), entradas
- ASF (formato de sistemas avanzados), entradas
- Formato de sistemas avanzados (ASF),streams
- ASF (formato de sistemas avanzados), secuencias
- Formato de sistemas avanzados (ASF), salidas
- ASF (formato de sistemas avanzados), salidas
- Formato de sistemas avanzados (ASF), formatos
- ASF (formato de sistemas avanzados),formatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10f217b9935926d7bd7d5cba9ac53e6834385685e4a0f87ea6ba713cc8ff70b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089695"
---
# <a name="formats"></a>Formatos

La información en un formato describe todo lo que necesita saber sobre un tipo determinado de medios. Cada formato tiene un tipo principal, como audio o vídeo, y puede tener un subtipo. Los formatos contienen información diferente basada en el tipo principal. Los formatos de audio y vídeo requieren mucha más información que otros tipos.

Del mismo modo que los objetos del SDK de formato multimedia de Windows diferencian entre números de entrada, números de flujo y números de salida (consulte [Entradas, Secuencias y Salidas),](inputs-streams-and-outputs.md)hay diferencias importantes entre los formatos de entrada, los formatos de secuencia y los formatos de salida. Estas diferencias se describen aquí:

## <a name="input-formats"></a>Formatos de entrada

Un formato de entrada describe los medios digitales que se pasan al objeto de escritor. Si una secuencia de un archivo ASF se comprime con un códec, el códec solo admitirá determinados formatos de entrada. Al usar los códecs Windows audio multimedia y vídeo, puede enumerar los formatos de entrada admitidos mediante el objeto de escritor. Al escribir un archivo, es responsable de seleccionar un formato de entrada que coincida con el medio de entrada.

Aunque el códec que comprimirá los datos debe ser compatible con el formato de los medios de entrada, algunas configuraciones de formato de entrada no tienen que coincidir con el formato de secuencia. Por ejemplo, el formato de entrada de una secuencia de vídeo puede tener un tamaño de fotograma diferente del definido en el formato de secuencia. El códec realizará conversiones en estos casos.

## <a name="stream-formats"></a>Formatos de secuencia

Un formato de secuencia describe la forma del medio tal como se almacena en el archivo ASF. El formato de secuencia es el formato descrito en el perfil y puede ser o no el mismo que el formato de entrada y el formato de salida. Si se usa un códec para comprimir los datos de una secuencia, el formato de secuencia será diferente de los formatos de entrada y salida.

Al usar los códecs Windows Media Audio y Video, debe obtener una lista de formatos de secuencia admitidos del códec para asegurarse de que no está intentando especificar un formato que el código no admite. Algunas opciones de formato, como el tamaño y la profundidad de color de un fotograma de vídeo, deben configurarse manualmente después de recuperar el formato de códec.

## <a name="output-formats"></a>Formatos de salida

Un formato de salida describe los medios digitales que el lector (o lector sincrónico) entrega a la aplicación. Si una secuencia de un archivo ASF se comprime con un códec, el códec solo admitirá determinados formatos de salida. Al usar los códecs Windows audio multimedia y vídeo, puede enumerar los formatos de salida admitidos mediante el objeto lector. Cada uno de los códecs Windows media tiene un formato de salida predeterminado, pero puede seleccionar cualquier formato de salida compatible para la entrega de ejemplo.

Aunque el códec que comprimió los datos debe ser compatible con el formato del medio de salida, algunas configuraciones de formato de salida no deben coincidir con el formato de secuencia. Por ejemplo, el formato de salida de una secuencia de vídeo puede tener un tamaño de fotograma diferente del definido en el formato de secuencia. El códec realizará conversiones en estos casos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Conceptos**](concepts.md)
</dt> </dl>

 

 




