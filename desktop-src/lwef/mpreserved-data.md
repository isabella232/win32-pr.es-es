---
title: MPRESERVED_DATA estructura (MpClient. h)
description: Datos de notificación reservados.
ms.assetid: C92206BD-6E56-4B7D-ABB1-DC1149AE141D
keywords:
- MPRESERVED_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPRESERVED_DATA características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPRESERVED_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b1e08184da71fe857cb412ef986c986a0c59baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150575"
---
# <a name="mpreserved_data-structure"></a><span data-ttu-id="03d91-105">\_Estructura de datos MPRESERVED</span><span class="sxs-lookup"><span data-stu-id="03d91-105">MPRESERVED\_DATA structure</span></span>

<span data-ttu-id="03d91-106">Datos de notificación reservados.</span><span class="sxs-lookup"><span data-stu-id="03d91-106">Reserved notification data.</span></span>

## <a name="syntax"></a><span data-ttu-id="03d91-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03d91-107">Syntax</span></span>


```C++
typedef struct tagMPRESERVED_DATA {
  DWORD cbReservedData;
  BYTE  *pbReservedData;
} MPRESERVED_DATA, *PMPRESERVED_DATA;
```



## <a name="members"></a><span data-ttu-id="03d91-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="03d91-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="03d91-109">**cbReservedData**</span><span class="sxs-lookup"><span data-stu-id="03d91-109">**cbReservedData**</span></span>
</dt> <dd>

<span data-ttu-id="03d91-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="03d91-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="03d91-111">Tamaño de los datos reservados, en bytes.</span><span class="sxs-lookup"><span data-stu-id="03d91-111">Size of reserved data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="03d91-112">**pbReservedData**</span><span class="sxs-lookup"><span data-stu-id="03d91-112">**pbReservedData**</span></span>
</dt> <dd>

<span data-ttu-id="03d91-113">Tipo: **byte \***</span><span class="sxs-lookup"><span data-stu-id="03d91-113">Type: **BYTE\***</span></span>

</dd> <dd>

<span data-ttu-id="03d91-114">Puntero a los datos reservados.</span><span class="sxs-lookup"><span data-stu-id="03d91-114">Pointer to reserved data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03d91-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03d91-115">Requirements</span></span>



| <span data-ttu-id="03d91-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="03d91-116">Requirement</span></span> | <span data-ttu-id="03d91-117">Value</span><span class="sxs-lookup"><span data-stu-id="03d91-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03d91-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03d91-118">Minimum supported client</span></span><br/> | <span data-ttu-id="03d91-119">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="03d91-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="03d91-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03d91-120">Minimum supported server</span></span><br/> | <span data-ttu-id="03d91-121">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="03d91-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="03d91-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03d91-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="03d91-123"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="03d91-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





