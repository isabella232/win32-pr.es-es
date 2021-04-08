---
title: Escribir secuencias de imagen
description: Escribir secuencias de imagen
ms.assetid: 3a017bdd-9723-4b7f-b5e1-22838c0ba4ff
keywords:
- Advanced Systems Format (ASF), escribir secuencias de imágenes
- ASF (formato de sistemas avanzados), escribir secuencias de imágenes
- Advanced Systems Format (ASF), stream Image
- ASF (formato de sistemas avanzados), flujos de imagen
- flujos de imagen, escritura
- secuencias, escribir secuencias de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60daa9b62701c172d127c4cff1fb6c301edf7d86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994950"
---
# <a name="writing-image-streams"></a>Escribir secuencias de imagen

Las entradas de un flujo de imagen deben ser imágenes de mapa de bits con formato RGB. El escritor coordina la compresión de los ejemplos de imagen de entrada con el formato JPEG. Antes de empezar a escribir un archivo que contiene una secuencia de imagen, debe establecer una calidad de imagen para la entrada mediante el \_ valor g wszJPEGCompressionQuality. Use [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) para establecer la calidad en un valor **DWORD** comprendido entre 1 y 100. Los valores bajos representan una alta relación de compresión a costa de la calidad, mientras que los valores altos producen imágenes de alta calidad que requieren más espacio.

Los flujos de imágenes suelen requerir ventanas de búfer más grandes que las secuencias de vídeo normales. El tamaño exacto necesario depende del tipo de imagen y de la calidad de la imagen, entre otros factores. Use la prueba y el error para determinar el tamaño adecuado para las imágenes que desea procesar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Flujos de imagen**](image-streams.md)
</dt> <dt>

[**Para establecer la configuración de entrada**](to-set-input-settings.md)
</dt> <dt>

[**Escribir archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




