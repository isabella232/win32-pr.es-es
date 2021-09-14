---
description: Los métodos Image::Save Methods e Image::SaveAdd Methods de la clase Image reciben un objeto EncoderParameters que contiene una matriz de objetos EncoderParameter.
ms.assetid: babc89f0-aea5-4341-8cf9-40d11e73fb10
title: Constantes del codificador de imágenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8130b90ad7f1d559ca480a581a0b157ff152fc0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170273"
---
# <a name="image-encoder-constants"></a>Constantes del codificador de imágenes

Los [métodos Image::Save Methods](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) e [Image::SaveAdd Methods](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) de la clase [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) reciben un objeto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) que contiene una matriz [**de objetos EncoderParameter.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) Cada **objeto EncoderParameter** tiene un miembro de datos GUID que especifica la categoría de parámetro. Las siguientes constantes, definidas en Gdiplusimaging.h, representan GUID que especifican las distintas categorías de parámetros.

-   EncoderChrominanceTable
-   EncoderColorDepth
-   EncoderColorSpace
-   EncoderCompression
-   EncoderLuminanceTable
-   EncoderQuality
-   EncoderRenderMethod
-   EncoderSaveFlag
-   EncoderScanMethod
-   EncoderTransformation
-   EncoderVersion
-   EncoderImageItems
-   EncoderSaveAs ENCODER

 

 
