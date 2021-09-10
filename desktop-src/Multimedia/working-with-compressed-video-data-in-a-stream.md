---
title: Trabajar con datos de vídeo comprimidos en una secuencia
description: Trabajar con datos de vídeo comprimidos en una secuencia
ms.assetid: b701e072-f162-438f-b607-aea7491a02f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0587ee6c12a93eb014368642ba1605f546129e0
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372475"
---
# <a name="working-with-compressed-video-data-in-a-stream"></a>Trabajar con datos de vídeo comprimidos en una secuencia

AVIFile proporciona varias maneras de acceder a secuencias de vídeo comprimidas.

Si desea mostrar uno o varios fotogramas de una secuencia de vídeo comprimida, puede recuperar los fotogramas mediante la función [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) y reenviar los datos del fotograma comprimido a las funciones DrawDib para mostrarlos. Las funciones DrawDib pueden mostrar imágenes de varias profundidades de imagen y ditrae automáticamente imágenes para pantallas que no pueden controlar determinados tipos de mapas de bits independientes del dispositivo (DIB). Estas funciones funcionan con imágenes sin comprimir y comprimidas. Para obtener más información sobre las funciones DrawDib, vea [Funciones DrawDib](drawdib-functions.md).

AVIFile proporciona funciones para descomprimir un único fotograma de vídeo. Para asignar recursos, use la [**función AVIStreamGetFrameOpen.**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) Esta función crea un búfer para los datos descomprimidos.

Puede descomprimir un único fotograma de vídeo mediante la [**función AVIStreamGetFrame.**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) Esta función descomprime el marco y recupera un fotograma completo de datos de imagen, devolviendo la dirección de la DIB en la [estructura BITMAPINFOHEADER.](/previous-versions//ms532290(v=vs.85)) La aplicación puede mostrar la DIB mediante funciones de dibujo estándar o mediante las funciones DrawDib.

Si la aplicación realiza llamadas sucesivas a **AVIStreamGetFrame,** la función sobrescribe su búfer con cada fotograma recuperado.

Cuando termine de usar **AVIStreamGetFrame** y la DIB descomprimida esté en su búfer, puede liberar los recursos asignados mediante la [**función AVIStreamGetFrameClose.**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose)

Para obtener más información sobre la descompresión de imágenes, vea [Administrador de compresión de vídeo](video-compression-manager.md).

 

 