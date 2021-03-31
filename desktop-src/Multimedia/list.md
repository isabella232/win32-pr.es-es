---
title: List (comando)
description: El comando list determina el número y los tipos de entradas de vídeo y audio. Los dispositivos digitales-vídeo y VCR reconocen este comando.
ms.assetid: b3fe3819-0b8a-4de5-9c79-03e1e089436f
keywords:
- Mostrar comandos de Windows multimedia
topic_type:
- apiref
api_name:
- list
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d0a171c6768caf1b947a0d07cb46e5cccd28c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151130"
---
# <a name="list-command"></a>List (comando)

El comando list determina el número y los tipos de entradas de vídeo y audio. Los dispositivos digitales-vídeo y VCR reconocen este comando.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("list %s %s %s"), 
  lpszDeviceID, 
  lpszList, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de un dispositivo MCI. Este identificador o alias se asigna cuando se abre el dispositivo.

</dd> <dt>

<span id="lpszList"></span><span id="lpszlist"></span><span id="LPSZLIST"></span>*lpszList*
</dt> <dd>

Marca que identifica el número y los tipos de entradas de vídeo y audio. En la tabla siguiente se enumeran los tipos de dispositivos que reconocen el comando **List** y las marcas usadas por cada tipo.



| Value        | Significado                                                                           | Significado                                                                                                                      |
|--------------|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| digitalvideo | audio algorithmaudio de *algoritmo* de algoritmo de calidad de audio streamcountnumber *Índice* de audio | algoritmo de algoritmo de calidad de algorithmstill *de vídeo flujo* de calidad de algorithmvideo *de vídeo* |
| vídeos          | origen de audio countaudio *Índice* de número de origen                                     | origen de vídeo countvideo *Índice* de número de origen                                                                                |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el parámetro **lpszList** y su significado.



| Value                               | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algoritmo de audio                     | Especifica que el comando debe recuperar los nombres de los algoritmos de audio.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *algoritmo* de algoritmo de calidad de audio | Especifica que el comando debe recuperar los niveles de calidad asociados con el *algoritmo* especificado. Si *algorithm* es "Current", se devuelve el nivel de calidad del algoritmo actual.                                                                                                                                                                                                                                                                                                   |
| recuento de origen de audio                  | Devuelve el número total de entradas de audio.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| *Índice* de número de origen de audio         | Devuelve el tipo de entrada de audio del *Índice* de origen.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| secuencia de audio                        | Especifica que el comando debe recuperar los nombres de las secuencias de audio asociadas al área de trabajo. Estas cadenas (como "inglés" o "alemán") se insertan en el archivo e identifican la secuencia.                                                                                                                                                                                                                                                                                    |
| count                               | Devuelve el número de opciones del tipo especificado.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| *Índice* de número                      | Devuelve una cadena que describe una opción específica (como se identifica por *Índice*) del tipo de opción especificado. *Index* debe ser un entero comprendido entre 1 y el valor devuelto por "Count".                                                                                                                                                                                                                                                                                                         |
| algoritmo de todavía                     | Especifica que el comando debe recuperar los nombres de los algoritmos.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *algoritmo* de algoritmo de calidad todavía | Especifica que el comando debe recuperar los niveles de calidad asociados al *algoritmo* todavía especificado. Si *algorithm* es "Current", se devuelve el nivel de calidad del algoritmo actual.                                                                                                                                                                                                                                                                                             |
| algoritmo de vídeo                     | Especifica que el comando debe recuperar los nombres de los algoritmos de vídeo.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *algoritmo* de algoritmo de calidad de vídeo | Especifica que el comando debe recuperar los niveles de calidad asociados al *algoritmo* de vídeo especificado. Si *algorithm* es "Current", se devuelve el nivel de calidad del algoritmo actual.                                                                                                                                                                                                                                                                                             |
| origen de vídeo                        | Especifica que el comando debe devolver información sobre los orígenes de vídeo. Cuando se usa con la marca "Count", devuelve el número de orígenes de vídeo. Cuando se usa con la marca "número", devuelve el tipo de un origen de vídeo. MCI define las constantes siguientes para el tipo: "NTSC", "RGB", "PAL", "SECAM", "Svideo" y "Generic". Puede haber más de un origen de cada tipo devuelto. El tipo de origen "genérico" se usa cuando se permite más de una señal para dicho conector. |
| recuento de orígenes de vídeo                  | Devuelve el número total de entradas de vídeo.                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *Índice* de número de origen de vídeo         | Devuelve el tipo de entrada de vídeo del *Índice* de origen.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| secuencia de vídeo                        | Especifica que el comando debe recuperar los nombres de las secuencias de vídeo asociadas al área de trabajo. Estas cadenas (como "Finally divertido" o "Sad Terminate") se insertan en el archivo e identifican la secuencia.                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "Wait", "Notify" o "Test". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="remarks"></a>Observaciones

En el caso de los dispositivos VCR, el "origen de vídeo" o el "origen de audio" deben especificarse con las marcas "recuento" o "número". Si se especifica "Count", se devuelve el número total de entradas de vídeo o audio. Si se especifica "Number", el controlador devuelve un tipo correspondiente a la entrada. El tipo puede ser cualquiera de los siguientes: "Tuner", "line", "Svideo", "AUX" o "Generic". Normalmente, primero debe consultar el VCR para el "recuento" y, a continuación, usar el recuento como el intervalo de la marca "número". Los números de "origen" empiezan por 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadenas de comandos MCI](mci-command-strings.md)
</dt> </dl>

 

