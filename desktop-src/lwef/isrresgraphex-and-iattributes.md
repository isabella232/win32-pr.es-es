---
title: ISRResGraphEx y IAttributes
description: ISRResGraphEx y IAttributes
ms.assetid: 6eb37da1-5252-4c41-891c-c19cca6fb7d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659d7d4723bfc5145fb8abcc77043031a0e48e8b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077580"
---
# <a name="isrresgraphex-and-iattributes"></a>ISRResGraphEx y IAttributes

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Los objetos de resultados devueltos por el motor deben admitir la interfaz ISRResGraphEx y la interfaz IAttributes. La simple compatibilidad con la interfaz ISRResGraphEx es suficiente para permitir que el editor de sonido proporcione información de separación de palabras, pero no proporciona la compatibilidad necesaria con la información de fonema.

El editor de sonidos requiere que los motores también admitan un atributo DWord especial, **SRATTR \_ PHONESEG**. El editor consulta los motores para ver la interfaz IAttributes e intenta establecer **SRATTR \_ PHONESEG** en 1. Si la llamada se realiza correctamente, el editor de sonido supone que los resultados del motor admitirán la recopilación de información de segmentación de fonemas del objeto de resultados.

`#define    SRATTR_PHONESEG    MAKELONG (1, SRVEN_MICROSOFT)`

Cuando un objeto de resultados se transmite al editor de sonido, consulta ese objeto para su implementación de ISRResGraphEx. ISRResGraphEx contiene una función miembro, DataGet, con la signatura de tipo

`HRESULT  DataGet  (DWord, dwID, GUID gAttrib, SDATA *psData)`

Donde **dwID** es el identificador del objeto de gráfico, **GATTRIB** es un GUID que se corresponde con el atributo buscado y **psData** es un puntero a un objeto SDATA que contiene los datos devueltos. El motor es responsable de la asignación de los datos almacenados en **psData** a través de [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc). La aplicación que realiza la llamada (en este caso, el editor de sonidos) es responsable de liberarla a través de [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) cuando ha finalizado.

DataGet es necesario para reconocer tres GUID predefinidos, que se enumeran en la documentación de SAPI. Un motor que devuelve un código de operación correcta a la llamada a **DWORDSet (SRATTR \_ PHONESEG, 1)** también es necesario para reconocer un GUID específico, **SRGARC \_ PHONEMESEGMENTATION**, cuando se llama con un **dwID** que corresponde a un borde del gráfico.

`DEFINE_GUID(SRGARC_PHONMESEGMENTATION, 0xd05405b0, 0x1db1, 0x11d2, 0x94, 0x2, 0x0, 0xc0, 0x4f, 0x8e, 0xf4, 0x8f);`

Cuando se devuelve la llamada, **psData** debe apuntar a una matriz de estructura alineada con DWORD de tipo **PHONESEG**, definida por:

``` syntax
typedef struct tagSRPHONESEG {
   DWORD   dwSize;       // Size of the SRPHONESEG structure + phone data
   QWORD   qwStartTime;  // SAPI timestamp of the start of the seqment
   …QWORD   qwEndTime;    // SAPI timestamp of the end of the seqment
   int      nScore;      // The segment's score
   WCHAR   aPhones[0];   // Array of phone(s) making up the segment
} SRPHONESEG,  *PSRPHONESEG;
```

donde **qwStartTime** y **qwEndTime** apuntan al principio y al final de cada fonema que conforman la palabra incluida en el borde y **aPhones** es una matriz de caracteres Unicode correspondientes a la representación del IPA del teléfono, que se han producido en este segmento. (En algunos idiomas, hay fonemas que están escritas con más de un fonema de IPA. En inglés, por ejemplo, el sonido "Long I" de la palabra "Live" es realmente un diptongo, compuesto por dos fonemas más simples concatenados juntos). La matriz **aPhones** debe terminar en cero y rellenarse al final para que cada estructura **SRPHONESEG** de la matriz sea un múltiplo par de cuatro bytes de longitud.

Por ejemplo, supongamos que la palabra hablado en el arco 4 fue "hecha". A continuación, la llamada a DataGet (4, **SRGARC \_ PHONEMESEGMENTATION**, &SD) puede devolver una matriz de tres segmentos de fonema,/m/que se ejecuta desde **qwStartTime**= 328434 bytes a **qwEndTime**= 330354 bytes,/1e/que se ejecuta desde **qwStartTime**= 330354 bytes hasta **qwEndTime**= 344114 bytes y/d/ejecutándose desde **qwStartTime**= 344114 bytes a **qwEndTime**= 347314 bytes. Estos se presentarían como una matriz empaquetada de tres estructuras **SRPHONESEG** de los tamaños 28, 32 y 28 bytes, respectivamente. Observe que hay algún relleno al final de la estructura **SRPHONESEG** central, de modo que el siguiente elemento de la matriz se inicie en un límite de 4 bytes.

El SDK de SAPI 4,0 incluye una herramienta (SRFunc) para probar el cumplimiento con la especificación de SAPI 4,0. En esa herramienta se incluye una prueba para la compatibilidad con este conjunto de interfaces. El código fuente de esa herramienta es un buen punto de partida para entender cómo interactúan estas interfaces con el editor de sonido y para depurar las interfaces durante el desarrollo.

 

 