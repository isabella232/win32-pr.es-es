---
description: Referencia de archivo de AVI
ms.assetid: 2d8cf5be-1252-4b58-89b1-f5c53ea17d0e
title: Referencia de archivo de AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f28a7254ac9eb927381e313603ffd2bd0d050c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495664"
---
# <a name="avi-riff-file-reference"></a>Referencia de archivo de AVI

El formato de archivo AVI de Microsoft es una especificación de archivo RIFF utilizada con aplicaciones que capturan, editan y reproducen secuencias de audio y vídeo. En general, los archivos AVI contienen varios flujos de tipos de datos diferentes. La mayoría de las secuencias AVI usan secuencias de audio y vídeo. Una variación simple de una secuencia AVI usa datos de vídeo y no requiere una secuencia de audio.

En esta sección no se describen las extensiones de formato de archivo AVI OpenDML. Para obtener más información acerca de estas extensiones, consulte *extensiones de formato de archivo AVI de OpenDML*, publicadas por el Subcomité del formato de archivo AVI de OpenDML AVI.

## <a name="fourccs"></a>FOURCCs

Un FOURCC (código de cuatro caracteres) es un entero sin signo de 32 bits creado mediante la concatenación de cuatro caracteres ASCII. Por ejemplo, el FOURCC ' abcd ' se representa en un sistema Little-Endian como 0x64636261. FOURCCs puede contener caracteres de espacio, por lo que ' ABC ' es un FOURCC válido. El formato de archivo AVI usa códigos FOURCC para identificar tipos de secuencias, fragmentos de datos, entradas de índice y otra información.

## <a name="riff-file-format"></a>Formato de archivo RIFF

El formato de archivo AVI se basa en el formato de documento RIFF (formato de archivo de intercambio de recursos). Un archivo RIFF está formado por un encabezado RIFF seguido de cero o más *listas* y *fragmentos*.

-   El encabezado RIFF tiene el formato siguiente:

    `'RIFF' fileSize fileType (data)`

    donde ' RIFF ' es el código FOURCC literal ' RIFF ', `fileSize` es un valor de 4 bytes que asigna el tamaño de los datos en el archivo y `fileType` es un FourCC que identifica el tipo de archivo específico. El valor de `fileSize` incluye el tamaño del `fileType` FourCC más el tamaño de los datos siguientes, pero no incluye el tamaño del FourCC ' riff ' ni el tamaño de `fileSize` . Los datos de archivo se componen de fragmentos y listas, en cualquier orden.

-   Un fragmento tiene el formato siguiente:

    `ckID ckSize ckData`

    donde `ckID` es un FourCC que identifica los datos contenidos en el fragmento, `ckSize` es un valor de 4 bytes que asigna el tamaño de los datos `ckData` y `ckData` es cero o más bytes de datos. Los datos siempre se rellenan hasta el límite de la **palabra** más cercana. `ckSize` proporciona el tamaño de los datos válidos en el fragmento; no incluye el relleno, el tamaño `ckID` o el tamaño de `ckSize` .

-   Una lista tiene el formato siguiente:

    `'LIST' listSize listType listData`

    donde ' LIST ' es el código FOURCC literal ' LIST ', `listSize` es un valor de 4 bytes que proporciona el tamaño de la lista, `listType` es un código FourCC y `listData` consta de fragmentos o listas, en cualquier orden. El valor de `listSize` incluye el tamaño de `listType` más el tamaño de `listData` ; no incluye el FourCC ' List ' o el tamaño de `listSize` .

En el resto de esta sección se usa la siguiente notación para describir fragmentos RIFF:

`ckID ( ckData )`

donde el tamaño del fragmento es implícito. Con esta notación, una lista se puede representar como:

`'LIST' ( listType ( listData ) )`

Los elementos opcionales se colocan entre corchetes: `[ optional element ]`

## <a name="avi-riff-form"></a>Forma de AVI RIFF

Los archivos AVI se identifican mediante el FOURCC ' AVI ' en el encabezado RIFF. Todos los archivos AVI incluyen dos fragmentos de lista obligatorios, que definen el formato de las secuencias y los datos de la secuencia, respectivamente. Un archivo AVI también puede incluir un fragmento de índice, que proporciona la ubicación de los fragmentos de datos dentro del archivo. Un archivo AVI con estos componentes tiene el formato siguiente:


```C++
RIFF ('AVI '
      LIST ('hdrl' ... )
      LIST ('movi' ... )
      ['idx1' (<AVI Index>) ]
     )
```



La lista ' HDRL ' define el formato de los datos y es el primer fragmento de lista necesario. La lista ' movi ' contiene los datos de la secuencia AVI y es el segundo fragmento de lista necesario. La lista ' idx1 ' contiene el índice. Los archivos AVI deben mantener estos tres componentes en la secuencia adecuada.

> [!Note]  
> Las extensiones OpenDML definen otro tipo de índice, identificado por el FOURCC ' indx '.

 

Las listas "HDRL" y "movi" usan subfragmentos para sus datos. En el ejemplo siguiente se muestra la forma de AVI RIFF expandida con los fragmentos necesarios para completar estas listas:


```C++
RIFF ('AVI '
      LIST ('hdrl'
            'avih'(<Main AVI Header>)
            LIST ('strl'
                  'strh'(<Stream header>)
                  'strf'(<Stream format>)
                  [ 'strd'(<Additional header data>) ]
                  [ 'strn'(<Stream name>) ]
                  ...
                 )
             ...
           )
      LIST ('movi'
            {SubChunk | LIST ('rec '
                              SubChunk1
                              SubChunk2
                              ...
                             )
               ...
            }
            ...
           )
      ['idx1' (<AVI Index>) ]
     )
```



## <a name="avi-main-header"></a>Encabezado principal de AVI

La lista ' HDRL ' comienza con el encabezado AVI principal, que se encuentra en un fragmento ' AVIH '. El encabezado principal contiene información global del archivo AVI completo, como el número de flujos dentro del archivo y el ancho y el alto de la secuencia AVI. El fragmento del encabezado principal se compone de una estructura [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) .

## <a name="avi-stream-headers"></a>Encabezados de secuencia AVI

Una o más listas ' strl ' siguen el encabezado principal. Se requiere una lista ' strl ' para cada flujo de datos. Cada lista ' strl ' contiene información sobre una secuencia en el archivo y debe contener un fragmento de encabezado de secuencia (' strh ') y un fragmento de formato de secuencia (' strf '). Además, una lista ' strl ' podría contener un fragmento de datos de encabezado de flujo (' StrD ') y un fragmento de nombre de flujo (' STRN ').

El fragmento de encabezado de secuencia (' strh ') se compone de una estructura [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) .

Un fragmento de formato de secuencia (' strf ') debe seguir el fragmento de encabezado de flujo. El fragmento de formato de secuencia describe el formato de los datos de la secuencia. Los datos contenidos en este fragmento dependen del tipo de flujo. En el caso de las secuencias de vídeo, la información es una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , incluida la información de la paleta si es necesario. En el caso de las secuencias de audio, la información es una estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .

Si el fragmento de datos de encabezado de secuencia (' StrD ') está presente, sigue el fragmento de formato de secuencia. El formato y el contenido de este fragmento se definen mediante el controlador del códec. Normalmente, los controladores usan esta información para la configuración. No es necesario que las aplicaciones que leen y escriben archivos AVI interpreten esta información; simplemente lo transfieren al controlador como un bloque de memoria y desde él.

El fragmento opcional ' STRN ' contiene una cadena de texto terminada en null que describe la secuencia.

Los encabezados de la secuencia de la lista ' HDRL ' se asocian con los datos de la secuencia de la lista ' movi ' según el orden de los fragmentos ' strl '. El primer fragmento ' strl ' se aplica al flujo 0, el segundo se aplica a la secuencia 1, y así sucesivamente.

## <a name="stream-data-movi-list"></a>Streaming de datos (lista ' movi ')

La información de encabezado siguiente es una lista de "movi" que contiene los datos reales de las secuencias, es decir, los fotogramas de vídeo y ejemplos de audio. Los fragmentos de datos pueden residir directamente en la lista ' movi ' o pueden estar agrupados en listas de ' Rec '. La agrupación ' Rec ' implica que los fragmentos agrupados se deben leer del disco todos a la vez y está destinado a los archivos que se intercalan en el CD-ROM.

El FOURCC que identifica cada fragmento de datos consta de un número de secuencia de dos dígitos seguido de un código de dos caracteres que define el tipo de información del fragmento.



| Código de dos caracteres | Descripción              |
|--------------------|--------------------------|
| db                 | Fotograma de vídeo sin comprimir |
| dc                 | Fotograma de vídeo comprimido   |
| pc                 | Cambio de paleta           |
| Pulsa                 | Datos de audio               |



 

Por ejemplo, si la secuencia 0 contiene audio, los fragmentos de datos de esa secuencia tendrían el valor de FOURCC ' 00wb '. Si el flujo 1 contiene vídeo, los fragmentos de datos de esa secuencia tendrían el FOURCC ' 01dB ' o ' 01dc '. Los fragmentos de datos de vídeo también pueden definir nuevas entradas de la paleta para actualizar la paleta durante una secuencia AVI. Cada fragmento de cambio de paleta (' xxpc ') contiene una estructura [**AVIPALCHANGE**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avipalchange) . Si una secuencia contiene cambios de paleta, establezca la marca **AVISF \_ video \_ PALCHANGES** en el miembro **dwFlags** de la estructura [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) para esa secuencia.

Los flujos de texto pueden usar códigos de dos caracteres arbitrarios.

## <a name="avi-index-entries"></a>Entradas de índice AVI

<dl> <dt>

<span id="AVI_1.0_index"></span><span id="avi_1.0_index"></span><span id="AVI_1.0_INDEX"></span>Índice de AVI 1,0
</dt> <dd>

Un fragmento de índice opcional (' idx1 ') puede seguir la lista ' movi '. El índice contiene una lista de los fragmentos de datos y su ubicación en el archivo. Consta de una estructura [**AVIOLDINDEX**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avioldindex) con entradas para cada fragmento de datos, incluidos fragmentos "REC". Si el archivo contiene un índice, establezca la marca **AVIF \_ HASINDEX** en el miembro **DwFlags** de la estructura [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) .

</dd> <dt>

<span id="AVI_2.0_index"></span><span id="avi_2.0_index"></span><span id="AVI_2.0_INDEX"></span>Índice de AVI 2,0
</dt> <dd>

Un índice AVI 2,0 puede aparecer como un solo fragmento. Como alternativa, los segmentos de índice se pueden intercalar dentro del fragmento ' movi '. Si los segmentos del índice se colocan en el fragmento "movi", un superíndice contiene un índice de los segmentos del índice. La estructura [**AVIMETAINDEX**](/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex) es la estructura base de los segmentos de índice y del superíndice. Para obtener más información, vea las *extensiones de formato de archivo AVI de OpenDML*, publicadas por el Subcomité formato de archivo AVI M-JPEG de OpenDML. (Es posible que este recurso no esté disponible en algunos idiomas y países).

</dd> </dl>

## <a name="other-data-chunks"></a>Otros fragmentos de datos

Los datos se pueden alinear en un archivo AVI insertando fragmentos ' no deseado ' según sea necesario. Las aplicaciones deben omitir el contenido de un fragmento de "correo no deseado".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de archivo AVI](avi-file-format.md)
</dt> </dl>

 

 
