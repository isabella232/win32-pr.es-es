---
title: Comando list
description: El comando list determina el número y los tipos de entradas de audio y vídeo. Los dispositivos de vídeo digital y VCR reconocen este comando.
ms.assetid: b3fe3819-0b8a-4de5-9c79-03e1e089436f
keywords:
- comando list Windows Multimedia
topic_type:
- apiref
api_name:
- list
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d0a171c6768caf1b947a0d07cb46e5cccd28c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473896"
---
# <a name="list-command"></a>Comando list

El comando list determina el número y los tipos de entradas de audio y vídeo. Los dispositivos de vídeo digital y VCR reconocen este comando.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

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

Marca que identifica el número y los tipos de entradas de audio y vídeo. En la tabla siguiente se enumeran los tipos de dispositivo que reconocen el comando **list** y las marcas usadas por cada tipo.



| Value        | Significado                                                                           | Significado                                                                                                                      |
|--------------|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| digitalvideo | audio algorithmaudio quality algorithm *audio* streamcountnumber *index* | still algorithmstil algorithm video algorithm *video* algorithmvideo quality *algorithm video* sourcevideo stream |
| Vcr          | audio source countaudio source number *index*                                     | recuento de orígenes de vídeo Índice de número de origen de *vídeo*                                                                                |



 

En la tabla siguiente se enumeran las marcas que se pueden especificar en el **parámetro lpszList** y sus significados.



| Value                               | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algoritmo de audio                     | Especifica que el comando debe recuperar nombres de algoritmos de audio.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| algoritmo de calidad de *audio* | Especifica que el comando debe recuperar los niveles de calidad asociados al algoritmo *especificado.* Si *el* algoritmo es "actual", se devuelve el nivel de calidad del algoritmo actual.                                                                                                                                                                                                                                                                                                   |
| recuento de orígenes de audio                  | Devuelve el número total de entradas de audio.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| índice de número de origen *de audio*         | Devuelve el tipo de entrada de audio del índice de *origen.*                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| secuencia de audio                        | Especifica que el comando debe recuperar los nombres de las secuencias de audio asociadas al área de trabajo. Estas cadenas (como "Inglés" o "Alemán") se incrustan en el archivo e identifican la secuencia.                                                                                                                                                                                                                                                                                    |
| count                               | Devuelve el número de opciones del tipo especificado.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| number *index*                      | Devuelve una cadena que describe una opción específica (identificada por *el índice)* del tipo de opción especificado. *Index* debe ser un entero entre 1 y el valor devuelto por "count".                                                                                                                                                                                                                                                                                                         |
| algoritmo still                     | Especifica que el comando debe recuperar nombres de algoritmos todavía.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| algoritmo de calidad *todavía* | Especifica que el comando debe recuperar los niveles de calidad asociados al algoritmo still *especificado.* Si *el* algoritmo es "actual", se devuelve el nivel de calidad del algoritmo actual.                                                                                                                                                                                                                                                                                             |
| algoritmo de vídeo                     | Especifica que el comando debe recuperar nombres de algoritmos de vídeo.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| algoritmo de calidad de *vídeo* | Especifica que el comando debe recuperar los niveles de calidad asociados al algoritmo de *vídeo especificado.* Si *el* algoritmo es "actual", se devuelve el nivel de calidad del algoritmo actual.                                                                                                                                                                                                                                                                                             |
| origen de vídeo                        | Especifica que el comando debe devolver información sobre los orígenes de vídeo. Cuando se usa con la marca "count", devuelve el número de orígenes de vídeo. Cuando se usa con la marca "number", devuelve el tipo de un origen de vídeo. MCI define las siguientes constantes para el tipo: "cide", "rgb", "pal", "secam", "svideo" y "generic". Puede haber más de un origen de cada tipo devuelto. El tipo de origen "genérico" se usa cuando se permite más de una señal para ese conector. |
| recuento de orígenes de vídeo                  | Devuelve el número total de entradas de vídeo.                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| índice de número de origen de *vídeo*         | Devuelve el tipo de entrada de vídeo del índice de *origen.*                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| secuencia de vídeo                        | Especifica que el comando debe recuperar los nombres de las secuencias de vídeo asociadas al área de trabajo. Estas cadenas (por ejemplo, "final desastados" o "final desastados") se incrustan en el archivo e identifican la secuencia.                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Puede ser "wait", "notify" o "test". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o se produce un error en caso contrario.

## <a name="remarks"></a>Observaciones

En el caso de los dispositivos VCR, se debe especificar "origen de vídeo" o "origen de audio" con las marcas "count" o "number". Si se especifica "count", se devuelve el número total de entradas de vídeo o audio. Si se especifica "number", el controlador devuelve un tipo correspondiente a la entrada. El tipo puede ser cualquiera de los siguientes: "tuner", "line", "svideo", "aux" o "generic". Normalmente, primero debe consultar el vcr para el "recuento" y, a continuación, usar el recuento como intervalo para la marca "number". Los números de "origen" comienzan a partir de 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadenas de comandos de MCI](mci-command-strings.md)
</dt> </dl>

 

