---
description: La estructura HANDOFFENTRY define una entrada de protocolo específica en una estructura HANDOFFTABLE.
ms.assetid: 85793326-3007-4dd9-9325-3447d6e09883
title: Estructura HANDOFFENTRY (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7c04c7bc90fdd0f36beb6aed26a6b84c077eff5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540195"
---
# <a name="handoffentry-structure"></a><span data-ttu-id="7d05f-103">Estructura HANDOFFENTRY</span><span class="sxs-lookup"><span data-stu-id="7d05f-103">HANDOFFENTRY structure</span></span>

<span data-ttu-id="7d05f-104">La estructura **HANDOFFENTRY** define una entrada de protocolo específica en una estructura **HANDOFFTABLE** .</span><span class="sxs-lookup"><span data-stu-id="7d05f-104">The **HANDOFFENTRY** structure defines a specific protocol entry in a **HANDOFFTABLE** structure.</span></span>

<span data-ttu-id="7d05f-105">Esta estructura se rellena mediante Monitor de red en función de la información del archivo. ini proporcionado por el usuario que se proporciona al llamar a la función [**CreateHandoffTable**](createhandofftable.md) .</span><span class="sxs-lookup"><span data-stu-id="7d05f-105">This structure is filled in by Network Monitor based on information in a user supplied .ini file provided when calling the [**CreateHandoffTable**](createhandofftable.md) function.</span></span> <span data-ttu-id="7d05f-106">Una aplicación nunca debe modificar explícitamente esta estructura.</span><span class="sxs-lookup"><span data-stu-id="7d05f-106">This structure should never be explicitly modified by an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d05f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d05f-107">Syntax</span></span>


```C++
typedef struct _SESSIONSTATS {
  DWORD      hoe_sig;
  DWORD      hoe_ProtIdentNumber;
  HPPROTOCOL hoe_ProtocolHandle;
  DWORD      hoe_ProtocolData;
} HANDOFFENTRY, *LPHANDOFFENTRY;
```



## <a name="members"></a><span data-ttu-id="7d05f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7d05f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7d05f-109">**Cómo \_ SIG**</span><span class="sxs-lookup"><span data-stu-id="7d05f-109">**hoe\_sig**</span></span>
</dt> <dd>

<span data-ttu-id="7d05f-110">Firma que identifica esta entrada como una entrada de la tabla de entrega.</span><span class="sxs-lookup"><span data-stu-id="7d05f-110">Signature that identifies this entry as a handoff table entry.</span></span>

</dd> <dt>

<span data-ttu-id="7d05f-111">**Cómo \_ ProtIdentNumber**</span><span class="sxs-lookup"><span data-stu-id="7d05f-111">**hoe\_ProtIdentNumber**</span></span>
</dt> <dd>

<span data-ttu-id="7d05f-112">Número de protocolo proporcionado por el archivo. ini proporcionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="7d05f-112">Protocol number provided by user supplied .ini file.</span></span>

</dd> <dt>

<span data-ttu-id="7d05f-113">**Cómo \_ ProtocolHandle**</span><span class="sxs-lookup"><span data-stu-id="7d05f-113">**hoe\_ProtocolHandle**</span></span>
</dt> <dd>

<span data-ttu-id="7d05f-114">Identificador del protocolo creado con el nombre de protocolo proporcionado por el archivo. ini proporcionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="7d05f-114">Handle of protocol created using the protocol name provided by user supplied .ini file.</span></span>

</dd> <dt>

<span data-ttu-id="7d05f-115">**Cómo \_ ProtocolData**</span><span class="sxs-lookup"><span data-stu-id="7d05f-115">**hoe\_ProtocolData**</span></span>
</dt> <dd>

<span data-ttu-id="7d05f-116">Datos de instancia de protocolo proporcionados por el archivo. ini proporcionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="7d05f-116">Protocol instance data provided by user supplied .ini file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d05f-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d05f-117">Remarks</span></span>

<span data-ttu-id="7d05f-118">Esta estructura se rellena por Monitor de red cuando Monitor de red crea una tabla de entrega.</span><span class="sxs-lookup"><span data-stu-id="7d05f-118">This structure is filled in by Network Monitor when Network Monitor creates a handoff table.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d05f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d05f-119">Requirements</span></span>



| <span data-ttu-id="7d05f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d05f-120">Requirement</span></span> | <span data-ttu-id="7d05f-121">Value</span><span class="sxs-lookup"><span data-stu-id="7d05f-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7d05f-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d05f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7d05f-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7d05f-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7d05f-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d05f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7d05f-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7d05f-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7d05f-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7d05f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d05f-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d05f-127"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d05f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d05f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d05f-129">HANDOFFTABLE</span><span class="sxs-lookup"><span data-stu-id="7d05f-129">HANDOFFTABLE</span></span>](handofftable.md)
</dt> </dl>

 

 




