---
title: Escritura de imágenes Secuencias
description: Escritura de imágenes Secuencias
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
ms.openlocfilehash: 60daa9b62701c172d127c4cff1fb6c301edf7d86
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570156"
---
# <a name="writing-image-streams"></a>Escritura de imágenes Secuencias

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

 

 




