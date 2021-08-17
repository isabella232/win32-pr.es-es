---
title: ISRResGraphEx e IAttributes
description: ISRResGraphEx e IAttributes
ms.assetid: 6eb37da1-5252-4c41-891c-c19cca6fb7d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81f5e08b77b917e4630afcaeb8baed5aac4e13c20a1ed289418681abbbdca20b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749001"
---
# <a name="isrresgraphex-and-iattributes"></a>ISRResGraphEx e IAttributes

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Los objetos de resultados devueltos por el motor deben admitir la interfaz ISRResGraphEx y la interfaz IAttributes. Simplemente admitir la interfaz ISRResGraphEx es suficiente para permitir que el editor de sonido proporcione información de salto de palabras, pero no proporciona la compatibilidad necesaria para la información de phoneme.

El editor de sonido requiere que los motores también admitan un atributo DWord especial, **SRATTR \_ PHONESEG**. El editor consulta los motores para ver la interfaz IAttributes e intenta establecer **SRATTR \_ PHONESEG** en 1. Si esa llamada se realiza correctamente, el editor de sonido da por supuesto que los resultados del motor admitirán la recopilación de información de segmentación de phoneme del objeto de resultados.

`#define    SRATTR_PHONESEG    MAKELONG (1, SRVEN_MICROSOFT)`

Cuando un objeto de resultados se transmite al editor de sonido, consulta ese objeto para su implementación de ISRResGraphEx. ISRResGraphEx contiene una función miembro, DataGet, con firma de tipo

`HRESULT  DataGet  (DWord, dwID, GUID gAttrib, SDATA *psData)`

Donde **dwID** es el identificador del objeto de grafo, **gAttrib** es un GUID correspondiente al atributo buscado y **psData** es un puntero a un objeto SDATA que contiene los datos devueltos. El motor es responsable de asignar los datos almacenados en **psData** a través [**de CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc). La aplicación que realiza la llamada (en este caso, el editor de sonido) es responsable de liberarla a través de [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) cuando haya terminado.

DataGet es necesario para reconocer tres GUID predefinidos, que se enumeran en la documentación de SAPI. Un motor que devuelve un código correcto a la llamada a **DWORDSet(SRATTR \_ PHONESEG, 1)** también es necesario para reconocer un GUID específico, **SRGARC \_ PHONEMESEGMENTATION,** cuando se llama con un **dwID** que corresponde a un borde en el gráfico.

`DEFINE_GUID(SRGARC_PHONMESEGMENTATION, 0xd05405b0, 0x1db1, 0x11d2, 0x94, 0x2, 0x0, 0xc0, 0x4f, 0x8e, 0xf4, 0x8f);`

Cuando se devuelve la llamada, **psData** debe apuntar a una matriz de estructura alineada con DWORD de tipo **PHONESEG,** definida por:

``` syntax
typedef struct tagSRPHONESEG {
   DWORD   dwSize;       // Size of the SRPHONESEG structure + phone data
   QWORD   qwStartTime;  // SAPI timestamp of the start of the seqment
   …QWORD   qwEndTime;    // SAPI timestamp of the end of the seqment
   int      nScore;      // The segment's score
   WCHAR   aPhones[0];   // Array of phone(s) making up the segment
} SRPHONESEG,  *PSRPHONESEG;
```

donde **qwStartTime** y **qwEndTime** apuntan al principio y al final de cada phonema que forma la palabra cubierta por el borde, y **aPhones** es una matriz de caracteres Unicode correspondientes a la representación IPA del teléfono, que se produjeron en este segmento. (En algunos idiomas, hay phonemas que se escriben con más de un phonema IPA. En inglés, por ejemplo, el sonido "long I" de la palabra "live" es en realidad una diphtong, que se forma con dos phonemas más sencillos concatenados). La **matriz aPhones** debe terminarse en cero y agregarse al final para que cada estructura **SRPHONESEG** de la matriz tenga incluso un múltiplo de cuatro bytes de longitud.

Por ejemplo, supongamos que la palabra hablada en arc 4 se "hizo". A continuación, la llamada a DataGet(4, **SRGARC \_ PHONEMESEGMENTATION**, &sd) podría devolver una matriz de tres segmentos de phonema, /m/ que se ejecuta desde **qwStartTime**=328434 bytes hasta **qwEndTime**=330354 bytes, /1e/ que se ejecuta desde **qwStartTime**=330354 bytes hasta **qwEndTime**=344114 bytes y /d/ que se ejecuta desde **qwStartTime**=344114 bytes a **qwEndTime**=347314 bytes. Se presentarían como una matriz empaquetada de tres estructuras **SRPHONESEG** de tamaños de 28, 32 y 28 bytes, respectivamente. Observe que hay cierto relleno al final de la estructura **SRPHONESEG** central, de modo que el siguiente elemento de la matriz comienza en un límite de 4 bytes.

El SDK de SAPI 4.0 incluye una herramienta (SRFunc) para probar el cumplimiento con la especificación SAPI 4.0. En esa herramienta se incluye una prueba para comprobar el cumplimiento de este conjunto de interfaces. El código fuente de esa herramienta es un buen punto de inicio para comprender cómo interactuarán estas interfaces con el editor de sonido y para depurar las interfaces durante el desarrollo.

 

 