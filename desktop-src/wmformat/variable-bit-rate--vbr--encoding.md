---
title: Codificación de velocidad de bits variable (VBR)
description: Codificación de velocidad de bits variable (VBR)
ms.assetid: d3fe0cc6-64d7-44ce-8bb4-dd2eed021345
keywords:
- Windows SDK de formato multimedia, codificación VBR
- Windows SDK de formato multimedia, velocidad de bits variable (VBR)
- Windows SDK de formato multimedia, codificación VBR basada en calidad
- Windows SDK de formato multimedia, codificación VBR sin restricciones
- Windows SDK de formato multimedia, codificación VBR restringida
- códecs, codificación VBR
- codecs,velocidad de bits variable (VBR)
- códecs, codificación VBR basada en calidad
- códecs, codificación VBR sin restricciones
- códecs, codificación VBR restringida
- velocidad de bits variable (VBR),about
- VBR (velocidad de bits variable), acerca de
- codificación VBR basada en calidad, acerca de
- codificación VBR sin restricciones, acerca de
- codificación VBR restringida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c7a6fdb8b5f860bdbf00ff07b6752e7233462bf41e21d78717118242a96f2ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653865"
---
# <a name="variable-bit-rate-vbr-encoding"></a>Codificación de velocidad de bits variable (VBR)

La codificación de velocidad de bits variable (VBR) es una alternativa a la codificación de velocidad de bits constante (CBR) y es compatible con algunos códecs. Cuando la codificación CBR se esfuerza por mantener la velocidad de bits de los medios codificados, VBR se esfuerza por lograr la mejor calidad posible de los medios codificados.

La calidad del contenido codificado se determina por la cantidad de datos que se pierden al comprimir o descomprimir el contenido. Hay varios factores que afectan a la pérdida de datos en el proceso de compresión, pero generalmente cuanto más complejos sean los datos originales y mayor sea la razón de compresión, más detalle se perderá en el proceso de compresión.

Hay tres tipos de codificación VBR: basada en la calidad, sin restricciones y restringida.

## <a name="quality-based-vbr-encoding"></a>Codificación VBR basada en calidad

El primer tipo de codificación de VBR se basa en la calidad, que usa un paso de codificación. La codificación VBR basada en la calidad permite especificar un nivel de calidad para un flujo multimedia digital en lugar de una velocidad de bits. A continuación, el códec codificará el contenido para que todas las muestras sean de una calidad comparable.

La principal ventaja de la codificación VBR basada en la calidad es que la calidad es coherente dentro de un archivo y de un archivo al siguiente. Por ejemplo, puede escribir un programa para copiar canciones de CD a archivos ASF en un equipo. En este caso, la calidad coherente es probablemente más importante para la experiencia del usuario final que el tamaño de archivo coherente. El uso de la codificación VBR basada en la calidad garantizaría que todas las canciones copiadas sean de la misma calidad.

La desventaja de la codificación VBR basada en calidad es que realmente no hay ninguna manera de conocer los requisitos de tamaño o ancho de banda del medio codificado antes de la codificación. Esto puede hacer que los archivos codificados con VBR basados en calidad sean inadecuados en circunstancias en las que la memoria o el ancho de banda están restringidos, como reproductores multimedia portátiles o conexiones a Internet de ancho de banda bajo.

En general, la codificación VBR basada en la calidad es adecuada para la reproducción local o las conexiones de red de ancho de banda alto. En esos casos, la calidad coherente proporcionará una mejor experiencia de usuario.

## <a name="unconstrained-vbr-encoding"></a>Codificación VBR sin restricciones

La codificación VBR sin restricciones usa dos pases de codificación. Cuando se usa la codificación VBR sin restricciones, se especifica una velocidad de bits para la secuencia, como lo haría con la codificación CBR. Sin embargo, el códec usa este valor solo como velocidad de bits media para la secuencia y codifica para que la calidad sea lo más alta posible mientras se mantiene el promedio. La velocidad de bits real en cualquier punto de la secuencia codificada puede variar considerablemente con respecto al valor medio.

No se establece una ventana de búfer para la codificación VBR sin restricciones como lo haría para una secuencia codificada por CBR. En su lugar, el códec calcula el tamaño de la ventana de búfer necesaria en función de los requisitos de las muestras codificadas.

La ventaja de la codificación VBR sin restricciones es que la secuencia comprimida tiene la mayor calidad posible mientras se mantiene dentro de un ancho de banda medio predecible.

## <a name="constrained-vbr-encoding"></a>Codificación de VBR restringida

La codificación VBR restringida es idéntica a la codificación VBR sin restricciones, salvo que se especifica una velocidad de bits máxima y una ventana de búfer máxima en el perfil. A continuación, el códec usa los valores máximos para determinar cómo comprimir los datos. Si establece los valores máximos lo suficientemente altos, la codificación VBR restringida producirá la misma secuencia codificada que la codificación VBR sin restricciones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Elegir un método de codificación**](choosing-an-encoding-method.md)
</dt> <dt>

[**Características de códec**](codec-features.md)
</dt> <dt>

[**Configuración de Secuencias**](configuring-streams.md)
</dt> <dt>

[**Configuración de vbr Secuencias**](configuring-vbr-streams.md)
</dt> <dt>

[**Codificación de velocidad de bits constante (CBR)**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**Codificación de dos pases**](two-pass-encoding.md)
</dt> <dt>

[**Uso de Two-Pass codificación**](using-two-pass-encoding.md)
</dt> </dl>

 

 




