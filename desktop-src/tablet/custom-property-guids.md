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
# <a name="custom-property-guids"></a><span data-ttu-id="35b5c-103">GUID de propiedad personalizada</span><span class="sxs-lookup"><span data-stu-id="35b5c-103">Custom Property GUIDs</span></span>

<span data-ttu-id="35b5c-104">Windows Journal usa los siguientes identificadores únicos globales (GUID) para identificar propiedades personalizadas en trazos o atributos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="35b5c-104">The following globally unique identifiers (GUIDs) are used by Windows Journal to identify custom properties on strokes or drawing attributes.</span></span>

## <a name="guid_stroke_timestamp"></a><span data-ttu-id="35b5c-105">marca de tiempo de trazo de GUID \_ \_</span><span class="sxs-lookup"><span data-stu-id="35b5c-105">GUID\_STROKE\_TIMESTAMP</span></span>


```C++
GUID_STROKE_TIMESTAMP = {4EA66C4-F33A-461B-B8FE-68070D9C7575}
```



<span data-ttu-id="35b5c-106">Se trata de una estructura de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) que indica la hora a la que se creó el trazo o se agregó al documento.</span><span class="sxs-lookup"><span data-stu-id="35b5c-106">This is a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure that indicates the time at which the stroke was created or added to the document.</span></span>


```C++
typedef struct _FILETIME {
    DWORD dwLowDateTime;
    DWORD dwHighDateTime;
} FILETIME, *PFILETIME;
```



## <a name="guid_stroke_timeid"></a><span data-ttu-id="35b5c-107">\_TIMEID de trazo de GUID \_</span><span class="sxs-lookup"><span data-stu-id="35b5c-107">GUID\_STROKE\_TIMEID</span></span>


```C++
GUID_STROKE_TIMEID = {50B6BC8-3B7D-4816-8C61-BC7E905B2132}
```



<span data-ttu-id="35b5c-108">Se trata de una estructura **TIMEID** .</span><span class="sxs-lookup"><span data-stu-id="35b5c-108">This is a **TIMEID** structure.</span></span> <span data-ttu-id="35b5c-109">Permite mantener el orden de los trazos en las operaciones de pegar y colocar.</span><span class="sxs-lookup"><span data-stu-id="35b5c-109">It allows stroke order to be maintained across paste and drop operations.</span></span> <span data-ttu-id="35b5c-110">Sin la estructura **TIMEID** , la marca de tiempo de todos los objetos de [**interfaz IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) cortados y pegados en una [colección InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) será la misma.</span><span class="sxs-lookup"><span data-stu-id="35b5c-110">Without the **TIMEID** structure, the timestamp for all [**IInkStrokeDisp Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects cut and pasted in a [InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) will be the same.</span></span>


```C++
typedef struct tagTIMEID {
    FILETIME  tmFiletime;
    ULONG     uiOrder;
} TIMEID;
```



## <a name="guid_highlighter"></a><span data-ttu-id="35b5c-111">\_marcador de resaltado de GUID</span><span class="sxs-lookup"><span data-stu-id="35b5c-111">GUID\_HIGHLIGHTER</span></span>

<span data-ttu-id="35b5c-112">Se trata de un valor **booleano**, donde **true**= tinta de marcador de resaltado, **false**= entrada de lápiz normal.</span><span class="sxs-lookup"><span data-stu-id="35b5c-112">This is a **BOOL**, where **TRUE**=highlighter ink, **FALSE**=regular ink.</span></span> <span data-ttu-id="35b5c-113">Esto se aplica a los atributos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="35b5c-113">This is applied to drawing attributes.</span></span>


```C++
GUID_HIGHLIGHTER = {9B6267B8-3968-4048-AB74-F490406A2DFA}
```



## <a name="guid_ink_style_bold"></a><span data-ttu-id="35b5c-114">estilo de tinta de GUID en \_ \_ \_ negrita</span><span class="sxs-lookup"><span data-stu-id="35b5c-114">GUID\_INK\_STYLE\_BOLD</span></span>

<span data-ttu-id="35b5c-115">Se trata de un valor **booleano**, donde **true**= tinta negrita, **false**= normal.</span><span class="sxs-lookup"><span data-stu-id="35b5c-115">This is a **BOOL**, where **TRUE**=bold ink, **FALSE**=normal.</span></span> <span data-ttu-id="35b5c-116">Esto se aplica a los atributos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="35b5c-116">This is applied to drawing attributes.</span></span>


```C++
GUID_INK_STYLE_BOLD = {E02FB5C1-9693-4312-A434-00DE7F3AD493}
```



## <a name="guid_ink_style_italics"></a><span data-ttu-id="35b5c-117">estilo de tinta de GUID en \_ \_ \_ cursiva</span><span class="sxs-lookup"><span data-stu-id="35b5c-117">GUID\_INK\_STYLE\_ITALICS</span></span>

<span data-ttu-id="35b5c-118">Es un valor **booleano**, donde **true**= tinta en cursiva, **false**= normal.</span><span class="sxs-lookup"><span data-stu-id="35b5c-118">This is a **BOOL**, where **TRUE**=italicized ink, **FALSE**=normal.</span></span> <span data-ttu-id="35b5c-119">Esto se aplica a los atributos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="35b5c-119">This is applied to drawing attributes.</span></span>


```C++
GUID_INK_STYLE_ITALICS = {05253B51-49C6-4A04-8993-64DD9ABD842A}
```



## <a name="related-topics"></a><span data-ttu-id="35b5c-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="35b5c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35b5c-121">**Interfaz IJournalReader**</span><span class="sxs-lookup"><span data-stu-id="35b5c-121">**IJournalReader Interface**</span></span>](ijournalreader.md)
</dt> </dl>

 

 
