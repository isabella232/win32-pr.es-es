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
# <a name="interlockedpushlistslist-function"></a>Función InterlockedPushListSList

## <a name="description"></a>Descripción

Inserta una lista vinculada individualmente en la parte frontal de otra lista vinculada de forma individual.
El acceso a las listas se sincroniza en un sistema con varios procesadores.

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

Puntero a una estructura de **SLIST_HEADER** que representa el encabezado de una lista vinculada individualmente.
La lista especificada por la *lista* y los parámetros *escuchados* se inserta al principio de esta lista.

### <a name="list-in-out"></a>List [in, out]

Puntero a una estructura de [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) que representa el primer elemento de la lista que se va a insertar.

### <a name="listend-in-out"></a>Escucha [in, out]

Puntero a una estructura de [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) que representa el último elemento de la lista que se va a insertar.

### <a name="count-in"></a>Recuento [in]

Número de elementos de la lista que se va a insertar.

## <a name="returns"></a>Devoluciones

El valor devuelto es el primer elemento de la lista especificado por el parámetro *ListHead* .
Si la lista estaba vacía previamente, el valor devuelto es **null**.

## <a name="remarks"></a>Observaciones

Todos los elementos de la lista se deben alinear en un límite de **MEMORY_ALLOCATION_ALIGNMENT** ; de lo contrario, esta función se comportará de forma impredecible.
Vea **_aligned_malloc**.

**Windows 8 y Windows Server 2012:**  Esta función se ha sustituido por [InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex).
Al compilar con **NTDDI_VERSION** establecido en **NTDDI_WIN8** o superior, las llamadas a **InterlockedPushListSList** Irán a **InterlockedPushListSListEx** en su lugar.

## <a name="see-also"></a>Vea también

[Listas vinculadas de un solo vínculo](/windows/desktop/Sync/interlocked-singly-linked-lists)

[InterlockedPopEntrySList](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)

[InterlockedPushEntrySList](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)

[InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)

[InterlockedFlushSList](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedflushslist)

[SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry)

[Usar listas vinculadas individualmente](/windows/desktop/Sync/using-singly-linked-lists)
