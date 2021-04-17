---
title: MPHEALTH_DATA estructura (MpClient. h)
description: Datos de notificación de estado.
ms.assetid: 37A87F77-386A-4508-B338-ED2151518968
keywords:
- MPHEALTH_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPHEALTH_DATA características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPHEALTH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e729bdea82b6a885b64e95ecd77f9deae6bff4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705183"
---
# <a name="mphealth_data-structure"></a><span data-ttu-id="048cf-105">\_Estructura de datos MPHEALTH</span><span class="sxs-lookup"><span data-stu-id="048cf-105">MPHEALTH\_DATA structure</span></span>

<span data-ttu-id="048cf-106">Datos de notificación de estado.</span><span class="sxs-lookup"><span data-stu-id="048cf-106">Health notification data.</span></span>

## <a name="syntax"></a><span data-ttu-id="048cf-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="048cf-107">Syntax</span></span>


```C++
typedef struct tagMPHEALTH_DATA {
  DWORD dwNotificationType;
  DWORD dwNotificationFlag;
} MPHEALTH_DATA, *PMPHEALTH_DATA;
```



## <a name="members"></a><span data-ttu-id="048cf-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="048cf-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="048cf-109">**dwNotificationType**</span><span class="sxs-lookup"><span data-stu-id="048cf-109">**dwNotificationType**</span></span>
</dt> <dd>

<span data-ttu-id="048cf-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="048cf-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="048cf-111">Tipo de notificación.</span><span class="sxs-lookup"><span data-stu-id="048cf-111">Type of notification.</span></span>

</dd> <dt>

<span data-ttu-id="048cf-112">**dwNotificationFlag**</span><span class="sxs-lookup"><span data-stu-id="048cf-112">**dwNotificationFlag**</span></span>
</dt> <dd>

<span data-ttu-id="048cf-113">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="048cf-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="048cf-114">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="048cf-114">Unused.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="048cf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="048cf-115">Requirements</span></span>



| <span data-ttu-id="048cf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="048cf-116">Requirement</span></span> | <span data-ttu-id="048cf-117">Value</span><span class="sxs-lookup"><span data-stu-id="048cf-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="048cf-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="048cf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="048cf-119">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="048cf-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="048cf-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="048cf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="048cf-121">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="048cf-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="048cf-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="048cf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="048cf-123"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="048cf-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





