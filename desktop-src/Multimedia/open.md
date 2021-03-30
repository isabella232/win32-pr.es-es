---
title: comando Open (Corecrt \_ IO. h)
description: El comando Open Inicializa un dispositivo. Todos los dispositivos MCI reconocen este comando.
ms.assetid: 0bb97c8c-8222-4d4e-b20b-94e9f9095afe
keywords:
- abrir comando de Windows multimedia
topic_type:
- apiref
api_name:
- open
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8d31f1806a9c12f764c679548564aa053c3041
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802222"
---
# <a name="open-command"></a>abrir (comando)

El comando Open Inicializa un dispositivo. Todos los dispositivos MCI reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("open %s %s %s"), 
  lpszDevice, 
  lpszOpenFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDevice"></span><span id="lpszdevice"></span><span id="LPSZDEVICE"></span>*lpszDevice*
</dt> <dd>

Identificador de un dispositivo MCI o controlador de dispositivo. Puede ser un nombre de dispositivo (como se indica en el registro o en el archivo SYSTEM.INI) o el nombre de archivo del controlador de dispositivo. Si especifica el nombre de archivo del controlador de dispositivo, puede incluir opcionalmente el. Extensión DRV, pero no debe incluir la ruta de acceso al archivo.

</dd> <dt>

<span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszOpenFlags*
</dt> <dd>

Marca que identifica lo que se va a inicializar. En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **Open** y las marcas usadas por cada tipo.



| Value        | Significado                                                        | Significado                                                                         |
|--------------|----------------------------------------------------------------|---------------------------------------------------------------------------------|
| cdaudio      | alias *de \_ dispositivo* de alias compartible                                  | tipo *de \_ dispositivo*                                                             |
| digitalvideo | alias *Device \_ aliaselementname* nostatic *hWnd* primario compartible | estilo secundario de estilo superpuesto estilo *emergente \_ tipo de estilo tipo* de *\_ dispositivo* |
| overlay      | alias de dispositivo alias primario *hWnd* elemento secundario de estilo compartido *\_*         | estilo de estilo emergente de estilo superpuesto de estilo tipo de tipo de *dispositivo \_* *\_*             |
| sequencer    | alias *de \_ dispositivo* de alias compartible                                 | tipo *de \_ dispositivo*                                                             |
| vídeos          | alias *de \_ dispositivo* de alias compartible                                  | tipo *de \_ dispositivo*                                                             |
| videodisco    | alias *de \_ dispositivo* de alias compartible                                  | tipo *de \_ dispositivo*                                                             |
| waveaudio    | *\_ tamaño de búfer* de búfer de *\_ alias de dispositivo* de alias                     | tipo de *dispositivo \_* compartible                                                    |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszOpenFlags** y su significado.



| Value                 | Significado                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| alias *de \_ dispositivo* alias | Especifica un nombre alternativo para el dispositivo especificado. Si se especifica, se debe usar como el *\_ identificador del dispositivo* en los siguientes comandos.                                                                                                                                                                                                                                          |
| *ElementName*         | Especifica el nombre del elemento de dispositivo (archivo) que se carga cuando se abre el dispositivo.                                                                                                                                                                                                                                                                                        |
| *\_ tamaño de búfer* de búfer | Establece el tamaño, en segundos, del búfer usado por el dispositivo de audio de forma de onda. El tamaño predeterminado del búfer se establece cuando el dispositivo de audio de forma de onda está instalado o configurado. Normalmente, el tamaño del búfer se establece en 4 segundos. Con el dispositivo MCIWAVE, el tamaño mínimo es 2 segundos y el tamaño máximo es de 9 segundos.                                                |
| *hWnd* primario         | Especifica el identificador de ventana de la ventana primaria.                                                                                                                                                                                                                                                                                                                    |
| compartible              | Inicializa el dispositivo o archivo como compartible. Los intentos posteriores para abrir el dispositivo o el archivo producirán un error a menos que especifique "compartible" en los comandos **abiertos** originales y posteriores. MCI devuelve un error de dispositivo no válido si el dispositivo ya está abierto y no se pueda compartir.<br/> Los dispositivos MCISEQ Sequencer y MCIWAVE no admiten archivos compartidos.<br/> |
| estilo secundario           | Abre una ventana con un estilo de ventana secundario.                                                                                                                                                                                                                                                                                                                            |
| estilo superpuesto      | Abre una ventana con un estilo de ventana superpuesto.                                                                                                                                                                                                                                                                                                                      |
| cuadro emergente de estilo           | Abre una ventana con un estilo de ventana emergente.                                                                                                                                                                                                                                                                                                                           |
| *\_ tipo de estilo* de estilo   | Indica un estilo de ventana.                                                                                                                                                                                                                                                                                                                                            |
| tipo *de \_ dispositivo*   | Especifica el tipo de dispositivo de un archivo.                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o ambos. Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

MCI reserva "cdaudio" para el tipo de dispositivo de audio de CD, "VideoDisc" para el tipo de dispositivo de videodisco, "Sequencer" para el tipo de dispositivo del secuenciador de MIDI, "AVIVideo" para el tipo de dispositivo de vídeo digital y "WaveAudio" para el tipo de dispositivo de audio de onda.

Como alternativa a la marca "tipo", MCI puede seleccionar el dispositivo en función de la extensión que usa el archivo, tal como se registra en el registro o en la \[ sección de la extensión MCI \] del archivo de SYSTEM.INI.

MCI puede abrir archivos AVI mediante un puntero de interfaz de archivo o un puntero de interfaz de flujo. Para abrir un archivo mediante cualquier tipo de puntero de interfaz, especifique un signo de arroba (@) seguido del puntero de interfaz en lugar del nombre de archivo o dispositivo para el parámetro *lpszDevice* . Para obtener más información sobre las interfaces de archivo y de secuencia, vea " [funciones y macros de AVIFile](avifile-functions-and-macros.md)".

El siguiente comando abre el dispositivo "de".

``` syntax
open new type waveaudio alias mysound buffer 6
```

Con el nombre de dispositivo "nuevo", el controlador de la onda prepara un nuevo recurso de onda. El comando asigna el alias del dispositivo "mi sonido" y especifica un búfer de 6 segundos.

Puede eliminar la marca "tipo" si combina el nombre del dispositivo con el nombre de archivo. MCI reconoce esta combinación cuando se usa la sintaxis siguiente:

*\_ nombre del dispositivo* *nombre del elemento \_*

El signo de exclamación separa el nombre del dispositivo del nombre de archivo. El signo de exclamación no debe estar delimitado por espacios en blanco.

En el siguiente ejemplo se abre la derecha. Archivo WAV mediante el dispositivo "WaveAudio".

``` syntax
open waveaudio!right.wav
```

El controlador MCIWAVE requiere un dispositivo de audio de onda asincrónica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Corecrt \_ IO. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadenas de comandos MCI](mci-command-strings.md)
</dt> </dl>

 

