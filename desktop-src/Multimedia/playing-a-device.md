---
title: Reproducir un dispositivo
description: Reproducir un dispositivo
ms.assetid: 48d83e06-9e6e-498b-ad9b-0b66f235db25
keywords:
- MCI_PLAY comando
- Ventana de reproducción de MCIAVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9efc06b3d5f33dfb798aa4c47bf7d5a7a8bab45842de1da170c860d2a4a5f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372646"
---
# <a name="playing-a-device"></a>Reproducir un dispositivo

El [**comando play**](play.md) [**(MCI \_ PLAY)**](mci-play.md)comienza a reproducir un dispositivo. Sin marcas, este comando comienza a reproducirse desde la posición actual y se reproduce hasta que se interrumpe el comando o hasta que se alcanza el final del archivo o del medio. Después de la reproducción, la posición actual está al final del medio. También puede usar el [**comando seek**](seek.md) [**(MCI \_ SEEK)**](mci-seek.md)para cambiar la posición actual.

La mayoría de los dispositivos que admiten el comando **play** también admiten las marcas "from" (MCI \_ FROM) y "to" (MCI \_ TO). Estas marcas indican la posición en la que el dispositivo debe iniciarse y dejar de reproducirse. Por ejemplo, el comando siguiente reproduce un disco de audio de CD desde el principio de la primera pista mediante la [**función mciSendString:**](/previous-versions//dd757161(v=vs.85))


```C++
mciSendString("play cdaudio from 0", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



Algunos tipos de dispositivo amplían este comando para aprovechar las funcionalidades de un dispositivo determinado. Por ejemplo, el comando [**play**](play.md) para el tipo de dispositivo **videodisc** incluye las marcas "fast" (MCI \_ VD PLAY \_ \_ FAST), "slow" (MCI VD PLAY SLOW) y \_ \_ \_ "scan" (MCI \_ VD PLAY \_ \_ SCAN).

> [!Note]  
> Las unidades asignadas al valor de posición dependen del formato de tiempo utilizado por el dispositivo. Cada dispositivo tiene un formato de hora predeterminado, pero debe especificar el formato de hora mediante el comando [**set**](set.md) ([**MCI \_ SET**](mci-set.md)) antes de emitir cualquier comando que use valores de posición.

 

## <a name="playing-an-avi-file"></a>Reproducir un archivo AVI

Los archivos de Windows están integrados por al menos dos flujos de datos intercalados: una secuencia de vídeo (imagentorial) y una secuencia de audio. Puede reproducir fácilmente estos archivos de audio y vídeo intercalado (AVI) mediante comandos de MCI. En las secciones siguientes se describe la reproducción de archivos AVI.

## <a name="setting-up-an-mciavi-playback-window"></a>Configuración de una ventana de reproducción de MCIAVI

La aplicación puede especificar las siguientes opciones para definir la ventana de reproducción para reproducir un archivo AVI:

-   Use la ventana emergente predeterminada del controlador MCIAVI.
-   Especifique una ventana primaria y un estilo de ventana que el controlador MCIAVI pueda usar para crear la ventana de reproducción.
-   Especifique una ventana de reproducción para el controlador MCIAVI que se usará para la reproducción.
-   Reproducir el archivo AVI en una pantalla completa.

Si la aplicación no especifica ninguna opción de ventana, el controlador MCIAVI crea una ventana predeterminada para reproducir la secuencia. El controlador crea esta [](open.md) ventana de reproducción para el comando open [**(MCI \_ OPEN),**](mci-open.md)pero no muestra la ventana hasta que la aplicación envía un comando para mostrar la ventana o reproducir el archivo. Esta ventana de reproducción predeterminada es una ventana emergente con un borde  de ajuste de tamaño, una barra de título, un marco grueso, un menú de ventana y un botón Minimizar.

La aplicación también puede especificar un identificador de ventana principal y un estilo de ventana cuando emite el **comando open.** En este caso, el controlador MCIAVI crea una ventana basada en estas especificaciones en lugar de la ventana emergente predeterminada. La aplicación puede especificar cualquier estilo de ventana disponible para la [función CreateWindow.](/windows/win32/api/winuser/nf-winuser-createwindowa) Los estilos que requieren una ventana primaria, como WS \_ CHILD, deben incluir un identificador de ventana primario.

La aplicación también puede crear su propia ventana y proporcionar el identificador al controlador MCIAVI mediante el comando [**window**](window.md) ([**MCI \_ WINDOW**](mci-window.md)). El controlador MCIAVI usa esta ventana en lugar de crear una propia.

Cuando el controlador MCIAVI crea la ventana de reproducción u obtiene un identificador de ventana de la aplicación, no muestra la ventana hasta que la aplicación reproduce la secuencia o envía un comando para mostrar la ventana. La aplicación puede usar el comando **de** ventana para mostrar la ventana sin reproducir la secuencia. Por ejemplo, el comando siguiente muestra la ventana mediante [**mciSendString**](/previous-versions//dd757161(v=vs.85)):


```C++
mciSendString("window movie state show", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



En este ejemplo, "movie" es un alias para el dispositivo de vídeo digital.

La aplicación también puede reproducir un archivo AVI a pantalla completa. Para reproducir pantalla completa, modifique el comando [**play**](play.md) [**(MCI \_ PLAY)**](mci-play.md)con la marca "fullscreen" (MCI \_ MCIAVI \_ PLAY \_ FULLSCREEN). Cuando la aplicación usa esta marca, el controlador MCIAVI usa un formato de pantalla completa de 320 por 240 píxeles para reproducir la secuencia. Por ejemplo, el comando siguiente reproduce el archivo abierto a pantalla completa (con "movie" como alias):


```C++
mciSendString("play movie fullscreen", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



## <a name="changing-the-playback-state-for-an-avi-file"></a>Cambiar el estado de reproducción de un archivo AVI

La aplicación puede usar el comando [**seek**](seek.md) [**(MCI \_ SEEK)**](mci-seek.md)para mover la posición actual al principio, al final o a una posición arbitraria en un archivo AVI. Hay dos modos de búsqueda para el controlador MCIAVI: exacto e inexacto. La aplicación puede cambiar el modo de búsqueda mediante el [**comando set**](set.md) ([**MCI \_ SET**](mci-set.md)). Cuando se usa **el conjunto** "buscar exactamente en", el controlador MCIAVI busca exactamente en el marco que la aplicación especifica. Esto puede provocar un retraso si el archivo está comprimido temporalmente y la aplicación no especifica un fotograma clave. Cuando se usa **el conjunto** "buscar exactamente desactivado", el controlador MCIAVI busca al fotograma clave más cercano en un archivo comprimido temporalmente.

Algunos comandos de MCI permiten a la aplicación modificar la reproducción de un archivo AVI de otras maneras. Por ejemplo, un archivo AVI, de forma predeterminada, se reproduce a su velocidad normal, pero la aplicación puede aumentar o disminuir esta velocidad mediante la marca "speed" con el **comando set.** Para los archivos AVI, un valor de velocidad de 1000 es típico. Por lo tanto, para reproducir una película a la mitad de su velocidad típica, la aplicación puede usar el comando **set** "movie speed 500". Como alternativa, puede usar **establecer** "velocidad de película 2000" para reproducir la secuencia a dos veces su velocidad normal.

El [**comando setaudio**](setaudio.md) ([**MCI \_ SETAUDIO**](mci-setaudio.md)) permite que la aplicación controle la parte de audio de un archivo AVI. La aplicación puede silenciar el audio durante la reproducción o, en el caso de varios archivos de secuencia de audio, seleccionar la secuencia de audio que se reproduce.

El controlador MCIAVI tiene un cuadro de diálogo para controlar algunas de sus opciones de reproducción. Algunas de las opciones disponibles para el usuario incluyen seleccionar la reproducción de pantalla completa o orientada a ventanas, seleccionar el modo de búsqueda y acercar la imagen. La aplicación puede hacer que MCIAVI muestre este cuadro de diálogo mediante el [**comando configure**](configure.md) [**(MCI \_ CONFIGURE).**](mci-configure.md)

## <a name="stream-handlers"></a>Controladores de flujo

Los datos de un archivo AVI se tratan como una serie de secuencias. Normalmente, un archivo AVI contiene una secuencia de audio y vídeo, y también puede haber una secuencia personalizada que contenga texto o algunos otros datos personalizados. El controlador MCIAVI puede usar controladores diferentes para estos flujos de datos. Para obtener más información sobre los archivos AVI personalizados, vea [Custom File and Stream Handlers](custom-file-and-stream-handlers.md).

 

 