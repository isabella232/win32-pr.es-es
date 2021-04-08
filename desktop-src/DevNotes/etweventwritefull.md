---
description: Escribe un evento completo en una sesión.
title: EtwEventWriteFull
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWriteFull
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: 5ea3de0dba842544b0ffacc785fb138bdda571a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000705"
---
# <a name="etweventwritefull-function"></a><span data-ttu-id="9ec95-103">EtwEventWriteFull función)</span><span class="sxs-lookup"><span data-stu-id="9ec95-103">EtwEventWriteFull function</span></span>

<span data-ttu-id="9ec95-104">[La función EtwEventWriteFull y las estructuras que devuelve son internas del sistema operativo y están sujetas a cambios de una versión de Windows a otra.]</span><span class="sxs-lookup"><span data-stu-id="9ec95-104">[The EtwEventWriteFull function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.]</span></span>

<span data-ttu-id="9ec95-105">Escribe un evento completo en una sesión.</span><span class="sxs-lookup"><span data-stu-id="9ec95-105">Writes a full event to a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ec95-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ec95-106">Syntax</span></span>

```C++
ULONG
EVNTAPI
EtwEventWriteFull(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in USHORT EventProperty,
    __in_opt LPCGUID ActivityId,
    __in_opt LPCGUID RelatedActivityId,
    __in ULONG UserDataCount,
    __in_ecount_opt(UserDataCount) PEVENT_DATA_DESCRIPTOR UserData
    );
```

## <a name="parameters"></a><span data-ttu-id="9ec95-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ec95-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ec95-108">*RegHandle*</span><span class="sxs-lookup"><span data-stu-id="9ec95-108">*RegHandle*</span></span>
</dt> <dd>

<span data-ttu-id="9ec95-109">RegHandle para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="9ec95-109">RegHandle for the provider.</span></span>

</dd> <dt>

<span data-ttu-id="9ec95-110">*EventDescriptor*</span><span class="sxs-lookup"><span data-stu-id="9ec95-110">*EventDescriptor*</span></span> 
</dt> <dd>

<span data-ttu-id="9ec95-111">Descriptor de eventos del evento que se va a registrar.</span><span class="sxs-lookup"><span data-stu-id="9ec95-111">Event Descriptor of the event to log.</span></span>

</dd> <dt>

<span data-ttu-id="9ec95-112">*EventProperty*</span><span class="sxs-lookup"><span data-stu-id="9ec95-112">*EventProperty*</span></span>
</dt> <dd>

<span data-ttu-id="9ec95-113">Marca proporcionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="9ec95-113">Flag given by the user.</span></span>

</dd> <dt>

<span data-ttu-id="9ec95-114">*ActivityId*</span><span class="sxs-lookup"><span data-stu-id="9ec95-114">*ActivityId*</span></span>
</dt> <dd>

<span data-ttu-id="9ec95-115">ID. de actividad.</span><span class="sxs-lookup"><span data-stu-id="9ec95-115">Activity Id.</span></span>

</dd> <dt>

<span data-ttu-id="9ec95-116">*RelatedActivityId*</span><span class="sxs-lookup"><span data-stu-id="9ec95-116">*RelatedActivityId*</span></span>
</dt> <dd>

<span data-ttu-id="9ec95-117">Identificador de actividad relacionado.</span><span class="sxs-lookup"><span data-stu-id="9ec95-117">Related activity Id.</span></span>

</dd> <dt>

<span data-ttu-id="9ec95-118">*UserDataCount*</span><span class="sxs-lookup"><span data-stu-id="9ec95-118">*UserDataCount*</span></span>
</dt> <dd>

<span data-ttu-id="9ec95-119">El número de elementos de datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="9ec95-119">The number of user data items.</span></span>

</dd> <dt>

<span data-ttu-id="9ec95-120">*UserData*</span><span class="sxs-lookup"><span data-stu-id="9ec95-120">*UserData*</span></span>
</dt> <dd>

<span data-ttu-id="9ec95-121">Puntero a una matriz de elementos de datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="9ec95-121">Pointer to an array of user data items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ec95-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ec95-122">Return value</span></span>

<span data-ttu-id="9ec95-123">Código de error de Win32.</span><span class="sxs-lookup"><span data-stu-id="9ec95-123">A Win32 error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ec95-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ec95-124">Remarks</span></span>

<span data-ttu-id="9ec95-125">La función EtwEventWriteFull y las estructuras que devuelve son internas del sistema operativo y están sujetas a cambios de una versión de Windows a otra.</span><span class="sxs-lookup"><span data-stu-id="9ec95-125">The EtwEventWriteFull function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="9ec95-126">Para mantener la compatibilidad de la aplicación, es mejor usar funciones públicas en su lugar.</span><span class="sxs-lookup"><span data-stu-id="9ec95-126">To maintain the compatibility of your application, it is better to use public functions instead.</span></span>


## <a name="requirements"></a><span data-ttu-id="9ec95-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ec95-127">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9ec95-128">**Plataforma de destino**</span><span class="sxs-lookup"><span data-stu-id="9ec95-128">**Target Platform**</span></span> | <span data-ttu-id="9ec95-129">Windows</span><span class="sxs-lookup"><span data-stu-id="9ec95-129">Windows</span></span> |
| <span data-ttu-id="9ec95-130">**Header**</span><span class="sxs-lookup"><span data-stu-id="9ec95-130">**Header**</span></span> | <span data-ttu-id="9ec95-131">ntetw. h</span><span class="sxs-lookup"><span data-stu-id="9ec95-131">ntetw.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="9ec95-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ec95-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ec95-133">EventWrite</span><span class="sxs-lookup"><span data-stu-id="9ec95-133">EventWrite</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[<span data-ttu-id="9ec95-134">EventWriteEx</span><span class="sxs-lookup"><span data-stu-id="9ec95-134">EventWriteEx</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
