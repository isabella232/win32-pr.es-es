---
description: La estructura HANDOFFTABLE define los protocolos de una tabla de entrega.
ms.assetid: 6bb7465b-c1ba-4ffe-aecf-8125993c309a
title: Estructura HANDOFFTABLE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 842ef9fde56ff6b4c420034b861aa8c151e7e6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666271"
---
# <a name="handofftable-structure"></a><span data-ttu-id="0dbbe-103">Estructura HANDOFFTABLE</span><span class="sxs-lookup"><span data-stu-id="0dbbe-103">HANDOFFTABLE structure</span></span>

<span data-ttu-id="0dbbe-104">La estructura **HANDOFFTABLE** define los protocolos de una tabla de entrega.</span><span class="sxs-lookup"><span data-stu-id="0dbbe-104">The **HANDOFFTABLE** structure defines the protocols of a handoff table.</span></span>

<span data-ttu-id="0dbbe-105">Esta estructura se rellena mediante Monitor de red en función de la información del archivo. ini proporcionado por el usuario que se proporciona al llamar a la función [**CreateHandoffTable**](createhandofftable.md) .</span><span class="sxs-lookup"><span data-stu-id="0dbbe-105">This structure is filled in by Network Monitor based on information in a user supplied .ini file provided when calling the [**CreateHandoffTable**](createhandofftable.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dbbe-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0dbbe-106">Syntax</span></span>


```C++
typedef struct HANDOFFTABLE {
  DWORD          hot_sig;
  DWORD          hot_NumEntries;
  LPHANDOFFENTRY hot_Entries;
} HANDOFFTABLE, *LPHANDOFFTABLE;
```



## <a name="members"></a><span data-ttu-id="0dbbe-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0dbbe-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0dbbe-108">**\_SIG activo**</span><span class="sxs-lookup"><span data-stu-id="0dbbe-108">**hot\_sig**</span></span>
</dt> <dd>

<span data-ttu-id="0dbbe-109">Firma que identifica esta tabla como una tabla de entrega.</span><span class="sxs-lookup"><span data-stu-id="0dbbe-109">Signature that identifies this table as a handoff table.</span></span>

</dd> <dt>

<span data-ttu-id="0dbbe-110">**NumEntries en caliente \_**</span><span class="sxs-lookup"><span data-stu-id="0dbbe-110">**hot\_NumEntries**</span></span>
</dt> <dd>

<span data-ttu-id="0dbbe-111">Número de entradas que Monitor de red agregaron a la tabla de entrega.</span><span class="sxs-lookup"><span data-stu-id="0dbbe-111">Number of entries that Network Monitor added to the handoff table.</span></span>

</dd> <dt>

<span data-ttu-id="0dbbe-112">**\_entradas activas**</span><span class="sxs-lookup"><span data-stu-id="0dbbe-112">**hot\_Entries**</span></span>
</dt> <dd>

<span data-ttu-id="0dbbe-113">Tabla de entrega.</span><span class="sxs-lookup"><span data-stu-id="0dbbe-113">Handoff table.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0dbbe-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0dbbe-114">Remarks</span></span>

<span data-ttu-id="0dbbe-115">Esta estructura y sus estructuras HANDOFFENTRY asociadas se rellenan mediante Monitor de red cuando Monitor de red crea una tabla de entrega.</span><span class="sxs-lookup"><span data-stu-id="0dbbe-115">This structure, and its associated HANDOFFENTRY structures, are filled in by Network Monitor when Network Monitor creates a handoff table.</span></span>

<span data-ttu-id="0dbbe-116">La información del protocolo que se usa al crear una tabla de entrega se proporciona en un archivo. ini proporcionado por la aplicación cuando se llama a [**CreateHandoffTable**](createhandofftable.md) .</span><span class="sxs-lookup"><span data-stu-id="0dbbe-116">The protocol information that is used when creating a handoff table is provided in an .ini file supplied by the application when [**CreateHandoffTable**](createhandofftable.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dbbe-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0dbbe-117">Requirements</span></span>



| <span data-ttu-id="0dbbe-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dbbe-118">Requirement</span></span> | <span data-ttu-id="0dbbe-119">Value</span><span class="sxs-lookup"><span data-stu-id="0dbbe-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0dbbe-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0dbbe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0dbbe-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0dbbe-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0dbbe-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0dbbe-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0dbbe-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0dbbe-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0dbbe-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0dbbe-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0dbbe-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0dbbe-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dbbe-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="0dbbe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dbbe-127">HANDOFFENTRY</span><span class="sxs-lookup"><span data-stu-id="0dbbe-127">HANDOFFENTRY</span></span>](handoffentry.md)
</dt> <dt>

[<span data-ttu-id="0dbbe-128">CreateHandoffTable</span><span class="sxs-lookup"><span data-stu-id="0dbbe-128">CreateHandoffTable</span></span>](createhandofftable.md)
</dt> </dl>

 

 




