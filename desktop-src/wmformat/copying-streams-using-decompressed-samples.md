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
ms.openlocfilehash: 88c5c0f98b02090d98814983ad518ee3cd7e5d8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466725"
---
# <a name="copying-streams-using-decompressed-samples"></a>Copia de Secuencias mediante ejemplos descomprimidos

Se recomienda encarecidamente no copiar secuencias de un archivo a otro mediante ejemplos descomprimidos. El proceso de descompresión y recompresión de muestras degradará la calidad de la salida. Si necesita descomprimir los ejemplos y, a continuación, copiarlos en otra secuencia, puede encontrar cierta dificultad con las secuencias codificadas con velocidad de bits variable basada en calidad (VBR).

Cuando el códec termina de comprimir una secuencia de VBR basada en calidad, registra la velocidad de bits y la ventana de búfer del contenido resultante. Al leer un archivo que contiene una secuencia codificada con VBR basado en calidad, el perfil obtenido del lector tendrá en cuenta la velocidad de bits y la ventana de búfer, así como la velocidad de bits máxima y la ventana de búfer máxima. Esta configuración en el perfil normalmente significa una secuencia de velocidad de bits variable restringida. Como resultado, al establecer el perfil en el sistema de escritura, esperará un paso de preprocesamiento para la secuencia, ya que las secuencias de VBR restringidas de velocidad de bits requieren codificación de dos pases. Debe tratar la secuencia como si fuera una secuencia de VBR restringida de velocidad de bits y entregar los ejemplos para el preprocesamiento. Dado que usa los valores devueltos después de codificar el contenido en un nivel de calidad determinado, esos valores representan el nivel de calidad deseado. Por supuesto, la calidad de la salida codificada de nuevo se degradará de todos modos, como resultado de la nueva codificación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Copiar datos de un archivo a otro**](copying-data-from-one-file-to-another.md)
</dt> <dt>

[**Copiar Secuencias sin descomprimir los datos**](copying-streams-without-decompressing-the-data.md)
</dt> </dl>

 

 




