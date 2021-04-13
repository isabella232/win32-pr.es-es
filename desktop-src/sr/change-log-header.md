---
title: Estructura de CHANGE_LOG_HEADER
description: Encabezado del registro de cambios.
ms.assetid: 24fee9a5-b073-474f-afd5-d81f66399936
keywords:
- Restaurar sistema de estructura CHANGE_LOG_HEADER
- PCHANGE_LOG_HEADER de puntero de estructura para restaurar sistema
topic_type:
- apiref
api_name:
- CHANGE_LOG_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5512ff9c9e708095f38e3ae1dcf80ce2e0e4443b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421981"
---
# <a name="change_log_header-structure"></a><span data-ttu-id="642b2-105">CAMBIAR \_ la \_ estructura del encabezado del registro</span><span class="sxs-lookup"><span data-stu-id="642b2-105">CHANGE\_LOG\_HEADER structure</span></span>

<span data-ttu-id="642b2-106">\[Esta información solo se aplica a Windows XP con Service Pack 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="642b2-106">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="642b2-107">Encabezado del registro de cambios.</span><span class="sxs-lookup"><span data-stu-id="642b2-107">The change log header.</span></span>

## <a name="syntax"></a><span data-ttu-id="642b2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="642b2-108">Syntax</span></span>


```C++
typedef struct _CHANGE_LOG_HEADER {
  RECORD_HEADER RecordHeader;
  DWORD         dwMagicNum;
  DWORD         dwLogVersion;
  RECORD_HEADER DataHeader;
  BYTE          byteData[1];
} CHANGE_LOG_HEADER, *PCHANGE_LOG_HEADER;
```



## <a name="members"></a><span data-ttu-id="642b2-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="642b2-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="642b2-110">**RecordHeader**</span><span class="sxs-lookup"><span data-stu-id="642b2-110">**RecordHeader**</span></span>
</dt> <dd>

<span data-ttu-id="642b2-111">Una estructura de [**\_ encabezado de registro**](record-header.md) .</span><span class="sxs-lookup"><span data-stu-id="642b2-111">A [**RECORD\_HEADER**](record-header.md) structure.</span></span> <span data-ttu-id="642b2-112">El miembro **dwRecordType** debe establecerse en RecordTypeLogHeader (0).</span><span class="sxs-lookup"><span data-stu-id="642b2-112">The **dwRecordType** member should be set to RecordTypeLogHeader (0).</span></span> <span data-ttu-id="642b2-113">El miembro **dwRecordSize** debe tener en cuenta todos los miembros, más el valor **DWORD** adicional que sigue a este encabezado.</span><span class="sxs-lookup"><span data-stu-id="642b2-113">The **dwRecordSize** member should account for all the members, plus the extra **DWORD** value that follows this header.</span></span> <span data-ttu-id="642b2-114">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="642b2-114">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="642b2-115">**dwMagicNum**</span><span class="sxs-lookup"><span data-stu-id="642b2-115">**dwMagicNum**</span></span>
</dt> <dd>

<span data-ttu-id="642b2-116">Este miembro debe establecerse en 0xabcdef12.</span><span class="sxs-lookup"><span data-stu-id="642b2-116">This member should be set to 0xabcdef12.</span></span>

</dd> <dt>

<span data-ttu-id="642b2-117">**dwLogVersion**</span><span class="sxs-lookup"><span data-stu-id="642b2-117">**dwLogVersion**</span></span>
</dt> <dd>

<span data-ttu-id="642b2-118">Este miembro debe establecerse en 2.</span><span class="sxs-lookup"><span data-stu-id="642b2-118">This member should be set to 2.</span></span>

</dd> <dt>

<span data-ttu-id="642b2-119">**MyHeader**</span><span class="sxs-lookup"><span data-stu-id="642b2-119">**DataHeader**</span></span>
</dt> <dd>

<span data-ttu-id="642b2-120">Una estructura de [**\_ encabezado de registro**](record-header.md) .</span><span class="sxs-lookup"><span data-stu-id="642b2-120">A [**RECORD\_HEADER**](record-header.md) structure.</span></span> <span data-ttu-id="642b2-121">El miembro **dwRecordType** debe establecerse en **RecordTypeVolumePath** (2).</span><span class="sxs-lookup"><span data-stu-id="642b2-121">The **dwRecordType** member should be set to **RecordTypeVolumePath** (2).</span></span>

</dd> <dt>

<span data-ttu-id="642b2-122">**byteData**</span><span class="sxs-lookup"><span data-stu-id="642b2-122">**byteData**</span></span>
</dt> <dd>

<span data-ttu-id="642b2-123">Inicio de una cadena terminada en null que especifica la ruta de acceso del volumen.</span><span class="sxs-lookup"><span data-stu-id="642b2-123">The start of a null-terminated string that specifies the volume path.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="642b2-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="642b2-124">Remarks</span></span>

<span data-ttu-id="642b2-125">Este encabezado va seguido de un valor **DWORD** que debe ser idéntico al valor del miembro **dwRecordSize** de **RecordHeader**.</span><span class="sxs-lookup"><span data-stu-id="642b2-125">This header is followed by a **DWORD** value that should be identical to the value of the **dwRecordSize** member of **RecordHeader**.</span></span>

## <a name="requirements"></a><span data-ttu-id="642b2-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="642b2-126">Requirements</span></span>



| <span data-ttu-id="642b2-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="642b2-127">Requirement</span></span> | <span data-ttu-id="642b2-128">Value</span><span class="sxs-lookup"><span data-stu-id="642b2-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="642b2-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="642b2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="642b2-130">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="642b2-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="642b2-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="642b2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="642b2-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="642b2-132">None supported</span></span><br/>                            |
| <span data-ttu-id="642b2-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="642b2-133">End of client support</span></span><br/>    | <span data-ttu-id="642b2-134">Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="642b2-134">Windows XP with SP2</span></span><br/>                       |



 

 





