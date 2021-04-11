---
description: Define métodos que controlan los eventos de la interfaz ITablet.
ms.assetid: 9acf32fa-b33f-4b9a-be73-804b7d5434e8
title: Interfaz ITabletEventSink
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fc42bfe8a6e69504c35d7926c4c5a8b688404897
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279173"
---
# <a name="itableteventsink-interface"></a><span data-ttu-id="2b0e9-103">Interfaz ITabletEventSink</span><span class="sxs-lookup"><span data-stu-id="2b0e9-103">ITabletEventSink interface</span></span>

<span data-ttu-id="2b0e9-104">Define métodos que controlan los eventos de la [**interfaz ITablet**](itablet.md) .</span><span class="sxs-lookup"><span data-stu-id="2b0e9-104">Defines methods that handle the [**ITablet Interface**](itablet.md) events.</span></span>

## <a name="members"></a><span data-ttu-id="2b0e9-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="2b0e9-105">Members</span></span>

<span data-ttu-id="2b0e9-106">La interfaz **ITabletEventSink** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2b0e9-106">The **ITabletEventSink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2b0e9-107">**ITabletEventSink** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2b0e9-107">**ITabletEventSink** also has these types of members:</span></span>

-   [<span data-ttu-id="2b0e9-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="2b0e9-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2b0e9-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="2b0e9-109">Methods</span></span>

<span data-ttu-id="2b0e9-110">La interfaz **ITabletEventSink** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2b0e9-110">The **ITabletEventSink** interface has these methods.</span></span>



| <span data-ttu-id="2b0e9-111">Método</span><span class="sxs-lookup"><span data-stu-id="2b0e9-111">Method</span></span>                                                        | <span data-ttu-id="2b0e9-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b0e9-112">Description</span></span>                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b0e9-113">**ContextCreate**</span><span class="sxs-lookup"><span data-stu-id="2b0e9-113">**ContextCreate**</span></span>](itableteventsink-contextcreate.md)       | <span data-ttu-id="2b0e9-114">Se produce cuando se crea un nuevo contexto de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="2b0e9-114">Occurs when a new tablet context is created.</span></span><br/>                                          |
| [<span data-ttu-id="2b0e9-115">**ContextDestroy**</span><span class="sxs-lookup"><span data-stu-id="2b0e9-115">**ContextDestroy**</span></span>](itableteventsink-contextdestroy.md)     | <span data-ttu-id="2b0e9-116">Se produce cuando se destruye un contexto de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="2b0e9-116">Occurs when a tablet context is being destroyed.</span></span><br/>                                      |
| [<span data-ttu-id="2b0e9-117">**CursorDown**</span><span class="sxs-lookup"><span data-stu-id="2b0e9-117">**CursorDown**</span></span>](itableteventsink-cursordown.md)             | <span data-ttu-id="2b0e9-118">Se produce cuando la punta del lápiz se pone en contacto con la superficie de la tableta de la digitalización.</span><span class="sxs-lookup"><span data-stu-id="2b0e9-118">Occurs when the stylus tip contacts the digitizing tablet surface.</span></span><br/>                    |
| [<span data-ttu-id="2b0e9-119">**CursorInRange**</span><span class="sxs-lookup"><span data-stu-id="2b0e9-119">**CursorInRange**</span></span>](itableteventsink-cursorinrange.md)       | <span data-ttu-id="2b0e9-120">Se produce cuando un lápiz entra dentro del intervalo de detección del digitalizador.</span><span class="sxs-lookup"><span data-stu-id="2b0e9-120">Occurs when a stylus comes within the digitizer's range of detection.</span></span><br/>                 |
| [<span data-ttu-id="2b0e9-121">**CursorMove**</span><span class="sxs-lookup"><span data-stu-id="2b0e9-121">**CursorMove**</span></span>](itableteventsink-cursormove.md)             | <span data-ttu-id="2b0e9-122">Se produce cuando el cursor se mueve sobre el digitalizador de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="2b0e9-122">Occurs when the cursor moves over the tablet digitizer.</span></span><br/>                               |
| [<span data-ttu-id="2b0e9-123">**CursorNew**</span><span class="sxs-lookup"><span data-stu-id="2b0e9-123">**CursorNew**</span></span>](itableteventsink-cursornew.md)               | <span data-ttu-id="2b0e9-124">Se produce cuando se agrega un nuevo lápiz al sistema.</span><span class="sxs-lookup"><span data-stu-id="2b0e9-124">Occurs when a new stylus is added to the system.</span></span><br/>                                      |
| [<span data-ttu-id="2b0e9-125">**CursorOutOfRange**</span><span class="sxs-lookup"><span data-stu-id="2b0e9-125">**CursorOutOfRange**</span></span>](itableteventsink-cursoroutofrange.md) | <span data-ttu-id="2b0e9-126">Se produce cuando el lápiz deja el intervalo de detección física (proximidad) de la tableta.</span><span class="sxs-lookup"><span data-stu-id="2b0e9-126">Occurs when the stylus leaves the physical detection range (proximity) of the tablet.</span></span><br/> |
| [<span data-ttu-id="2b0e9-127">**CursorUp**</span><span class="sxs-lookup"><span data-stu-id="2b0e9-127">**CursorUp**</span></span>](itableteventsink-cursorup.md)                 | <span data-ttu-id="2b0e9-128">Se produce cuando el usuario ha generado el lápiz óptico desde la superficie del digitalizador de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="2b0e9-128">Occurs when the user has raised the stylus from the tablet digitizer surface.</span></span><br/>         |
| [<span data-ttu-id="2b0e9-129">**Paquetes**</span><span class="sxs-lookup"><span data-stu-id="2b0e9-129">**Packets**</span></span>](itableteventsink-packets.md)                   | <span data-ttu-id="2b0e9-130">Se produce cuando el lápiz óptico se mueve en el digitalizador.</span><span class="sxs-lookup"><span data-stu-id="2b0e9-130">Occurs when the stylus is moving on the digitizer.</span></span><br/>                                    |
| [<span data-ttu-id="2b0e9-131">**SystemEvent**</span><span class="sxs-lookup"><span data-stu-id="2b0e9-131">**SystemEvent**</span></span>](itableteventsink-systemevent.md)           | <span data-ttu-id="2b0e9-132">Se produce cuando hay un evento del sistema disponible.</span><span class="sxs-lookup"><span data-stu-id="2b0e9-132">Occurs when a system event is available.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="2b0e9-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b0e9-133">Remarks</span></span>

<span data-ttu-id="2b0e9-134">Los desarrolladores no deben utilizar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="2b0e9-134">Developers should not use this interface.</span></span>

<span data-ttu-id="2b0e9-135">En el código siguiente se muestra cómo se define la interfaz **ITabletEventSink** .</span><span class="sxs-lookup"><span data-stu-id="2b0e9-135">The following code shows how the **ITabletEventSink** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(788459C8-26C8-4666-BF57-04AD3A0A5EB5),
    pointer_default(unique)
]
interface ITabletEventSink: IUnknown
{

    HRESULT ContextCreate(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT ContextDestroy(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT CursorNew(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorInRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorOutOfRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorDown(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT CursorUp(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT Packets(
        [in] TABLET_CONTEXT_ID tcid,
        [in] ULONG cPkts,
        [in] ULONG cbPkts,
        [in, size_is(cbPkts)] BYTE * pbPkts,
        [in, unique, size_is(cPkts)
#ifndef NT_TARGET_XP
         ,disable_consistency_check
#endif
        ] ULONG *pnSerialNumbers,
        [in] CURSOR_ID cid
    );

    HRESULT SystemEvent(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] SYSTEM_EVENT event,
        [in] SYSTEM_EVENT_DATA eventdata
    );
};

     
```

## <a name="requirements"></a><span data-ttu-id="2b0e9-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b0e9-136">Requirements</span></span>



| <span data-ttu-id="2b0e9-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b0e9-137">Requirement</span></span> | <span data-ttu-id="2b0e9-138">Value</span><span class="sxs-lookup"><span data-stu-id="2b0e9-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b0e9-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b0e9-139">Minimum supported client</span></span><br/> | <span data-ttu-id="2b0e9-140">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2b0e9-140">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2b0e9-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b0e9-141">Minimum supported server</span></span><br/> | <span data-ttu-id="2b0e9-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2b0e9-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2b0e9-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2b0e9-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="2b0e9-144"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2b0e9-144"><dt>Wisptis.exe</dt></span></span> </dl> |



 

