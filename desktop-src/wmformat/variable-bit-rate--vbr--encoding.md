---
title: Codificación de velocidad de bits variable (VBR)
description: Codificación de velocidad de bits variable (VBR)
ms.assetid: d3fe0cc6-64d7-44ce-8bb4-dd2eed021345
keywords:
- SDK de Windows Media Format, codificación VBR
- Windows Media Format SDK, velocidad de bits variable (VBR)
- SDK de Windows Media Format, codificación VBR basada en la calidad
- SDK de Windows Media Format, codificación VBR sin restricciones
- SDK de Windows Media Format, codificación VBR restringida
- códecs, codificación VBR
- códecs, velocidad de bits variable (VBR)
- códecs, codificación VBR basada en la calidad
- códecs, codificación VBR sin restricciones
- códecs, codificación VBR restringida
- velocidad de bits variable (VBR), acerca de
- VBR (velocidad de bits variable), acerca de
- codificación VBR basada en la calidad, acerca de
- codificación VBR no restringida, acerca de
- codificación VBR restringida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b24a32b693cc4801f95695cc2d6e5f9ffa400c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714253"
---
# <a name="variable-bit-rate-vbr-encoding"></a>Codificación de velocidad de bits variable (VBR)

La codificación de velocidad de bits variable (VBR) es una alternativa a la codificación de velocidad de bits constante (CBR) y es compatible con algunos códecs. Cuando la codificación CBR se esfuerza por mantener la velocidad de bits de los medios codificados, VBR se esfuerza por lograr la mejor calidad posible de los medios codificados.

La calidad del contenido codificado se determina por la cantidad de datos que se pierden al comprimir o descomprimir el contenido. Hay varios factores que afectan a la pérdida de datos en el proceso de compresión, pero generalmente cuanto más complejos sean los datos originales y mayor sea la razón de compresión, más detalle se perderá en el proceso de compresión.

Hay tres tipos de codificación VBR: basado en la calidad, sin restricciones y restringidos.

## <a name="quality-based-vbr-encoding"></a>Codificación VBR basada en la calidad

El primer tipo de codificación VBR está basado en la calidad, que usa un paso de codificación. La codificación VBR basada en la calidad permite especificar un nivel de calidad para una secuencia de medios digitales en lugar de una velocidad de bits. El códec codificará el contenido para que todos los ejemplos sean de calidad comparable.

La principal ventaja de la codificación VBR basada en la calidad es que la calidad es coherente dentro de un archivo y de un archivo al siguiente. Por ejemplo, puede escribir un programa para copiar canciones de archivos de CD a ASF en un equipo. En este caso, la calidad coherente es probablemente más importante para la experiencia del usuario final que el tamaño de archivo coherente. El uso de la codificación VBR basada en la calidad garantiza que todas las canciones copiadas tengan la misma calidad.

La desventaja de la codificación VBR basada en la calidad es que no hay ninguna manera de conocer los requisitos de tamaño o ancho de banda de los medios codificados antes de la codificación. Esto puede hacer que los archivos de codificación VBR basados en la calidad sean inadecuados para las circunstancias en las que la memoria o el ancho de banda están restringidos, como reproductores multimedia portátiles o conexiones a Internet de ancho de banda bajo.

En general, la codificación VBR basada en la calidad es idónea para la reproducción local o las conexiones de red de ancho de banda alto. En esos casos, la calidad coherente proporcionará una mejor experiencia de usuario.

## <a name="unconstrained-vbr-encoding"></a>Codificación VBR sin restricciones

La codificación VBR sin restricciones utiliza dos fases de codificación. Cuando se usa la codificación VBR sin restricciones, se especifica una velocidad de bits para la secuencia, como lo haría con la codificación CBR. Sin embargo, el códec usa este valor solo como la velocidad de bits promedio para la secuencia y se codifica para que la calidad sea lo más alta posible mientras se mantiene el promedio. La velocidad de bits real en cualquier punto de la secuencia codificada puede variar considerablemente respecto al valor medio.

No se establece una ventana de búfer para la codificación VBR sin restricciones como se haría con una secuencia con codificación CBR. En su lugar, el códec calcula el tamaño de la ventana de búfer necesaria en función de los requisitos de los ejemplos codificados.

La ventaja de la codificación VBR no restringida es que el flujo comprimido tiene la máxima calidad posible y permanece dentro de un ancho de banda medio predecible.

## <a name="constrained-vbr-encoding"></a>Codificación VBR restringida

La codificación VBR restringida es idéntica a la codificación VBR sin restricciones, salvo que se especifica una velocidad de bits máxima y una ventana de búfer máxima en el perfil. A continuación, el códec usa los valores máximos para determinar cómo comprimir los datos. Si establece los valores máximos lo suficientemente altos, la codificación VBR restringida producirá la misma secuencia codificada que la codificación VBR sin restricciones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Elección de un método de codificación**](choosing-an-encoding-method.md)
</dt> <dt>

[**Características del códec**](codec-features.md)
</dt> <dt>

[**Configuración de secuencias**](configuring-streams.md)
</dt> <dt>

[**Configuración de secuencias VBR**](configuring-vbr-streams.md)
</dt> <dt>

[**Codificación de velocidad de bits constante (CBR)**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**Codificación de dos pasos**](two-pass-encoding.md)
</dt> <dt>

[**Uso de la codificación de Two-Pass**](using-two-pass-encoding.md)
</dt> </dl>

 

 




