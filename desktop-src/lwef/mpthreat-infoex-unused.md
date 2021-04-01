---
title: MPTHREAT_INFOEX_UNUSED estructura (MpClient. h)
description: Estructura ficticia para amenazas de tipo de modificación sin comportamiento.
ms.assetid: 3C5305CD-D533-47B5-ADD3-BD8DA05F2046
keywords:
- MPTHREAT_INFOEX_UNUSED estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPTHREAT_INFOEX_UNUSED características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_UNUSED
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fed78d904bd03fee17676dced7c828aaea8d319d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150571"
---
# <a name="mpthreat_infoex_unused-structure"></a><span data-ttu-id="30ec0-105">MPTHREAT \_ INFOEX de la \_ estructura no usada</span><span class="sxs-lookup"><span data-stu-id="30ec0-105">MPTHREAT\_INFOEX\_UNUSED structure</span></span>

<span data-ttu-id="30ec0-106">Estructura ficticia para amenazas de tipo de modificación sin comportamiento.</span><span class="sxs-lookup"><span data-stu-id="30ec0-106">Dummy structure for non-behavior modification type threats.</span></span>

## <a name="syntax"></a><span data-ttu-id="30ec0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30ec0-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFOEX_UNUSED {
  DWORD dwNone;
} MPTHREAT_INFOEX_UNUSED, *PMPTHREAT_INFOEX_UNUSED;
```



## <a name="members"></a><span data-ttu-id="30ec0-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="30ec0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="30ec0-109">**dwNone**</span><span class="sxs-lookup"><span data-stu-id="30ec0-109">**dwNone**</span></span>
</dt> <dd>

<span data-ttu-id="30ec0-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="30ec0-110">Type: **DWORD**</span></span>

<span data-ttu-id="30ec0-111"></dd> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="30ec0-111"></dd> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="30ec0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30ec0-112">Requirements</span></span>



| <span data-ttu-id="30ec0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="30ec0-113">Requirement</span></span> | <span data-ttu-id="30ec0-114">Value</span><span class="sxs-lookup"><span data-stu-id="30ec0-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30ec0-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30ec0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="30ec0-116">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="30ec0-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="30ec0-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30ec0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="30ec0-118">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="30ec0-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="30ec0-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30ec0-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="30ec0-120"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="30ec0-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





