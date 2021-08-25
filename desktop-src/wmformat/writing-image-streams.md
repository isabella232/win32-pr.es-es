---
title: Escribir imágenes Secuencias
description: Escribir imágenes Secuencias
ms.assetid: 3a017bdd-9723-4b7f-b5e1-22838c0ba4ff
keywords:
- Formato de sistemas avanzados (ASF), escritura de secuencias de imagen
- ASF (formato de sistemas avanzados), escribir secuencias de imágenes
- Formato de sistemas avanzados (ASF), secuencias de imagen
- ASF (formato de sistemas avanzados), secuencias de imagen
- secuencias de imágenes, escritura
- streams,writing image streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6061af2ff43cbeb3fe688b6533eee044036df029bdb7f7305af305c8d45084
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006305"
---
# <a name="writing-image-streams"></a>Escribir imágenes Secuencias

Las entradas de un flujo de imagen deben ser imágenes de mapa de bits con formato RGB. El sistema de escritura coordina la compresión de los ejemplos de imagen de entrada mediante el formato JPEG. Antes de empezar a escribir un archivo que contiene un flujo de imagen, debe establecer una calidad de imagen para la entrada, mediante la configuración \_ g wsz BOOKINGEGCompressionQuality. Use [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) para establecer la calidad en un **valor DWORD** que va de 1 a 100. Los valores bajos representan una relación de compresión alta a costa de la calidad, mientras que los valores altos generan imágenes de alta calidad que requieren más espacio.

Las secuencias de imágenes a menudo requieren ventanas de búfer más grandes que las secuencias de vídeo normales. El tamaño exacto necesario depende del tipo de imagen y la calidad de la imagen, entre otros factores. Use la prueba y el error para determinar el tamaño adecuado de las imágenes que desea procesar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Imagen Secuencias**](image-streams.md)
</dt> <dt>

[**Para establecer la entrada Configuración**](to-set-input-settings.md)
</dt> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




