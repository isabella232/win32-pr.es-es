---
title: Estructura WMDMDATETIME
description: La estructura WMDMDATETIME contiene una fecha y hora del día.
ms.assetid: 47f3994d-66c6-47e4-803d-0c98c70eccc8
keywords:
- Estructura WMDMDATETIME Administrador de dispositivos Windows Media
- Puntero de estructura PWMDMDATETIME Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- WMDMDATETIME
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07acf706aa63a21edd27fb2ac206db3039249055
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698558"
---
# <a name="wmdmdatetime-structure"></a><span data-ttu-id="b21c4-105">Estructura WMDMDATETIME</span><span class="sxs-lookup"><span data-stu-id="b21c4-105">WMDMDATETIME structure</span></span>

<span data-ttu-id="b21c4-106">La estructura **WMDMDATETIME** contiene una fecha y hora del día.</span><span class="sxs-lookup"><span data-stu-id="b21c4-106">The **WMDMDATETIME** structure contains a date and time of day.</span></span>

## <a name="syntax"></a><span data-ttu-id="b21c4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b21c4-107">Syntax</span></span>


```C++
typedef struct _WMDMDATETIME {
  WORD wYear;
  WORD wMonth;
  WORD wDay;
  WORD wHour;
  WORD wMinute;
  WORD wSecond;
} WMDMDATETIME, *PWMDMDATETIME;
```



## <a name="members"></a><span data-ttu-id="b21c4-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b21c4-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b21c4-109">**wYear**</span><span class="sxs-lookup"><span data-stu-id="b21c4-109">**wYear**</span></span>
</dt> <dd>

<span data-ttu-id="b21c4-110">Palabra que contiene el año de cuatro dígitos.</span><span class="sxs-lookup"><span data-stu-id="b21c4-110">Word containing the four-digit year.</span></span>

</dd> <dt>

<span data-ttu-id="b21c4-111">**wMonth**</span><span class="sxs-lookup"><span data-stu-id="b21c4-111">**wMonth**</span></span>
</dt> <dd>

<span data-ttu-id="b21c4-112">Palabra que contiene el mes (1-12).</span><span class="sxs-lookup"><span data-stu-id="b21c4-112">Word containing the month (1-12).</span></span>

</dd> <dt>

<span data-ttu-id="b21c4-113">**wDay**</span><span class="sxs-lookup"><span data-stu-id="b21c4-113">**wDay**</span></span>
</dt> <dd>

<span data-ttu-id="b21c4-114">Palabra que contiene el día del mes (1-31).</span><span class="sxs-lookup"><span data-stu-id="b21c4-114">Word containing the day of the month (1-31).</span></span>

</dd> <dt>

<span data-ttu-id="b21c4-115">**wHour**</span><span class="sxs-lookup"><span data-stu-id="b21c4-115">**wHour**</span></span>
</dt> <dd>

<span data-ttu-id="b21c4-116">Palabra que contiene la hora (0-23).</span><span class="sxs-lookup"><span data-stu-id="b21c4-116">Word containing the hour (0-23).</span></span>

</dd> <dt>

<span data-ttu-id="b21c4-117">**wMinute**</span><span class="sxs-lookup"><span data-stu-id="b21c4-117">**wMinute**</span></span>
</dt> <dd>

<span data-ttu-id="b21c4-118">Palabra que contiene el minuto (0-59).</span><span class="sxs-lookup"><span data-stu-id="b21c4-118">Word containing the minute (0-59).</span></span>

</dd> <dt>

<span data-ttu-id="b21c4-119">**wSecond**</span><span class="sxs-lookup"><span data-stu-id="b21c4-119">**wSecond**</span></span>
</dt> <dd>

<span data-ttu-id="b21c4-120">Palabra que contiene el segundo (0-59).</span><span class="sxs-lookup"><span data-stu-id="b21c4-120">Word containing the second (0-59).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b21c4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b21c4-121">Requirements</span></span>



| <span data-ttu-id="b21c4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b21c4-122">Requirement</span></span> | <span data-ttu-id="b21c4-123">Value</span><span class="sxs-lookup"><span data-stu-id="b21c4-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b21c4-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b21c4-124">Header</span></span><br/> | <dl> <span data-ttu-id="b21c4-125"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b21c4-125"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b21c4-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b21c4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b21c4-127">**IMDSPStorage:: GetDate**</span><span class="sxs-lookup"><span data-stu-id="b21c4-127">**IMDSPStorage::GetDate**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getdate)
</dt> <dt>

[<span data-ttu-id="b21c4-128">**IWMDMStorage:: GetDate**</span><span class="sxs-lookup"><span data-stu-id="b21c4-128">**IWMDMStorage::GetDate**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getdate)
</dt> <dt>

[<span data-ttu-id="b21c4-129">**WMDMRIGHTS**</span><span class="sxs-lookup"><span data-stu-id="b21c4-129">**WMDMRIGHTS**</span></span>](wmdmrights.md)
</dt> <dt>

[<span data-ttu-id="b21c4-130">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="b21c4-130">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





