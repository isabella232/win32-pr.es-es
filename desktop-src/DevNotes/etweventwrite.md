---
description: 'Más información acerca de: EtwEventWrite (función)'
title: EtwEventWrite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWrite
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: 149f611dfb298749befca805509e05fa2dec497a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080244"
---
# <a name="etweventwrite-function"></a><span data-ttu-id="0a217-103">EtwEventWrite función)</span><span class="sxs-lookup"><span data-stu-id="0a217-103">EtwEventWrite function</span></span>

<span data-ttu-id="0a217-104">[La función EtwEventWrite y las estructuras que devuelve son internas del sistema operativo y están sujetas a cambios de una versión de Windows a otra.]</span><span class="sxs-lookup"><span data-stu-id="0a217-104">[The EtwEventWrite function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.]</span></span>

<span data-ttu-id="0a217-105">Escribe un evento básico en una sesión.</span><span class="sxs-lookup"><span data-stu-id="0a217-105">Writes a basic event to a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a217-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a217-106">Syntax</span></span>

```C++
ULONG 
EVNTAPI
EtwEventWrite(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in ULONG UserDataCount,
    __in_ecount_opt(UserDataCount) PEVENT_DATA_DESCRIPTOR UserData
    );
```

## <a name="parameters"></a><span data-ttu-id="0a217-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a217-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a217-108">*RegHandle*</span><span class="sxs-lookup"><span data-stu-id="0a217-108">*RegHandle*</span></span>
</dt> <dd>

<span data-ttu-id="0a217-109">RegHandle para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="0a217-109">RegHandle for the provider.</span></span>

</dd> <dt>

<span data-ttu-id="0a217-110">*EventDescriptor*</span><span class="sxs-lookup"><span data-stu-id="0a217-110">*EventDescriptor*</span></span>
</dt> <dd>

<span data-ttu-id="0a217-111">Descriptor de eventos del evento que se va a registrar.</span><span class="sxs-lookup"><span data-stu-id="0a217-111">Event descriptor of the event to log.</span></span>

</dd> <dt>

<span data-ttu-id="0a217-112">*UserDataCount*</span><span class="sxs-lookup"><span data-stu-id="0a217-112">*UserDataCount*</span></span>
</dt> <dd>

<span data-ttu-id="0a217-113">Número de elementos de datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="0a217-113">Number of user data items.</span></span>

</dd> <dt>

<span data-ttu-id="0a217-114">*UserData*</span><span class="sxs-lookup"><span data-stu-id="0a217-114">*UserData*</span></span>
</dt> <dd>

<span data-ttu-id="0a217-115">Puntero a una matriz de elementos de datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="0a217-115">Pointer to an array of user data items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a217-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a217-116">Return value</span></span>

<span data-ttu-id="0a217-117">Código de error de Win32.</span><span class="sxs-lookup"><span data-stu-id="0a217-117">A Win32 error code.</span></span>


## <a name="remarks"></a><span data-ttu-id="0a217-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a217-118">Remarks</span></span>

<span data-ttu-id="0a217-119">La función EtwEventWrite y las estructuras que devuelve son internas del sistema operativo y están sujetas a cambios de una versión de Windows a otra.</span><span class="sxs-lookup"><span data-stu-id="0a217-119">The EtwEventWrite function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="0a217-120">Para mantener la compatibilidad de la aplicación, es mejor usar funciones públicas en su lugar.</span><span class="sxs-lookup"><span data-stu-id="0a217-120">To maintain the compatibility of your application, it is better to use public functions instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a217-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a217-121">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="0a217-122">**Plataforma de destino**</span><span class="sxs-lookup"><span data-stu-id="0a217-122">**Target Platform**</span></span> | <span data-ttu-id="0a217-123">Windows</span><span class="sxs-lookup"><span data-stu-id="0a217-123">Windows</span></span> |
| <span data-ttu-id="0a217-124">**Header**</span><span class="sxs-lookup"><span data-stu-id="0a217-124">**Header**</span></span> | <span data-ttu-id="0a217-125">ntetw. h</span><span class="sxs-lookup"><span data-stu-id="0a217-125">ntetw.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="0a217-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a217-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a217-127">EventWrite</span><span class="sxs-lookup"><span data-stu-id="0a217-127">EventWrite</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[<span data-ttu-id="0a217-128">EventWriteEx</span><span class="sxs-lookup"><span data-stu-id="0a217-128">EventWriteEx</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
