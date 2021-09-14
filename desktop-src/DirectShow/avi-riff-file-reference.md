---
description: Referencia de archivo RIFF de AVI
ms.assetid: 2d8cf5be-1252-4b58-89b1-f5c53ea17d0e
title: Referencia de archivo RIFF de AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f28a7254ac9eb927381e313603ffd2bd0d050c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161712"
---
# <a name="avi-riff-file-reference"></a>Referencia de archivo RIFF de AVI

El formato de archivo AVI de Microsoft es una especificación de archivo RIFF que se usa con aplicaciones que capturan, editan y reproducen secuencias de audio y vídeo. En general, los archivos AVI contienen varios flujos de diferentes tipos de datos. La mayoría de las secuencias AVI usan secuencias de audio y vídeo. Una variación simple para una secuencia AVI usa datos de vídeo y no requiere una secuencia de audio.

En esta sección no se describen las extensiones de formato de archivo AVI de OpenDML. Para obtener más información sobre estas extensiones, vea Extensiones de formato de archivo AVI de *OpenDML, publicadas* por el subcomando de formato de archivo M-JPEG de OpenDML AVI.

## <a name="fourccs"></a>FOURCC

Un FOURCC (código de cuatro caracteres) es un entero de 32 bits sin signo creado mediante la concatenación de cuatro caracteres ASCII. Por ejemplo, fourcc "abcd" se representa en un sistema Little-Endian como 0x64636261. Los FOURCC pueden contener caracteres de espacio, por lo que "abc" es un FOURCC válido. El formato de archivo AVI usa códigos FOURCC para identificar tipos de secuencia, fragmentos de datos, entradas de índice y otra información.

## <a name="riff-file-format"></a>Formato de archivo RIFF

El formato de archivo AVI se basa en el formato de documento RIFF (formato de archivo de intercambio de recursos). Un archivo RIFF consta de un encabezado RIFF seguido de cero o más *listas* y *fragmentos*.

-   El encabezado RIFF tiene el formato siguiente:

    `'RIFF' fileSize fileType (data)`

    donde "RIFF" es el código FOURCC literal "RIFF", es un valor de 4 bytes que da el tamaño de los datos del archivo y es un FOURCC que identifica el tipo de archivo `fileSize` `fileType` específico. El valor de incluye el tamaño de FOURCC más el tamaño de los datos siguientes, pero no incluye el tamaño del FOURCC de `fileSize` `fileType` "RIFF" ni el tamaño de `fileSize` . Los datos de archivo constan de fragmentos y listas, en cualquier orden.

-   Un fragmento tiene el formato siguiente:

    `ckID ckSize ckData`

    donde es un FOURCC que identifica los datos contenidos en el fragmento, es un valor de 4 bytes que da el tamaño de los datos en y es cero o `ckID` `ckSize` más bytes de `ckData` `ckData` datos. Los datos siempre se agregan al límite **de WORD** más cercano. `ckSize` proporciona el tamaño de los datos válidos en el fragmento; no incluye el relleno, el tamaño de `ckID` o el tamaño de `ckSize` .

-   Una lista tiene el formato siguiente:

    `'LIST' listSize listType listData`

    donde "LIST" es el código FOURCC literal "LIST", es un valor de 4 bytes que da el tamaño de la lista, es un código FOURCC y consta de fragmentos o listas, en `listSize` `listType` cualquier `listData` orden. El valor de incluye el tamaño de más el tamaño de ; no incluye el `listSize` `listType` `listData` FOURCC "LIST" ni el tamaño de `listSize` .

En el resto de esta sección se usa la siguiente notación para describir fragmentos de RIFF:

`ckID ( ckData )`

donde el tamaño del fragmento es implícito. Con esta notación, una lista se puede representar como:

`'LIST' ( listType ( listData ) )`

Los elementos opcionales se colocan entre corchetes: `[ optional element ]`

## <a name="avi-riff-form"></a>Formulario RIFF de AVI

Los archivos AVI se identifican mediante FOURCC 'AVI' en el encabezado RIFF. Todos los archivos AVI incluyen dos fragmentos LIST obligatorios, que definen el formato de las secuencias y los datos del flujo, respectivamente. Un archivo AVI también puede incluir un fragmento de índice, que proporciona la ubicación de los fragmentos de datos dentro del archivo. Un archivo AVI con estos componentes tiene el formato siguiente:


```C++
RIFF ('AVI '
      LIST ('hdrl' ... )
      LIST ('movi' ... )
      ['idx1' (<AVI Index>) ]
     )
```



La lista "hdrl" define el formato de los datos y es el primer fragmento LIST necesario. La lista "muvi" contiene los datos de la secuencia AVI y es el segundo fragmento list necesario. La lista "idx1" contiene el índice. Los archivos AVI deben mantener estos tres componentes en la secuencia adecuada.

> [!Note]  
> Las extensiones OpenDML definen otro tipo de índice, identificado por fourCC 'indx'.

 

Las listas "hdrl" y "mcade" usan subchunks para sus datos. En el ejemplo siguiente se muestra el formulario RIFF de AVI expandido con los fragmentos necesarios para completar estas listas:


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

La lista "hdrl" comienza con el encabezado AVI principal, que se encuentra en un fragmento "avih". El encabezado principal contiene información global para todo el archivo AVI, como el número de secuencias dentro del archivo y el ancho y alto de la secuencia AVI. El fragmento de encabezado principal consta de una [**estructura AVIMAINHEADER.**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader)

## <a name="avi-stream-headers"></a>Encabezados de flujo AVI

Una o varias listas "strl" siguen el encabezado principal. Se requiere una lista "strl" para cada flujo de datos. Cada lista "strl" contiene información sobre una secuencia del archivo y debe contener un fragmento de encabezado de secuencia ('strh') y un fragmento de formato de secuencia ('strf'). Además, una lista "strl" podría contener un fragmento de datos de encabezado de flujo ('strd') y un fragmento de nombre de flujo ('strn').

El fragmento de encabezado de secuencia ('strh') consta de una [**estructura AVISTREAMHEADER.**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader)

Un fragmento de formato de secuencia ('strf') debe seguir el fragmento de encabezado de secuencia. El fragmento de formato de secuencia describe el formato de los datos de la secuencia. Los datos contenidos en este fragmento dependen del tipo de secuencia. En el caso de las secuencias de vídeo, la información es una [**estructura BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) incluida la información de la paleta si procede. En el caso de las secuencias de audio, la información es [**una estructura DE FORMASONATEX.**](/previous-versions/dd757713(v=vs.85))

Si el fragmento de datos de encabezado de flujo ('strd') está presente, sigue el fragmento de formato de secuencia. El formato y el contenido de este fragmento se definen mediante el controlador de códec. Normalmente, los controladores usan esta información para la configuración. Las aplicaciones que leen y escriben archivos AVI no necesitan interpretar esta información; simplemente lo transfieren hacia y desde el controlador como un bloque de memoria.

El fragmento opcional "strn" contiene una cadena de texto terminada en NULL que describe la secuencia.

Los encabezados de secuencia de la lista "hdrl" están asociados a los datos de secuencia de la lista "mcade" según el orden de los fragmentos "strl". El primer fragmento "strl" se aplica a la secuencia 0, el segundo se aplica a la secuencia 1, etc.

## <a name="stream-data-movi-list"></a>Stream Data ('mtransmisión' List)

A continuación de la información de encabezado se muestra una lista "mzone" que contiene los datos reales de las secuencias, es decir, los fotogramas de vídeo y los ejemplos de audio. Los fragmentos de datos pueden residir directamente en la lista "mdores", o bien se pueden agrupar dentro de listas "rec". La agrupación 'rec' implica que los fragmentos agrupados se deben leer desde el disco a la vez y está destinado a archivos intercalados para reproducirse desde CD-ROM.

El FOURCC que identifica cada fragmento de datos consta de un número de secuencia de dos dígitos seguido de un código de dos caracteres que define el tipo de información del fragmento.



| Código de dos caracteres | Descripción              |
|--------------------|--------------------------|
| db                 | Fotograma de vídeo sin comprimir |
| dc                 | Fotograma de vídeo comprimido   |
| pc                 | Cambio de paleta           |
| Wb                 | Datos de audio               |



 

Por ejemplo, si la secuencia 0 contiene audio, los fragmentos de datos de esa secuencia tendrían fourCC "00wb". Si la secuencia 1 contiene vídeo, los fragmentos de datos de esa secuencia tendrían FOURCC "01db" o "01dc". Los fragmentos de datos de vídeo también pueden definir nuevas entradas de paleta para actualizar la paleta durante una secuencia AVI. Cada fragmento de cambio de paleta ('xxpc') contiene una [**estructura AVIPALCHANGE.**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avipalchange) Si una secuencia contiene cambios en la paleta, establezca la marca **AVISF \_ VIDEO \_ PALCHANGES** en el **miembro dwFlags** de la [**estructura AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) de esa secuencia.

Las secuencias de texto pueden usar códigos arbitrarios de dos caracteres.

## <a name="avi-index-entries"></a>Entradas de índice AVI

<dl> <dt>

<span id="AVI_1.0_index"></span><span id="avi_1.0_index"></span><span id="AVI_1.0_INDEX"></span>Índice AVI 1.0
</dt> <dd>

Un fragmento de índice opcional ('idx1') puede seguir la lista 'mdice'. El índice contiene una lista de los fragmentos de datos y su ubicación en el archivo. Consta de una estructura [**AVIOLDINDEX con**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avioldindex) entradas para cada fragmento de datos, incluidos los fragmentos "rec". Si el archivo contiene un índice, establezca la marca **\_ AVIF HASINDEX** en el **miembro dwFlags** de la [**estructura AVIMAINHEADER.**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader)

</dd> <dt>

<span id="AVI_2.0_index"></span><span id="avi_2.0_index"></span><span id="AVI_2.0_INDEX"></span>Índice AVI 2.0
</dt> <dd>

Un índice AVI 2.0 puede aparecer como un único fragmento. Como alternativa, los segmentos de índice se pueden intercalar dentro del fragmento "mzado". Si los segmentos de índice se colocan en el fragmento 'mmico', un superíndice contiene un índice de los segmentos de índice. La [**estructura AVIMETAINDEX**](/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex) es la estructura base para los segmentos de índice y el superíndice. Para más información, consulte las extensiones de formato de archivo AVI de *OpenDML, publicadas* por la subcomisión Formato de archivo M-JPEG de OpenDML AVI. (Es posible que este recurso no esté disponible en algunos idiomas y países).

</dd> </dl>

## <a name="other-data-chunks"></a>Otros fragmentos de datos

Los datos se pueden alinear en un archivo AVI insertando fragmentos "SPAM" según sea necesario. Las aplicaciones deben omitir el contenido de un fragmento "SPAM".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de archivo AVI](avi-file-format.md)
</dt> </dl>

 

 
