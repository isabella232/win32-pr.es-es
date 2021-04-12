---
title: Formatos
description: Formatos
ms.assetid: 7c602643-f1fc-4fbd-a739-4296dc758bc9
keywords:
- Windows Media Format SDK, entradas
- Windows Media Format SDK, secuencias
- Windows Media Format SDK, salidas
- Windows Media Format SDK, formatos
- Advanced Systems Format (ASF), INPUTS
- ASF (formato de sistemas avanzados), entradas
- Advanced Systems Format (ASF), streams
- ASF (formato de sistemas avanzados), secuencias
- Advanced Systems Format (ASF), salidas
- ASF (formato de sistemas avanzados), salidas
- Advanced Systems Format (ASF), Formats
- ASF (formato de sistemas avanzados), formatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e7895c27af3eb99e96d7009b79ea8df0011208
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357475"
---
# <a name="formats"></a>Formatos

La información en un formato describe todo lo que necesita saber sobre un tipo de medio determinado. Cada formato tiene un tipo principal, como audio o vídeo, y puede tener un subtipo. Los formatos contienen información diferente en función del tipo principal. Los formatos de audio y vídeo requieren mucha más información que otros tipos.

Del mismo modo que los objetos del SDK de Windows Media Format diferencian entre los números de entrada, los números de flujo y los números de salida (vea [entradas, secuencias y salidas](inputs-streams-and-outputs.md)), existen diferencias importantes entre los formatos de entrada, los formatos de flujo y los formatos de salida. Estas diferencias se describen aquí:

## <a name="input-formats"></a>Formatos de entrada

Un formato de entrada describe los medios digitales que se pasan al objeto escritor. Si una secuencia de un archivo ASF se comprime con un códec, el códec solo admitirá determinados formatos de entrada. Al usar los códecs de Windows Media Audio y vídeo, puede enumerar los formatos de entrada admitidos mediante el objeto escritor. Al escribir un archivo, usted es responsable de seleccionar un formato de entrada que coincida con los medios de entrada.

Aunque el formato del medio de entrada debe ser compatible con el códec que comprimirá los datos, es necesario que algunos valores de configuración de formato de entrada no coincidan con el formato de flujo. Por ejemplo, el formato de entrada de un flujo de vídeo puede tener un tamaño de fotograma diferente del definido en el formato de flujo. El códec realizará las conversiones en estos casos.

## <a name="stream-formats"></a>Formatos de secuencia

Un formato de secuencia describe la forma del medio tal como se almacena en el archivo ASF. El formato de flujo es el formato descrito en el perfil y puede o no ser el mismo que el formato de entrada y el formato de salida. Si se usa un códec para comprimir los datos de una secuencia, el formato del flujo será diferente de los formatos de entrada y salida.

Al usar los códecs de Windows Media Audio y vídeo, debe obtener una lista de formatos de secuencia compatibles del códec para asegurarse de que no está intentando especificar un formato no admitido por el código. Algunos valores de configuración de formato, como el tamaño y la profundidad de color de un fotograma de vídeo, deben configurarse manualmente una vez recuperado el formato del códec.

## <a name="output-formats"></a>Formatos de salida

Un formato de salida describe el medio digital que el lector (o lector sincrónico) entrega a la aplicación. Si una secuencia de un archivo ASF se comprime con un códec, el códec solo admitirá determinados formatos de salida. Al usar los códecs de Windows Media Audio y vídeo, puede enumerar los formatos de salida admitidos mediante el objeto lector. Cada uno de los códecs de Windows Media tiene un formato de salida predeterminado, pero puede seleccionar cualquier formato de salida compatible para la entrega de ejemplo.

Aunque el formato del medio de salida debe ser compatible con el códec que ha comprimido los datos, no es necesario que alguna configuración de formato de salida coincida con el formato de la secuencia. Por ejemplo, el formato de salida de una secuencia de vídeo puede tener un tamaño de fotograma diferente del definido en el formato de flujo. El códec realizará las conversiones en estos casos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Conceptos**](concepts.md)
</dt> </dl>

 

 




