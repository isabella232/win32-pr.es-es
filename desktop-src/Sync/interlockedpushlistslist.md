---
UID: ''
title: Función InterlockedPushListSList
description: Inserta una lista vinculada individualmente en la parte frontal de otra lista vinculada de forma individual.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: InterlockedPushListSListEx
ms.topic: reference
req.header:
- WinBase.h on Windows Vista, Windows 7, Windows Server 2008 and Windows Server 2008 R2
- InterlockedAPI.h on Windows 8 and Windows Server 2012
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-interlocked-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-interlocked-l1-1-0.dll
api_name:
- InterlockedPushListSList
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: ccecdae3af5119a86594c31856dac11ecb4507bc
ms.sourcegitcommit: be77ed1f97d3be57a2f42070589de21b66034adf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2020
ms.locfileid: "104420468"
---
# <a name="interlockedpushlistslist-function"></a><span data-ttu-id="8c7a0-103">Función InterlockedPushListSList</span><span class="sxs-lookup"><span data-stu-id="8c7a0-103">InterlockedPushListSList function</span></span>

## <a name="description"></a><span data-ttu-id="8c7a0-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c7a0-104">Description</span></span>

<span data-ttu-id="8c7a0-105">Inserta una lista vinculada individualmente en la parte frontal de otra lista vinculada de forma individual.</span><span class="sxs-lookup"><span data-stu-id="8c7a0-105">Inserts a singly-linked list at the front of another singly linked list.</span></span>
<span data-ttu-id="8c7a0-106">El acceso a las listas se sincroniza en un sistema con varios procesadores.</span><span class="sxs-lookup"><span data-stu-id="8c7a0-106">Access to the lists is synchronized on a multiprocessor system.</span></span>

```cpp
PSLIST_ENTRY  FASTCALL InterlockedPushListSList(
  _Inout_ PSLIST_HEADER ListHead,
  _Inout_ PSLIST_ENTRY  List,
  _Inout_ PSLIST_ENTRY  ListEnd,
  _In_    ULONG         Count
);
```

## <a name="parameters"></a><span data-ttu-id="8c7a0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c7a0-107">Parameters</span></span>

### <a name="listhead-in-out"></a><span data-ttu-id="8c7a0-108">ListHead [in, out]</span><span class="sxs-lookup"><span data-stu-id="8c7a0-108">ListHead [in, out]</span></span>

<span data-ttu-id="8c7a0-109">Puntero a una estructura de **SLIST_HEADER** que representa el encabezado de una lista vinculada individualmente.</span><span class="sxs-lookup"><span data-stu-id="8c7a0-109">Pointer to an **SLIST_HEADER** structure that represents the head of a singly linked list.</span></span>
<span data-ttu-id="8c7a0-110">La lista especificada por la *lista* y los parámetros *escuchados* se inserta al principio de esta lista.</span><span class="sxs-lookup"><span data-stu-id="8c7a0-110">The list specified by the *List* and *ListEnd* parameters is inserted at the front of this list.</span></span>

### <a name="list-in-out"></a><span data-ttu-id="8c7a0-111">List [in, out]</span><span class="sxs-lookup"><span data-stu-id="8c7a0-111">List [in, out]</span></span>

<span data-ttu-id="8c7a0-112">Puntero a una estructura de [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) que representa el primer elemento de la lista que se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="8c7a0-112">Pointer to an [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) structure that represents the first item in the list to be inserted.</span></span>

### <a name="listend-in-out"></a><span data-ttu-id="8c7a0-113">Escucha [in, out]</span><span class="sxs-lookup"><span data-stu-id="8c7a0-113">ListEnd [in, out]</span></span>

<span data-ttu-id="8c7a0-114">Puntero a una estructura de [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) que representa el último elemento de la lista que se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="8c7a0-114">Pointer to an [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) structure that represents the last item in the list to be inserted.</span></span>

### <a name="count-in"></a><span data-ttu-id="8c7a0-115">Recuento [in]</span><span class="sxs-lookup"><span data-stu-id="8c7a0-115">Count [in]</span></span>

<span data-ttu-id="8c7a0-116">Número de elementos de la lista que se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="8c7a0-116">The number of items in the list to be inserted.</span></span>

## <a name="returns"></a><span data-ttu-id="8c7a0-117">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="8c7a0-117">Returns</span></span>

<span data-ttu-id="8c7a0-118">El valor devuelto es el primer elemento de la lista especificado por el parámetro *ListHead* .</span><span class="sxs-lookup"><span data-stu-id="8c7a0-118">The return value is the previous first item in the list specified by the *ListHead* parameter.</span></span>
<span data-ttu-id="8c7a0-119">Si la lista estaba vacía previamente, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="8c7a0-119">If the list was previously empty, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c7a0-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c7a0-120">Remarks</span></span>

<span data-ttu-id="8c7a0-121">Todos los elementos de la lista se deben alinear en un límite de **MEMORY_ALLOCATION_ALIGNMENT** ; de lo contrario, esta función se comportará de forma impredecible.</span><span class="sxs-lookup"><span data-stu-id="8c7a0-121">All list items must be aligned on a **MEMORY_ALLOCATION_ALIGNMENT** boundary; otherwise, this function will behave unpredictably.</span></span>
<span data-ttu-id="8c7a0-122">Vea **_aligned_malloc**.</span><span class="sxs-lookup"><span data-stu-id="8c7a0-122">See **_aligned_malloc**.</span></span>

<span data-ttu-id="8c7a0-123">**Windows 8 y Windows Server 2012:**  Esta función se ha sustituido por [InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex).</span><span class="sxs-lookup"><span data-stu-id="8c7a0-123">**Windows 8 and Windows Server 2012:**  This function has been superceded by [InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex).</span></span>
<span data-ttu-id="8c7a0-124">Al compilar con **NTDDI_VERSION** establecido en **NTDDI_WIN8** o superior, las llamadas a **InterlockedPushListSList** Irán a **InterlockedPushListSListEx** en su lugar.</span><span class="sxs-lookup"><span data-stu-id="8c7a0-124">When compiling with **NTDDI_VERSION** set to **NTDDI_WIN8** or greater, calls to **InterlockedPushListSList** will go to **InterlockedPushListSListEx** instead.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c7a0-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c7a0-125">See also</span></span>

[<span data-ttu-id="8c7a0-126">Listas vinculadas de un solo vínculo</span><span class="sxs-lookup"><span data-stu-id="8c7a0-126">Interlocked Singly Linked Lists</span></span>](/windows/desktop/Sync/interlocked-singly-linked-lists)

[<span data-ttu-id="8c7a0-127">InterlockedPopEntrySList</span><span class="sxs-lookup"><span data-stu-id="8c7a0-127">InterlockedPopEntrySList</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)

[<span data-ttu-id="8c7a0-128">InterlockedPushEntrySList</span><span class="sxs-lookup"><span data-stu-id="8c7a0-128">InterlockedPushEntrySList</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)

[<span data-ttu-id="8c7a0-129">InterlockedPushListSListEx</span><span class="sxs-lookup"><span data-stu-id="8c7a0-129">InterlockedPushListSListEx</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)

[<span data-ttu-id="8c7a0-130">InterlockedFlushSList</span><span class="sxs-lookup"><span data-stu-id="8c7a0-130">InterlockedFlushSList</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedflushslist)

[<span data-ttu-id="8c7a0-131">SLIST_ENTRY</span><span class="sxs-lookup"><span data-stu-id="8c7a0-131">SLIST_ENTRY</span></span>](/windows/win32/api/winnt/ns-winnt-slist_entry)

[<span data-ttu-id="8c7a0-132">Usar listas vinculadas individualmente</span><span class="sxs-lookup"><span data-stu-id="8c7a0-132">Using Singly Linked Lists</span></span>](/windows/desktop/Sync/using-singly-linked-lists)
