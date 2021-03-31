---
title: Apertura de un dispositivo
description: Apertura de un dispositivo
ms.assetid: d4881d32-e8b7-45e6-b00b-b4cd69b738f1
keywords:
- Comando MCI_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd975b0dd5004fb4b1209003568b7fd5901cfc4e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077601"
---
# <a name="opening-a-device"></a>Apertura de un dispositivo

Antes de usar un dispositivo, debe inicializarlo con el comando [**abrir**](open.md) ([**MCI \_ abierto**](mci-open.md)). Este comando carga el controlador en la memoria (si aún no está cargado) y recupera el identificador de dispositivo que se usará para identificar el dispositivo en los comandos MCI posteriores. Debe comprobar el valor devuelto de la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) o [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) antes de usar un nuevo identificador de dispositivo para asegurarse de que el identificador es válido. (También puede recuperar un identificador de dispositivo mediante la función [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) ).

Al igual que todos los mensajes de comandos MCI, **MCI \_ Open** tiene una estructura asociada. Estas estructuras a veces se denominan *bloques de parámetros*. La estructura predeterminada de **MCI \_ Open** es [**MCI \_ Open \_ parms**](mci-open-parms.md). Algunos dispositivos (como la forma de *onda* y la *superposición*) tienen estructuras extendidas (como [**MCI \_ Wave \_ Open \_ parms**](mci-wave-open-parms.md) y [**MCI \_ OVLY \_ Open \_ parms**](mci-ovly-open-parms.md)) para dar cabida a parámetros opcionales adicionales. A menos que necesite usar estos parámetros adicionales, puede usar la estructura **MCI \_ Open \_ parms** con cualquier dispositivo MCI.

El número de dispositivos que puede tener abiertos solo está limitado por la cantidad de memoria disponible.

## <a name="using-an-alias"></a>Usar un alias

Al abrir un dispositivo, puede usar la marca "alias" para especificar un identificador de dispositivo para el dispositivo. Esta marca permite asignar un identificador de dispositivo corto para dispositivos compuestos con nombres de archivo largos y permite abrir varias instancias del mismo archivo o dispositivo.

Por ejemplo, el siguiente comando asigna el identificador de dispositivo "birdcall" al nombre de archivo largo C: \\ NABIRDS \\ Sounds \\ MOCKMTNG. WAV


```C++
mciSendString(
    "open c:\nabirds\sounds\mockmtng.wav type waveaudio alias birdcall", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



En la interfaz de mensajes de comandos, especifique un alias mediante el miembro **lpstrAlias** de la estructura [**de \_ \_ parms abierto de MCI**](mci-open-parms.md) .

## <a name="specifying-a-device-type"></a>Especificación de un tipo de dispositivo

Al abrir un dispositivo, puede usar la marca "tipo" para hacer referencia a un tipo de dispositivo, en lugar de a un controlador de dispositivo específico. En el siguiente ejemplo se abre el archivo de audio de forma de onda C: sonidos de \\ Windows \\ . WAV (mediante la marca "tipo" para especificar el tipo de dispositivo **WaveAudio** ) y asigna el alias "campanas":


```C++
mciSendString(
    "open c:\windows\chimes.wav type waveaudio alias chimes", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



En la interfaz de mensajes de comandos, el miembro **lpstrDeviceType** de la estructura de [**\_ \_ parms abierto de MCI**](mci-open-parms.md) proporciona la funcionalidad de la marca "tipo".

## <a name="simple-and-compound-devices"></a>Dispositivos simples y compuestos

MCI clasifica los controladores de dispositivos como *compuestos* o *simples*. Los controladores de dispositivos compuestos requieren el nombre de un archivo de datos para la reproducción. los controladores para dispositivos sencillos no lo hacen.

Los dispositivos simples incluyen dispositivos **cdaudio** y **VideoDisc** . Hay dos maneras de abrir dispositivos simples:

-   Especifique un puntero a una cadena terminada en null que contenga el nombre del dispositivo del registro o del archivo de SYSTEM.INI.

    Por ejemplo, puede abrir un dispositivo de **videodisco** con el siguiente comando:


```C++
    mciSendString("open videodisc", lpszReturnString, 
        lstrlen(lpszReturnString), NULL);
```



En este caso, "VideoDisc" es el nombre del dispositivo en el registro o en la \[ \] sección mci de SYSTEM.INI.

-   Especifique el nombre real del controlador de dispositivo. La apertura de un dispositivo con el nombre de archivo del controlador de dispositivo, sin embargo, hace que la aplicación sea específica del dispositivo y puede impedir que la aplicación se ejecute si cambia la configuración del sistema. Si utiliza un nombre de archivo, no es necesario especificar la ruta de acceso completa o la extensión de nombre de archivo. MCI supone que los controladores se encuentran en un directorio del sistema y tienen el. Extensión de nombre de archivo DRV.

Los dispositivos compuestos incluyen **WaveAudio** y los dispositivos **Sequencer** . Los datos de un dispositivo compuesto se denominan a veces *elemento de dispositivo*. Sin embargo, este documento normalmente hace referencia a estos datos como un archivo, aunque en algunos casos es posible que los datos no se almacenen como un archivo.

Hay tres maneras de abrir un dispositivo compuesto:

-   Especifique solo el nombre del dispositivo. Esto le permite abrir un dispositivo compuesto sin asociar un nombre de archivo. La mayoría de los dispositivos compuestos solo procesan los comandos [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) y [**Close**](close.md) ([**MCI \_ Close**](mci-close.md)) cuando se abren de esta manera.
-   Especifique solo el nombre de archivo. El nombre del dispositivo se determina a partir de las asociaciones del registro.
-   Especifique el nombre de archivo y el nombre del dispositivo. MCI omite las entradas en el registro y abre el nombre del dispositivo especificado.

Para asociar un archivo de datos a un dispositivo determinado, puede especificar el nombre de archivo y el nombre del dispositivo. Por ejemplo, el siguiente comando abre el dispositivo **WaveAudio** con el nombre de archivo de la voz. SND


```C++
mciSendString("open myvoice.snd type waveaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



En la interfaz de cadena de comandos, también puede abreviar la especificación de nombre de dispositivo mediante el formato de signo de exclamación alternativo, como se documenta con el comando [**abrir**](open.md) .

## <a name="opening-a-device-using-the-filename-extension"></a>Abrir un dispositivo con la extensión de nombre de archivo

Si el comando [**abrir**](open.md) ([**MCI \_ abierto**](mci-open.md)) especifica solo el nombre de archivo, MCI usa la extensión de nombre de archivo para seleccionar el dispositivo adecuado en la lista del registro o en la \[ \] sección de extensiones MCI del archivo de SYSTEM.INI. Las entradas de la \[ sección de extensiones MCI \] usan el formato siguiente:

*\_*  =  *\_ nombre del dispositivo* de extensión de nombre de archivo

MCI usa implícitamente *el \_ nombre del dispositivo* si se encuentra la extensión y si no se ha especificado un nombre de dispositivo en el comando **abrir** .

En el ejemplo siguiente se muestra una \[ sección de extensiones MCI típica \] :


```C++
[mci extensions]
wav=waveaudio
mid=sequencer
rmi=sequencer
```



Con estas definiciones, MCI abre el dispositivo **WaveAudio** si se emite el siguiente comando:


```C++
mciSendString("open train.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="new-data-files"></a>Nuevos archivos de datos

Para crear un nuevo archivo de datos, solo tiene que especificar un nombre de archivo en blanco. MCI no guarda un archivo nuevo hasta que lo guarde con el comando [**Guardar**](save.md) ([**MCI \_ Save**](mci-save.md)). Al crear un nuevo archivo, debe incluir un alias de dispositivo con el comando [**abrir**](open.md) ([**MCI \_ abierto**](mci-open.md)).

En el ejemplo siguiente se abre un nuevo archivo **WaveAudio** , se inicia y se detiene la grabación y, a continuación, se guarda y se cierra el archivo:


```C++
mciSendString("open new type waveaudio alias capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("record capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("stop capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("save capture orca.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="sharable-devices"></a>Dispositivos que se van a compartir

La marca "compartible" (MCI \_ Open \_ Shareable) del comando [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)) permite que varias aplicaciones tengan acceso simultáneamente al mismo dispositivo (o archivo) e instancia de dispositivo. Si la aplicación abre un dispositivo o un archivo como compartido, otras aplicaciones también pueden tener acceso al mismo abriéndolo como compartible. El dispositivo o archivo compartido proporciona a cada aplicación la capacidad de cambiar los parámetros que rigen su estado operativo. Cada vez que un dispositivo o un archivo se abre como compartido, MCI devuelve un identificador de dispositivo único, aunque los identificadores hagan referencia a la misma instancia.

Si la aplicación abre un dispositivo o un archivo sin especificar que se pueda compartir, ninguna otra aplicación podrá tener acceso a él hasta que la aplicación lo cierre. Además, si un dispositivo solo admite una instancia abierta, el comando **Open** producirá un error si se especifica la marca compartible.

Si la aplicación abre un dispositivo y especifica que se pueda compartir, la aplicación no debe hacer ninguna suposición sobre el estado de este dispositivo. Es posible que la aplicación necesite compensar los cambios realizados por otras aplicaciones que acceden al dispositivo.

La mayoría de los archivos compuestos no se pueden compartir. sin embargo, puede abrir varios archivos, o puede abrir un solo archivo varias veces. Si abre un solo archivo varias veces, MCI crea una instancia independiente para cada una de ellas con un estado operativo único.

Si abre varias instancias de un archivo, debe asignar un identificador de dispositivo único a cada uno de ellos. Puede usar un alias, como se describe en la sección siguiente, para asignar un nombre único a cada archivo.

 

 