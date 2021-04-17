---
description: Representa información sobre los destinos de llamada para la protección de flujo de control (CFG).
ms.assetid: 8DEF907F-3F23-4122-95CE-F413FC7FD96B
title: CFG_CALL_TARGET_INFO estructura (Ntmmapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFG_CALL_TARGET_INFO
api_type:
- HeaderDef
api_location:
- ntmmapi.h
ms.openlocfilehash: 66177f6b478264a10c1ce0e50297d943a16407c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677779"
---
# <a name="cfg_call_target_info-structure"></a><span data-ttu-id="d5ff6-103">\_Estructura de \_ información de destino de llamada cfg \_</span><span class="sxs-lookup"><span data-stu-id="d5ff6-103">CFG\_CALL\_TARGET\_INFO structure</span></span>

<span data-ttu-id="d5ff6-104">Representa información sobre los destinos de llamada para la protección de flujo de control (CFG).</span><span class="sxs-lookup"><span data-stu-id="d5ff6-104">Represents information about call targets for Control Flow Guard (CFG).</span></span>

## <a name="syntax"></a><span data-ttu-id="d5ff6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5ff6-105">Syntax</span></span>


```C++
typedef struct _CFG_CALL_TARGET_INFO {
  ULONG_PTR Offset;
  ULONG_PTR Flags;
} CFG_CALL_TARGET_INFO, *PCFG_CALL_TARGET_INFO;
```



## <a name="members"></a><span data-ttu-id="d5ff6-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d5ff6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d5ff6-107">**Offset**</span><span class="sxs-lookup"><span data-stu-id="d5ff6-107">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="d5ff6-108">Desplazamiento relativo a una dirección virtual (Inicio) proporcionada.</span><span class="sxs-lookup"><span data-stu-id="d5ff6-108">Offset relative to a provided (start) virtual address.</span></span> <span data-ttu-id="d5ff6-109">Este desplazamiento debe estar alineado con 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="d5ff6-109">This offset should be 16 byte aligned.</span></span>

</dd> <dt>

<span data-ttu-id="d5ff6-110">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="d5ff6-110">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="d5ff6-111">Marcas que describen la operación que se va a realizar en la dirección.</span><span class="sxs-lookup"><span data-stu-id="d5ff6-111">Flags describing the operation to be performed on the address.</span></span> <span data-ttu-id="d5ff6-112">Si se establece el destino de la **\_ llamada cfg \_ \_ válido** , la dirección se marcará como válida para cfg.</span><span class="sxs-lookup"><span data-stu-id="d5ff6-112">If **CFG\_CALL\_TARGET\_VALID** is set, then the address will be marked valid for CFG.</span></span> <span data-ttu-id="d5ff6-113">De lo contrario, se marcará como destino de llamada no válido.</span><span class="sxs-lookup"><span data-stu-id="d5ff6-113">Otherwise, it will be marked an invalid call target.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5ff6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5ff6-114">Requirements</span></span>



| <span data-ttu-id="d5ff6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5ff6-115">Requirement</span></span> | <span data-ttu-id="d5ff6-116">Value</span><span class="sxs-lookup"><span data-stu-id="d5ff6-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d5ff6-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5ff6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d5ff6-118">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5ff6-118">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d5ff6-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5ff6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d5ff6-120">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5ff6-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d5ff6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5ff6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5ff6-122"><dt>Ntmmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5ff6-122"><dt>Ntmmapi.h</dt></span></span> </dl> |



 

 




