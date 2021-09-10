---
title: Comando open (Corecrt \_ io.h)
description: El comando open inicializa un dispositivo. Todos los dispositivos MCI reconocen este comando.
ms.assetid: 0bb97c8c-8222-4d4e-b20b-94e9f9095afe
keywords:
- comando open Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369840"
---
# <a name="open-command"></a>Comando open

El comando open inicializa un dispositivo. Todos los dispositivos MCI reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

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

Identificador de un dispositivo MCI o controlador de dispositivo. Puede ser un nombre de dispositivo (como se especifica en el registro o el archivo SYSTEM.INI) o el nombre de archivo del controlador del dispositivo. Si especifica el nombre de archivo del controlador de dispositivo, opcionalmente puede incluir . Extensión DRV, pero no debe incluir la ruta de acceso al archivo.

</dd> <dt>

<span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszOpenFlags*
</dt> <dd>

Marca que identifica lo que se va a inicializar. En la tabla siguiente se enumeran los tipos de dispositivo que reconocen el comando **open** y las marcas usadas por cada tipo.



| Value        | Significado                                                        | Significado                                                                         |
|--------------|----------------------------------------------------------------|---------------------------------------------------------------------------------|
| cdaudio      | alias *de dispositivo \_ compartible*                                  | tipo *\_ de dispositivo*                                                             |
| digitalvideo | alias *de dispositivo \_ aliaselementname* nostatic parent *hwnd* compartible | estilo de estilo secundario superpuesto estilo emergente tipo *de \_ estilo tipo* de *dispositivo \_* |
| overlay      | alias *device \_ alias* parent *hwnd* shareable style child         | style overlapped style popup style *style \_ type type* device type (tipo de dispositivo de tipo de dispositivo de estilo emergente de estilo *\_ superpuesto de estilo superpuesto)*             |
| sequencer    | alias *de dispositivo \_ compartible*                                 | tipo *\_ de dispositivo*                                                             |
| Vcr          | alias *de dispositivo \_ compartible*                                  | tipo *\_ de dispositivo*                                                             |
| videodisk    | alias *de dispositivo \_ compartible*                                  | tipo *\_ de dispositivo*                                                             |
| waveaudio    | alias *device \_ alias* buffer *buffer \_ size*                     | tipo de dispositivo de tipo *\_ compartible*                                                    |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el **parámetro lpszOpenFlags** y sus significados.



| Value                 | Significado                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| alias *\_ de dispositivo* | Especifica un nombre alternativo para el dispositivo especificado. Si se especifica, debe usarse como identificador *de \_ dispositivo* en los comandos posteriores.                                                                                                                                                                                                                                          |
| *Elementname*         | Especifica el nombre del elemento de dispositivo (archivo) cargado cuando se abre el dispositivo.                                                                                                                                                                                                                                                                                        |
| tamaño *del búfer de \_ búfer* | Establece el tamaño, en segundos, del búfer utilizado por el dispositivo de audio de forma de onda. El tamaño predeterminado del búfer se establece cuando el dispositivo de audio de forma de onda está instalado o configurado. Normalmente, el tamaño del búfer se establece en 4 segundos. Con el dispositivo MCIWAVE, el tamaño mínimo es de 2 segundos y el tamaño máximo es de 9 segundos.                                                |
| hwnd *primario*         | Especifica el identificador de ventana de la ventana primaria.                                                                                                                                                                                                                                                                                                                    |
| compartible              | Inicializa el dispositivo o el archivo como compartible. Los intentos posteriores para abrir el dispositivo o el archivo producirán un error a menos que especifique "compartible" en los comandos abiertos originales **y** posteriores. MCI devuelve un error de dispositivo no válido si el dispositivo ya está abierto y no se puede compartir.<br/> El secuenciador MCISEQ y los dispositivos MCIWAVE no admiten archivos compartidos.<br/> |
| elemento secundario de estilo           | Abre una ventana con un estilo de ventana secundario.                                                                                                                                                                                                                                                                                                                            |
| estilo superpuesto      | Abre una ventana con un estilo de ventana superpuesto.                                                                                                                                                                                                                                                                                                                      |
| elemento emergente de estilo           | Abre una ventana con un estilo de ventana emergente.                                                                                                                                                                                                                                                                                                                           |
| tipo *de estilo de \_ estilo*   | Indica un estilo de ventana.                                                                                                                                                                                                                                                                                                                                            |
| tipo *\_ de dispositivo*   | Especifica el tipo de dispositivo de un archivo.                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o ambos. Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

MCI reserva "cdaudio" para el tipo de dispositivo de audio de CD, "videodisc" para el tipo de dispositivo videodisc, "sequencer" para el tipo de dispositivo secuenciador MIDI, "AVIVideo" para el tipo de dispositivo de vídeo digital y "waveaudio" para el tipo de dispositivo audio de onda.

Como alternativa a la marca "type", MCI puede seleccionar el dispositivo en función de la extensión usada por el archivo, tal como se registra en el registro o en la sección de extensión mci del archivo \[ \] SYSTEM.INI.

MCI puede abrir archivos AVI mediante un puntero de interfaz de archivo o un puntero de interfaz de secuencia. Para abrir un archivo mediante cualquiera de los tipos de puntero de interfaz, especifique un elemento at sign (@) seguido del puntero de interfaz en lugar del nombre del archivo o del dispositivo para el *parámetro lpszDevice.* Para obtener más información sobre las interfaces de archivos y secuencias, vea ["Funciones y macros AVIFile".](avifile-functions-and-macros.md)

El comando siguiente abre el dispositivo "mysound".

``` syntax
open new type waveaudio alias mysound buffer 6
```

Con el nombre de dispositivo "nuevo", el controlador de forma de onda prepara un nuevo recurso de forma de onda. El comando asigna el alias de dispositivo "mysound" y especifica un búfer de 6 segundos.

Puede eliminar la marca "type" si combina el nombre del dispositivo con el nombre de archivo. MCI reconoce esta combinación cuando se usa la sintaxis siguiente:

*device \_ name* ! *nombre del \_ elemento*

El signo de exclamación separa el nombre del dispositivo del nombre de archivo. El signo de exclamación no debe delimitarse por espacios en blanco.

En el ejemplo siguiente se abre right. Archivo WAV mediante el dispositivo "waveaudio".

``` syntax
open waveaudio!right.wav
```

El controlador MCIWAVE requiere un dispositivo asincrónico de audio de forma de onda.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Corecrt \_ io.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadenas de comandos de MCI](mci-command-strings.md)
</dt> </dl>

 

