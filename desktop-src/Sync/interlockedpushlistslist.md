---
UID: ''
title: Función InterlockedPushListSList
description: Inserta una lista vinculada de forma singly al frente de otra lista vinculada de forma singly.
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
ms.openlocfilehash: f2a13003b1b850431bac87a2ca02bbf093bc67dc9207e317b2c602bde83e15b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117959242"
---
# <a name="interlockedpushlistslist-function"></a>Función InterlockedPushListSList

## <a name="description"></a>Descripción

Inserta una lista vinculada de forma singly al frente de otra lista vinculada de forma singly.
El acceso a las listas se sincroniza en un sistema de varios procesadores.

```cpp
PSLIST_ENTRY  FASTCALL InterlockedPushListSList(
  _Inout_ PSLIST_HEADER ListHead,
  _Inout_ PSLIST_ENTRY  List,
  _Inout_ PSLIST_ENTRY  ListEnd,
  _In_    ULONG         Count
);
```

## <a name="parameters"></a>Parámetros

### <a name="listhead-in-out"></a>ListHead [in, out]

Puntero a una **SLIST_HEADER** estructura que representa el responsable de una lista vinculada de forma singly.
La lista especificada por los parámetros *List* *y ListEnd* se inserta al frente de esta lista.

### <a name="list-in-out"></a>Enumerar [in, out]

Puntero a una [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) estructura que representa el primer elemento de la lista que se va a insertar.

### <a name="listend-in-out"></a>ListEnd [in, out]

Puntero a una [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) estructura que representa el último elemento de la lista que se va a insertar.

### <a name="count-in"></a>Recuento [in]

Número de elementos de la lista que se va a insertar.

## <a name="returns"></a>Devoluciones

El valor devuelto es el primer elemento anterior de la lista especificada por el *parámetro ListHead.*
Si la lista estaba vacía anteriormente, el valor devuelto es **NULL.**

## <a name="remarks"></a>Comentarios

Todos los elementos de lista deben estar alineados en un **MEMORY_ALLOCATION_ALIGNMENT** límite; De lo contrario, esta función se comportará de forma impredecible.
Vea **_aligned_malloc**.

**Windows 8 y Windows Server 2012:**  [InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)ha supercedido esta función.
Al compilar con **NTDDI_VERSION** establecido en NTDDI_WIN8 o superior, las llamadas a **InterlockedPushListSList** irán **a** **InterlockedPushListSListEx** en su lugar.

## <a name="see-also"></a>Vea también

[Listas vinculadas de Singly entrelazados](/windows/desktop/Sync/interlocked-singly-linked-lists)

[InterlockedPopEntrySList](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)

[InterlockedPushEntrySList](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)

[InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)

[InterlockedFlushSList](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedflushslist)

[SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry)

[Uso de listas vinculadas de Singly](/windows/desktop/Sync/using-singly-linked-lists)
