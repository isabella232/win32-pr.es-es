---
title: Abrir un dispositivo
description: Abrir un dispositivo
ms.assetid: d4881d32-e8b7-45e6-b00b-b4cd69b738f1
keywords:
- MCI_OPEN comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd975b0dd5004fb4b1209003568b7fd5901cfc4e
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371653"
---
# <a name="opening-a-device"></a>Abrir un dispositivo

Antes de usar un dispositivo, debe inicializar mediante el [**comando open**](open.md) [**(MCI \_ OPEN).**](mci-open.md) Este comando carga el controlador en memoria (si aún no está cargado) y recupera el identificador de dispositivo que usará para identificar el dispositivo en los comandos MCI posteriores. Debe comprobar el valor devuelto de la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) o [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) antes de usar un nuevo identificador de dispositivo para asegurarse de que el identificador es válido. (También puede recuperar un identificador de dispositivo mediante la [**función mciGetDeviceID).**](/previous-versions//dd757156(v=vs.85))

Al igual que todos los mensajes de comandos de **MCI, MCI \_ OPEN** tiene una estructura asociada. A veces, estas estructuras se denominan *bloques de parámetros*. La estructura predeterminada de **MCI \_ OPEN** es [**MCI \_ OPEN \_ PARMS.**](mci-open-parms.md) Algunos dispositivos  (como la forma de onda y la superposición) tienen estructuras extendidas (como [**MCI WAVE OPEN \_ \_ \_ PARMS**](mci-wave-open-parms.md) y [**MCI \_ OVLY OPEN \_ \_ PARMS)**](mci-ovly-open-parms.md)para dar cabida a parámetros opcionales adicionales. A menos que necesite usar estos parámetros adicionales, puede usar la estructura **MCI \_ OPEN \_ PARMS** con cualquier dispositivo MCI.

El número de dispositivos que puede tener abiertos solo está limitado por la cantidad de memoria disponible.

## <a name="using-an-alias"></a>Uso de un alias

Al abrir un dispositivo, puede usar la marca "alias" para especificar un identificador de dispositivo para el dispositivo. Esta marca le permite asignar un identificador de dispositivo corto para dispositivos compuestos con nombres de archivo largos y le permite abrir varias instancias del mismo archivo o dispositivo.

Por ejemplo, el comando siguiente asigna el identificador de dispositivo "birdcall" al nombre de archivo largo C: \\ NABIRDS \\ SOUNDS \\ MOCKMTNG. WAV:


```C++
mciSendString(
    "open c:\nabirds\sounds\mockmtng.wav type waveaudio alias birdcall", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



En la interfaz de mensaje de comando, especifique un alias mediante el **miembro lpstrAlias** de la estructura [**MCI \_ OPEN \_ PARMS.**](mci-open-parms.md)

## <a name="specifying-a-device-type"></a>Especificar un tipo de dispositivo

Al abrir un dispositivo, puede usar la marca "type" para hacer referencia a un tipo de dispositivo, en lugar de a un controlador de dispositivo específico. En el ejemplo siguiente se abre el archivo de audio de forma de onda C: \\ WINDOWS \\ CHIMES. WAV (con la marca "type" para especificar el tipo de dispositivo **waveaudio)** y asigna el alias "chimes":


```C++
mciSendString(
    "open c:\windows\chimes.wav type waveaudio alias chimes", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



En la interfaz de mensaje de comando, el miembro **lpstrDeviceType** de la estructura [**MCI \_ OPEN \_ PARMS**](mci-open-parms.md) proporciona la funcionalidad de la marca "type".

## <a name="simple-and-compound-devices"></a>Dispositivos simples y compuestos

MCI clasifica los controladores de dispositivo como *compuestos* o *simples.* Los controladores para dispositivos compuestos requieren el nombre de un archivo de datos para la reproducción; Los controladores para dispositivos simples no lo hacen.

Los dispositivos simples **incluyen dispositivos cdaudio** **y videodisc.** Hay dos maneras de abrir dispositivos simples:

-   Especifique un puntero a una cadena terminada en NULL que contenga el nombre del dispositivo del Registro o del SYSTEM.INI archivo.

    Por ejemplo, puede abrir un **dispositivo videodisc** mediante el comando siguiente:


```C++
    mciSendString("open videodisc", lpszReturnString, 
        lstrlen(lpszReturnString), NULL);
```



En este caso, "videodisc" es el nombre del dispositivo del registro o la \[ sección mci \] de SYSTEM.INI.

-   Especifique el nombre real del controlador del dispositivo. Sin embargo, abrir un dispositivo con el nombre de archivo device-driver hace que el dispositivo de la aplicación sea específico y puede impedir que la aplicación se ejecute si cambia la configuración del sistema. Si usa un nombre de archivo, no es necesario especificar la ruta de acceso completa o la extensión de nombre de archivo; MCI supone que los controladores se encuentran en un directorio del sistema y tienen . Extensión de nombre de archivo DRV.

Los dispositivos compuestos **incluyen dispositivos waveaudio** **y sequencer.** Los datos de un dispositivo compuesto a veces se denominan *elemento de dispositivo*. Sin embargo, este documento suele hacer referencia a estos datos como un archivo, aunque en algunos casos es posible que los datos no se almacenen como un archivo.

Hay tres maneras de abrir un dispositivo compuesto:

-   Especifique solo el nombre del dispositivo. Esto le permite abrir un dispositivo compuesto sin asociar un nombre de archivo. La mayoría de [](capability.md) los dispositivos compuestos solo procesan la funcionalidad [**(MCI \_ GETDEVCAPS)**](mci-getdevcaps.md)y [**cierran**](close.md) los comandos [**(MCI \_ CLOSE)**](mci-close.md)cuando se abren de esta manera.
-   Especifique solo el nombre de archivo. El nombre del dispositivo se determina a partir de las asociaciones del Registro.
-   Especifique el nombre de archivo y el nombre del dispositivo. MCI omite las entradas del Registro y abre el nombre de dispositivo especificado.

Para asociar un archivo de datos a un dispositivo determinado, puede especificar el nombre de archivo y el nombre del dispositivo. Por ejemplo, el comando siguiente abre el **dispositivo waveaudio** con el nombre de archivo MYVOICE. SND:


```C++
mciSendString("open myvoice.snd type waveaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



En la interfaz de cadena de comandos, también puede abreviar la especificación del nombre del dispositivo mediante el formato de signo de exclamación alternativo, como se documenta con el [**comando open.**](open.md)

## <a name="opening-a-device-using-the-filename-extension"></a>Abrir un dispositivo mediante la extensión filename

Si el [**comando open**](open.md) [**(MCI \_ OPEN)**](mci-open.md)especifica solo el nombre de archivo, MCI usa la extensión filename para seleccionar el dispositivo adecuado en la lista del Registro o en la sección de extensiones mci del archivo \[ \] SYSTEM.INI. Las entradas de la sección \[ mci extensions \] usan el formato siguiente:

*nombre de \_ dispositivo de extensión* de nombre de  =  *\_ archivo*

MCI usa implícitamente *el nombre \_ del* dispositivo si se encuentra la extensión y si no se ha especificado un nombre de dispositivo en el **comando open.**

En el ejemplo siguiente se muestra una sección \[ típica de extensiones \] mci:


```C++
[mci extensions]
wav=waveaudio
mid=sequencer
rmi=sequencer
```



Con estas definiciones, MCI abre el **dispositivo waveaudio** si se emite el siguiente comando:


```C++
mciSendString("open train.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="new-data-files"></a>Nuevos archivos de datos

Para crear un nuevo archivo de datos, basta con especificar un nombre de archivo en blanco. MCI no guarda un nuevo archivo hasta que lo guarde mediante el comando [**save**](save.md) [**(MCI \_ SAVE).**](mci-save.md) Al crear un archivo, debe incluir un alias de dispositivo con el [**comando open**](open.md) [**(MCI \_ OPEN).**](mci-open.md)

En el ejemplo siguiente se abre un nuevo **archivo waveaudio,** se inicia y se detiene la grabación y, a continuación, se guarda y se cierra el archivo:


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



## <a name="sharable-devices"></a>Dispositivos compartibles

La marca "compartible" (MCI OPEN SHAREABLE) del comando \_ \_ [**open**](open.md) [**(MCI \_ OPEN)**](mci-open.md)permite que varias aplicaciones accedan al mismo dispositivo (o archivo) e instancia de dispositivo simultáneamente. Si la aplicación abre un dispositivo o archivo como compartible, otras aplicaciones también pueden acceder a él si lo abren como compartible. El archivo o dispositivo compartido ofrece a cada aplicación la capacidad de cambiar los parámetros que rigen su estado operativo. Cada vez que se abre un dispositivo o archivo como compartible, MCI devuelve un identificador de dispositivo único, aunque los identificadores hacen referencia a la misma instancia.

Si la aplicación abre un dispositivo o archivo sin especificar que es compartible, ninguna otra aplicación puede acceder a él hasta que la aplicación lo cierre. Además, si un dispositivo solo admite una instancia abierta, se producirá un error en el comando **open** si especifica la marca que se puede compartir.

Si la aplicación abre un dispositivo y especifica que se puede compartir, la aplicación no debe realizar ninguna suposición sobre el estado de este dispositivo. Es posible que la aplicación tenga que compensar los cambios realizados por otras aplicaciones que acceden al dispositivo.

La mayoría de los archivos compuestos no se pueden compartir; sin embargo, puede abrir varios archivos o puede abrir un único archivo varias veces. Si abre un único archivo varias veces, MCI crea una instancia independiente para cada una, con cada instancia con un estado operativo único.

Si abre varias instancias de un archivo, debe asignar un identificador de dispositivo único a cada una. Puede usar un alias, como se describe en la sección siguiente, para asignar un nombre único para cada archivo.

 

 