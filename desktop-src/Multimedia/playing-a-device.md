---
title: Reproducir un dispositivo
description: Reproducir un dispositivo
ms.assetid: 48d83e06-9e6e-498b-ad9b-0b66f235db25
keywords:
- Comando MCI_PLAY
- MCIAVI ventana de reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73d8b6539e842a1ffa632ed1efae5c2c8d3cda1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995254"
---
# <a name="playing-a-device"></a>Reproducir un dispositivo

El comando [**Play**](play.md) ([**MCI \_ Play**](mci-play.md)) empieza a reproducir un dispositivo. Sin marcas, este comando empieza a reproducirse desde la posición actual y se reproduce hasta que se interrumpe el comando o hasta que se alcanza el final del medio o el archivo. Después de la reproducción, la posición actual se encuentra al final del medio. También puede usar el comando [**Seek**](seek.md) ([**MCI \_ Seek**](mci-seek.md)) para cambiar la posición actual.

La mayoría de los dispositivos que admiten el comando **Play** también admiten las marcas "desde" (MCI \_ desde) y "hasta" (MCI \_ hasta). Estas marcas indican la posición en la que el dispositivo debe iniciarse y dejar de reproducirse. Por ejemplo, el siguiente comando reproduce un disco de audio de CD desde el principio de la primera pista mediante la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :


```C++
mciSendString("play cdaudio from 0", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



Algunos tipos de dispositivos amplían este comando para aprovechar las capacidades de un dispositivo determinado. Por ejemplo, el comando [**reproducir**](play.md) para el tipo de dispositivo de **videodisco** incluye las marcas "rápida" (MCI \_ Vd \_ Play \_ Fast), "lenta" (MCI \_ Vd \_ Play \_ Slow) y "SCAN" (MCI \_ Vd \_ Play \_ Scan).

> [!Note]  
> Las unidades asignadas al valor de posición dependen del formato de hora que usa el dispositivo. Cada dispositivo tiene un formato de hora predeterminado, pero debe especificar el formato de hora mediante el comando [**set**](set.md) ([**\_ set de MCI**](mci-set.md)) antes de emitir cualquier comando que use valores de posición.

 

## <a name="playing-an-avi-file"></a>Reproducir un archivo AVI

Los archivos de vídeo en Windows se componen de al menos dos flujos de datos intercalados: una secuencia de vídeo (gráfica) y una secuencia de audio. Puede reproducir fácilmente estos archivos de audio y vídeo intercalado (AVI) mediante comandos MCI. En las secciones siguientes se describe la reproducción de archivos AVI.

## <a name="setting-up-an-mciavi-playback-window"></a>Configuración de una ventana de reproducción de MCIAVI

La aplicación puede especificar las siguientes opciones para definir la ventana de reproducción para reproducir un archivo AVI:

-   Use la ventana emergente predeterminada del controlador MCIAVI.
-   Especifique una ventana primaria y un estilo de ventana que el controlador MCIAVI pueda utilizar para crear la ventana de reproducción.
-   Especifique una ventana de reproducción para el controlador MCIAVI que se usará para la reproducción.
-   Reproducir el archivo AVI en una pantalla completa.

Si la aplicación no especifica ninguna opción de ventana, el controlador MCIAVI crea una ventana predeterminada para la reproducción de la secuencia. El controlador crea esta ventana de reproducción para el comando [**abrir**](open.md) ([**MCI \_ abierto**](mci-open.md)), pero no muestra la ventana hasta que la aplicación envía un comando para mostrar la ventana o reproducir el archivo. Esta ventana de reproducción predeterminada es una ventana emergente con un borde de ajuste de tamaño, una barra de título, un marco grueso, un menú **ventana** y un botón minimizar.

La aplicación también puede especificar un identificador de ventana principal y un estilo de ventana cuando emite el comando **abrir** . En este caso, el controlador MCIAVI crea una ventana basada en estas especificaciones en lugar de la ventana emergente predeterminada. La aplicación puede especificar cualquier estilo de ventana disponible para la función [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) . Los estilos que requieren una ventana primaria, como WS \_ Child, deben incluir un identificador de ventana principal.

La aplicación también puede crear su propia ventana y proporcionar el identificador al controlador MCIAVI mediante el comando [**Window**](window.md) ([**\_ ventana de MCI**](mci-window.md)). El controlador MCIAVI usa esta ventana en lugar de crear una propia.

Cuando el controlador MCIAVI crea la ventana de reproducción u obtiene un identificador de ventana de la aplicación, no muestra la ventana hasta que la aplicación reproduce la secuencia o bien envía un comando para mostrar la ventana. La aplicación puede usar el comando de **ventana** para mostrar la ventana sin reproducir la secuencia. Por ejemplo, el siguiente comando muestra la ventana mediante [**mciSendString**](/previous-versions//dd757161(v=vs.85)):


```C++
mciSendString("window movie state show", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



En este ejemplo, "Movie" es un alias para el dispositivo de vídeo digital.

La aplicación también puede reproducir una pantalla completa de archivos AVI. Para reproducir una pantalla completa, modifique el comando [**reproducir**](play.md) ([**MCI \_ Play**](mci-play.md)) con la marca "pantalla completa" (MCI \_ MCIAVI \_ Play \_ fullscreen). Cuando la aplicación usa esta marca, el controlador MCIAVI usa un formato de pantalla completa de 320 x 240 píxeles para reproducir la secuencia. Por ejemplo, el siguiente comando reproduce la pantalla completa del archivo abierto (con "Movie" como alias):


```C++
mciSendString("play movie fullscreen", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



## <a name="changing-the-playback-state-for-an-avi-file"></a>Cambiar el estado de reproducción de un archivo AVI

La aplicación puede usar el comando [**Buscar**](seek.md) ([**MCI \_ Seek**](mci-seek.md)) para mover la posición actual al principio, al final o a una posición arbitraria en un archivo AVI. Hay dos modos de búsqueda para el controlador MCIAVI: exacto e inexacto. La aplicación puede cambiar el modo de búsqueda mediante el comando [**set**](set.md) ([**\_ set de MCI**](mci-set.md)). Cuando se usa **set** "Seek Exactly on", el controlador MCIAVI busca exactamente en el marco que especifica la aplicación. Esto puede producir un retraso si el archivo se comprime temporalmente y la aplicación no especifica un fotograma clave. Cuando se usa **set** "Seek Exactly OFF", el controlador MCIAVI busca el fotograma clave más cercano en un archivo comprimido temporalmente.

Algunos comandos de MCI permiten que la aplicación modifique la reproducción de un archivo AVI de otras maneras. Por ejemplo, un archivo AVI se reproduce de forma predeterminada a su velocidad normal, pero la aplicación puede aumentar o disminuir esta velocidad mediante el uso de la marca "Speed" con el comando **set** . En el caso de los archivos AVI, es habitual un valor de velocidad de 1000. Por lo tanto, para reproducir una película a la mitad de su velocidad normal, la aplicación puede usar el **conjunto** de comandos "Movie Speed 500". como alternativa, puede usar **set** "Movie Speed 2000" para reproducir la secuencia a la doble velocidad normal.

El comando [**SetAudio**](setaudio.md) ([**MCI \_ SetAudio**](mci-setaudio.md)) permite que la aplicación controle la parte de audio de un archivo AVI. La aplicación puede silenciar el audio durante la reproducción o, en el caso de varios archivos de secuencia de audio, seleccionar la secuencia de audio que se reproduce.

El controlador MCIAVI tiene un cuadro de diálogo para controlar algunas de sus opciones de reproducción. Algunas de las opciones disponibles para el usuario incluyen la selección de reproducción orientada a ventanas o de pantalla completa, la selección del modo de búsqueda y la ampliación de la imagen. La aplicación puede tener MCIAVI Mostrar este cuadro de diálogo mediante el comando [**configurar**](configure.md) ([**MCI \_ Configure**](mci-configure.md)).

## <a name="stream-handlers"></a>Controladores de secuencias

Los datos de un archivo AVI se tratan como una serie de secuencias. Un archivo AVI normalmente contiene un flujo de audio y vídeo, y también puede haber un flujo personalizado que contiene texto u otros datos personalizados. El controlador MCIAVI puede usar controladores diferentes para estos flujos de datos. Para obtener más información sobre los archivos AVI personalizados, vea [controladores personalizados de archivos y secuencias](custom-file-and-stream-handlers.md).

 

 