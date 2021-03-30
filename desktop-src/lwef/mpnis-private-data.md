---
title: MPNIS_PRIVATE_DATA estructura (MpClient. h)
description: Notificaciones NIS privadas.
ms.assetid: 19B4928F-BC78-4DEA-A563-1516B6454465
keywords:
- MPNIS_PRIVATE_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPNIS_PRIVATE_DATA características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPNIS_PRIVATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21340665a32b619c42d7909e8cd1b72ca6d09fb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801255"
---
# <a name="mpnis_private_data-structure"></a><span data-ttu-id="51e3e-105">MPNIS \_ \_ estructura de datos privada</span><span class="sxs-lookup"><span data-stu-id="51e3e-105">MPNIS\_PRIVATE\_DATA structure</span></span>

<span data-ttu-id="51e3e-106">Notificaciones NIS privadas.</span><span class="sxs-lookup"><span data-stu-id="51e3e-106">Private NIS notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="51e3e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51e3e-107">Syntax</span></span>


```C++
typedef struct tagMPNIS_PRIVATE_DATA {
  DWORD dwNotificationType;
  DWORD cbDataSize;
  BYTE  *pbData;
} MPNIS_PRIVATE_DATA, *PMPNIS_PRIVATE_DATA;
```



## <a name="members"></a><span data-ttu-id="51e3e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="51e3e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="51e3e-109">**dwNotificationType**</span><span class="sxs-lookup"><span data-stu-id="51e3e-109">**dwNotificationType**</span></span>
</dt> <dd>

<span data-ttu-id="51e3e-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="51e3e-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="51e3e-111">Tipo de notificación.</span><span class="sxs-lookup"><span data-stu-id="51e3e-111">Type of notification.</span></span>

</dd> <dt>

<span data-ttu-id="51e3e-112">**cbDataSize**</span><span class="sxs-lookup"><span data-stu-id="51e3e-112">**cbDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="51e3e-113">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="51e3e-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="51e3e-114">Tamaño de los datos reservados, en bytes.</span><span class="sxs-lookup"><span data-stu-id="51e3e-114">Size of reserved data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="51e3e-115">**pbData**</span><span class="sxs-lookup"><span data-stu-id="51e3e-115">**pbData**</span></span>
</dt> <dd>

<span data-ttu-id="51e3e-116">Tipo: **byte \***</span><span class="sxs-lookup"><span data-stu-id="51e3e-116">Type: **BYTE\***</span></span>

</dd> <dd>

<span data-ttu-id="51e3e-117">Puntero a los datos reservados.</span><span class="sxs-lookup"><span data-stu-id="51e3e-117">Pointer to reserved data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51e3e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51e3e-118">Requirements</span></span>



| <span data-ttu-id="51e3e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="51e3e-119">Requirement</span></span> | <span data-ttu-id="51e3e-120">Value</span><span class="sxs-lookup"><span data-stu-id="51e3e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51e3e-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51e3e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="51e3e-122">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="51e3e-122">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="51e3e-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51e3e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="51e3e-124">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="51e3e-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="51e3e-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51e3e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="51e3e-126"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="51e3e-126"><dt>MpClient.h</dt></span></span> </dl> |



 

 





