---
description: Windows Journal usa los siguientes identificadores únicos globales (GUID) para identificar propiedades personalizadas en trazos o atributos de dibujo.
ms.assetid: a7488c26-b61f-47d8-a19b-d630a8c00875
title: GUID de propiedad personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d9069f2c655f658752a6ae3891910ff68103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697572"
---
# <a name="custom-property-guids"></a>GUID de propiedad personalizada

Windows Journal usa los siguientes identificadores únicos globales (GUID) para identificar propiedades personalizadas en trazos o atributos de dibujo.

## <a name="guid_stroke_timestamp"></a>marca de tiempo de trazo de GUID \_ \_


```C++
GUID_STROKE_TIMESTAMP = {4EA66C4-F33A-461B-B8FE-68070D9C7575}
```



Se trata de una estructura de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) que indica la hora a la que se creó el trazo o se agregó al documento.


```C++
typedef struct _FILETIME {
    DWORD dwLowDateTime;
    DWORD dwHighDateTime;
} FILETIME, *PFILETIME;
```



## <a name="guid_stroke_timeid"></a>\_TIMEID de trazo de GUID \_


```C++
GUID_STROKE_TIMEID = {50B6BC8-3B7D-4816-8C61-BC7E905B2132}
```



Se trata de una estructura **TIMEID** . Permite mantener el orden de los trazos en las operaciones de pegar y colocar. Sin la estructura **TIMEID** , la marca de tiempo de todos los objetos de [**interfaz IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) cortados y pegados en una [colección InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) será la misma.


```C++
typedef struct tagTIMEID {
    FILETIME  tmFiletime;
    ULONG     uiOrder;
} TIMEID;
```



## <a name="guid_highlighter"></a>\_marcador de resaltado de GUID

Se trata de un valor **booleano**, donde **true**= tinta de marcador de resaltado, **false**= entrada de lápiz normal. Esto se aplica a los atributos de dibujo.


```C++
GUID_HIGHLIGHTER = {9B6267B8-3968-4048-AB74-F490406A2DFA}
```



## <a name="guid_ink_style_bold"></a>estilo de tinta de GUID en \_ \_ \_ negrita

Se trata de un valor **booleano**, donde **true**= tinta negrita, **false**= normal. Esto se aplica a los atributos de dibujo.


```C++
GUID_INK_STYLE_BOLD = {E02FB5C1-9693-4312-A434-00DE7F3AD493}
```



## <a name="guid_ink_style_italics"></a>estilo de tinta de GUID en \_ \_ \_ cursiva

Es un valor **booleano**, donde **true**= tinta en cursiva, **false**= normal. Esto se aplica a los atributos de dibujo.


```C++
GUID_INK_STYLE_ITALICS = {05253B51-49C6-4A04-8993-64DD9ABD842A}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IJournalReader**](ijournalreader.md)
</dt> </dl>

 

 
