---
description: Métodos de codificación
ms.assetid: 17ab5ecc-0173-4c5c-9d65-40e506ab7e07
title: Métodos de codificación (Microsoft Media Foundation)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4366f11ea9d120d638c5600f84fc16f6c5320f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714910"
---
# <a name="encoding-methods-microsoft-media-foundation"></a>Métodos de codificación (Microsoft Media Foundation)

La mayoría de los códecs de Windows Media Audio y vídeo admiten varios métodos de codificación. Saber cómo y Cuándo usar cada método puede ayudarle a crear contenido comprimido de alta calidad.

Los métodos de codificación se centran en el búfer usado por el descodificador para administrar los datos de entrada comprimidos. Este búfer se define por la velocidad de bits de la secuencia, en bits por segundo, y la ventana de búfer, en milisegundos. Al codificar, el códec se atiene a las restricciones del búfer. Para obtener más información sobre el búfer, vea [el modelo de búfer de depósitos con fugas](the-leaky-bucket-buffer-model.md).

## <a name="constant-bit-rate-encoding"></a>Codificación de velocidad de bits constante

La velocidad de bits de cualquier secuencia codificada mediante uno de los códecs de Windows Media Audio y vídeo no es constante. La codificación de velocidad de bits constante (CBR) es, por lo tanto, un término engañoso en cierto modo. La característica distintiva de una secuencia con codificación CBR es una pequeña ventana de búfer, que limita la variación de los tamaños de ejemplo. La codificación CBR se utiliza principalmente para el contenido que se transmite a través de una red a su destino. En este escenario, es importante poder confiar en el uso de ancho de banda coherente.

Desde el punto de vista de la configuración, la codificación CBR difiere de los demás modos en que antes de empezar a codificar, se establece la velocidad de bits promedio del contenido de salida y la ventana de búfer que se aplica a esa velocidad de bits. En otros modos, uno o ambos de estos valores son desconocidos al configurar el codificador y es calculado por el códec mientras se codifica. CBR es el modo de codificación estándar que usa Windows Media Encoder DMOs.

## <a name="two-pass-constant-bit-rate-encoding"></a>Two-Pass codificación de velocidad de bits constante

Estándar CBR solo usa un único paso de codificación. El contenido se proporciona como ejemplo de entrada y el códec comprime el contenido y devuelve ejemplos de salida. También es posible procesar dos ejemplos de entrada. En el primer paso, el códec realiza cálculos para optimizar la codificación para el contenido. En el segundo paso, el códec usa los datos recopilados durante el primer paso para codificar el contenido.

La codificación CBR de dos pasos tiene muchas ventajas. A menudo, proporciona mejoras de calidad significativas con respecto a la codificación CBR estándar sin cambiar ninguno de los requisitos de almacenamiento en búfer. Esto hace que este modo de codificación sea idóneo para el contenido que se transmite a través de una red. La única situación en la que no es viable usar CBR de dos pasos es cuando se codifica contenido desde un origen en directo y no se puede utilizar un segundo paso.

El tipo de medio de salida de una secuencia CBR de dos pasos es idéntico al de una secuencia CBR estándar; todavía se especifica la velocidad de bits y la ventana de búfer que se va a usar. Al configurar DMO, debe establecerlo para realizar dos pasos. Y debe notificar a DMO cuando haya terminado de enviar ejemplos para el primer paso.

## <a name="quality-based-variable-bit-rate-encoding"></a>Quality-Based codificación de velocidad de bits variable

Dado que la codificación CBR no mantiene realmente una velocidad de bits constante, la diferencia entre ella y la codificación de velocidad de bits variable (VBR) puede parecer un poco Hazy. La principal diferencia entre CBR y VBR es el tamaño de la ventana de búfer utilizada. Las secuencias con codificación VBR suelen tener ventanas de búfer grandes en comparación con las secuencias con codificación CBR. La VBR basada en la calidad no es una excepción, ya que no se define ninguna velocidad de bits ni ventana de búfer para ella. En su lugar, se establece un valor de calidad. A continuación, el códec intenta comprimir los datos para que la calidad de los medios codificados sea coherente a lo largo de su duración, independientemente de los requisitos de búfer del flujo resultante.

La VBR basada en la calidad utiliza un único paso de codificación y tiende a crear grandes flujos comprimidos. Una vez completada la codificación, el códec establece los requisitos de búfer para que el descodificador pueda descomprimir los datos. La secuencia VBR codificada no es adecuada para el streaming a través de una red, por lo que la VBR basada en la calidad debe usarse solo para escenarios de reproducción local (o descarga y reproducción).

## <a name="unconstrained-variable-bit-rate-encoding"></a>Codificación de velocidad de bits variable sin restricciones

A diferencia de VBR basada en la calidad, VBR no restringida no codifica en un nivel de calidad específico. En su lugar, codifica el contenido con la máxima calidad posible manteniendo una velocidad de bits especificada. La VBR sin restricciones utiliza dos fases de codificación y es similar a la de dos pasos CBR, salvo que no se especifica una configuración de ventana de búfer para la secuencia. Esto significa que no hay ningún límite en el tamaño de los ejemplos individuales de la secuencia, siempre que la velocidad de bits media sea menor o igual que el valor establecido.

La VBR sin restricción es de uso limitado, ya que hay pocos escenarios de reproducción que tienen requisitos para mantener sus requisitos de búfer. El códec puede establecer la ventana de búfer en el valor que sea necesario después de la codificación, lo que no le permite controlar el tamaño del búfer. En la mayoría de los casos, si no le preocupa el tamaño del búfer o la coherencia del uso de ancho de banda, debe usar VBR basada en la calidad.

## <a name="peak-constrained-variable-bit-rate-encoding"></a>Peak-Constrained codificación de velocidad de bits variable

El modo de codificación final es VBR máxima restringida. Al igual que VBR sin restricciones, este modo usa dos fases de codificación y codifica en una velocidad de bits especificada. Sin embargo, con VBR máxima restringida también se configura el valor máximo para la codificación. Los valores máximos son similares a los valores de configuración de búfer normales: hay una velocidad de bits máxima y una ventana de búfer máximo. El archivo está codificado para ajustarse a un búfer descrito por los valores máximos, con la condición de que la velocidad de bits media general de la secuencia sea igual o menor que el valor de velocidad de bits promedio que especifique.

La VBR restringida puede ser difícil de conceptualizar. Esta es la forma más sencilla de pensar en el modelo de almacenamiento en búfer usado. Supongamos que el flujo es un flujo CBR con la velocidad de bits máxima y la ventana de búfer máxima que se usan para definir el búfer. Normalmente, la velocidad de bits máxima es bastante alta. El codificador garantiza que el valor de velocidad de bits promedio esperado que indique se mantiene a lo largo de la duración de la secuencia. En un punto concreto de la secuencia, se garantiza que la velocidad de bits promedio es mayor que el tamaño de flujo total en bits dividido por la duración de la secuencia en segundos).

Considere el ejemplo siguiente: configure una secuencia con una velocidad de bits media de 16.000 bits por segundo, una velocidad de bits máxima de 48.000 bits por segundo y una ventana de búfer máximo de 3.000 (3 segundos). El tamaño del búfer usado para el flujo es de 144.000 bits (48.000 bits por segundo x 3 segundos), según lo determinen los valores máximos. El codificador comprime los datos para que se ajusten a ese búfer. Además, la velocidad de bits media de la secuencia debe ser de 16.000 o inferior. Si el codificador necesita realizar algunos ejemplos muy grandes para controlar un segmento complejo de contenido, puede aprovechar el tamaño de búfer grande. Sin embargo, otras partes de la secuencia deben codificarse a una velocidad de bits más baja para reducir el promedio hasta el nivel especificado.

La codificación VBR máxima limitada es útil para dispositivos de reproducción con una capacidad de búfer finita y algunas restricciones de velocidad de datos. Un ejemplo común es la codificación que se usa para los DVD.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar la codificación VBR](usingvbrencoding.md)
</dt> <dt>

[Códecs de Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



