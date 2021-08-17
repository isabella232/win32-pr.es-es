---
title: Copia de Secuencias mediante ejemplos descomprimidos
description: Copia de Secuencias mediante ejemplos descomprimidos
ms.assetid: 03ad8415-1dff-4362-94b4-7ec69c3e7888
keywords:
- Windows SDK de formato multimedia, copiar secuencias
- Formato de sistemas avanzados (ASF), copiar secuencias
- ASF (formato de sistemas avanzados), copiar secuencias
- streams,copying using decompressed data
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e044d2a1d456c14c2e2d069e0a117ab6f6de218c062771da9c24bf887ddfdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848811"
---
# <a name="copying-streams-using-decompressed-samples"></a>Copia de Secuencias mediante ejemplos descomprimidos

Se recomienda encarecidamente no copiar secuencias de un archivo a otro mediante muestras descomprimidas. El proceso de descompresión y recompresión de muestras degradará la calidad de la salida. Si necesita descomprimir los ejemplos y, a continuación, copiarlos en otra secuencia, puede encontrar cierta dificultad con las secuencias codificadas de velocidad de bits variable (VBR) basada en calidad.

Cuando el códec termina de comprimir una secuencia de VBR basada en la calidad, registra la velocidad de bits y la ventana de búfer del contenido resultante. Al leer un archivo que contiene una secuencia codificada con VBR basado en calidad, el perfil obtenido del lector tendrá en cuenta la velocidad de bits y la ventana de búfer, así como la velocidad de bits máxima y la ventana de búfer máxima. Esta configuración en el perfil normalmente significa un flujo de velocidad de bits variable restringida de velocidad de bits. Como resultado, al establecer el perfil en el sistema de escritura, se espera un paso de preprocesamiento para la secuencia, ya que las secuencias DE VBR restringidas de velocidad de bits requieren codificación de dos pases. Debe tratar la secuencia como si fuera una secuencia de VBR restringida de velocidad de bits y entregar los ejemplos para el preprocesamiento. Dado que usa los valores devueltos después de codificar el contenido en un nivel de calidad determinado, esos valores representan el nivel de calidad deseado. Por supuesto, la calidad de la salida codificada de todos modos se degradará ligeramente, como resultado de la nueva codificación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Copiar datos de un archivo a otro**](copying-data-from-one-file-to-another.md)
</dt> <dt>

[**Copiar Secuencias sin descomprimir los datos**](copying-streams-without-decompressing-the-data.md)
</dt> </dl>

 

 




