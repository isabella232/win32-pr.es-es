---
title: MPTHREAT_INFOEX_NIS estructura (MpClient. h)
description: Contiene información específica de NIS.
ms.assetid: 3887C5BF-B1F6-4420-B40A-9585E44BE7A9
keywords:
- MPTHREAT_INFOEX_NIS estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPTHREAT_INFOEX_NIS características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_NIS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b4ed68432a2d0ebe78535a139fcc7b0882b9ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079320"
---
# <a name="mpthreat_infoex_nis-structure"></a><span data-ttu-id="16993-105">MPTHREAT \_ INFOEX ( \_ estructura de NIS)</span><span class="sxs-lookup"><span data-stu-id="16993-105">MPTHREAT\_INFOEX\_NIS structure</span></span>

<span data-ttu-id="16993-106">Contiene información específica de NIS.</span><span class="sxs-lookup"><span data-stu-id="16993-106">Contains NIS-specific information.</span></span>

## <a name="syntax"></a><span data-ttu-id="16993-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16993-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFOEX_NIS {
  MP_MIDL_STRING LPWSTR SourceIP;
  MP_MIDL_STRING LPWSTR DestinationIP;
  DWORD                 dwSourceport;
  DWORD                 dwDestinationport;
  MP_MIDL_STRING LPWSTR Protocol;
  MP_MIDL_STRING LPWSTR Link;
} MPTHREAT_INFOEX_NIS, *PMPTHREAT_INFOEX_NIS;
```



## <a name="members"></a><span data-ttu-id="16993-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="16993-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="16993-109">**SourceIP**</span><span class="sxs-lookup"><span data-stu-id="16993-109">**SourceIP**</span></span>
</dt> <dd>

<span data-ttu-id="16993-110">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="16993-110">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="16993-111">**DestinationIP**</span><span class="sxs-lookup"><span data-stu-id="16993-111">**DestinationIP**</span></span>
</dt> <dd>

<span data-ttu-id="16993-112">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="16993-112">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="16993-113">**dwSourceport**</span><span class="sxs-lookup"><span data-stu-id="16993-113">**dwSourceport**</span></span>
</dt> <dd>

<span data-ttu-id="16993-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="16993-114">Type: **DWORD**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="16993-115">**dwDestinationport**</span><span class="sxs-lookup"><span data-stu-id="16993-115">**dwDestinationport**</span></span>
</dt> <dd>

<span data-ttu-id="16993-116">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="16993-116">Type: **DWORD**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="16993-117">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="16993-117">**Protocol**</span></span>
</dt> <dd>

<span data-ttu-id="16993-118">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="16993-118">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="16993-119">**Vínculo**</span><span class="sxs-lookup"><span data-stu-id="16993-119">**Link**</span></span>
</dt> <dd>

<span data-ttu-id="16993-120">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="16993-120">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

<span data-ttu-id="16993-121"></dd> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="16993-121"></dd> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="16993-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16993-122">Requirements</span></span>



| <span data-ttu-id="16993-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="16993-123">Requirement</span></span> | <span data-ttu-id="16993-124">Value</span><span class="sxs-lookup"><span data-stu-id="16993-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16993-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16993-125">Minimum supported client</span></span><br/> | <span data-ttu-id="16993-126">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="16993-126">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="16993-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16993-127">Minimum supported server</span></span><br/> | <span data-ttu-id="16993-128">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="16993-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="16993-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16993-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="16993-130"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="16993-130"><dt>MpClient.h</dt></span></span> </dl> |



 

 





