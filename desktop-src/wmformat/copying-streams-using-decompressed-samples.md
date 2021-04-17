---
title: Copiar secuencias mediante ejemplos descomprimidos
description: Copiar secuencias mediante ejemplos descomprimidos
ms.assetid: 03ad8415-1dff-4362-94b4-7ec69c3e7888
keywords:
- SDK de Windows Media Format, copiar flujos
- Advanced Systems Format (ASF), copiar flujos
- ASF (formato de sistemas avanzados), copiar flujos
- flujos, copiar mediante datos descomprimidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c5c0f98b02090d98814983ad518ee3cd7e5d8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704773"
---
# <a name="copying-streams-using-decompressed-samples"></a>Copiar secuencias mediante ejemplos descomprimidos

Se recomienda encarecidamente no copiar flujos de un archivo a otro mediante ejemplos descomprimidos. El proceso de descomprimir y volver a comprimir los ejemplos degradará la calidad de la salida. Si necesita descomprimir los ejemplos y copiarlos después en otro flujo, puede encontrarse con cierta dificultad con secuencias codificadas de velocidad de bits variable (VBR) basadas en la calidad.

Cuando el códec termina de comprimir una secuencia VBR basada en la calidad, registra la velocidad de bits y la ventana de búfer del contenido resultante. Cuando se lee un archivo que contiene una secuencia codificada con VBR basada en la calidad, el perfil obtenido del lector observará la velocidad de bits y la ventana del búfer, así como las ventanas velocidad de bits máxima y búfer máximo. Esta configuración en el perfil normalmente significa un flujo de velocidad de bits variable restringido de velocidad de bits. Como resultado, cuando se establece el perfil en el escritor, se espera un paso de preprocesamiento para el flujo, ya que las secuencias VBR con restricción de velocidad de bits requieren codificación de dos pasos. Debe tratar el flujo como si fuera una secuencia VBR restringida de velocidad de bits y ofrecer los ejemplos para el preprocesamiento. Dado que está usando los valores devueltos después de codificar el contenido en un nivel de calidad determinado, esos valores representan el nivel de calidad deseado. Por supuesto, la calidad de la salida recodificada se degradará en cierto modo, como resultado de la recodificación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Copiar datos de un archivo a otro**](copying-data-from-one-file-to-another.md)
</dt> <dt>

[**Copiar secuencias sin descomprimir los datos**](copying-streams-without-decompressing-the-data.md)
</dt> </dl>

 

 




