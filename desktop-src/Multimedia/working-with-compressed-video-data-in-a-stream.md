---
title: Trabajar con datos de vídeo comprimidos en un flujo
description: Trabajar con datos de vídeo comprimidos en un flujo
ms.assetid: b701e072-f162-438f-b607-aea7491a02f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0587ee6c12a93eb014368642ba1605f546129e0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077646"
---
# <a name="working-with-compressed-video-data-in-a-stream"></a>Trabajar con datos de vídeo comprimidos en un flujo

AVIFile proporciona varias maneras de tener acceso a las secuencias de vídeo comprimidas.

Si desea mostrar uno o varios fotogramas de un flujo de vídeo comprimido, puede recuperar los fotogramas mediante la función [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) y reenviar los datos del marco comprimido a las funciones DrawDib para mostrarlos. Las funciones DrawDib pueden mostrar imágenes de varias profundidades de imagen y tramas automáticas de imágenes para las pantallas que no pueden controlar determinados tipos de mapas de bits independientes del dispositivo (DIB). Estas funciones funcionan con imágenes sin comprimir y comprimidas. Para obtener más información sobre las funciones de DrawDib, consulte [funciones de DrawDib](drawdib-functions.md).

AVIFile proporciona funciones para descomprimir un solo fotograma de vídeo. Para asignar recursos, use la función [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) . Esta función crea un búfer para los datos descomprimidos.

Puede descomprimir un solo fotograma de vídeo mediante la función [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) . Esta función descomprime el marco y recupera un marco completo de datos de imagen, y devuelve la dirección del DIB en la estructura [BITMAPINFOHEADER](/previous-versions//ms532290(v=vs.85)) . La aplicación puede mostrar el DIB mediante funciones de dibujo estándar o mediante las funciones de DrawDib.

Si la aplicación realiza llamadas sucesivas a **AVIStreamGetFrame**, la función sobrescribe su búfer con cada fotograma recuperado.

Cuando termine de usar **AVIStreamGetFrame** y el DIB descomprimido está en su búfer, puede liberar los recursos asignados mediante la función [**AVIStreamGetFrameClose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose) .

Para obtener más información sobre la descompresión de imágenes, consulte [Administrador de compresión de vídeo](video-compression-manager.md).

 

 