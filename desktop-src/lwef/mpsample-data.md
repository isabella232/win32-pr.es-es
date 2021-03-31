---
title: MPSAMPLE_DATA estructura (MpClient. h)
description: Datos de notificación pasados a la función de devolución de llamada de envío de ejemplo.
ms.assetid: 58F348C6-411D-4545-9D4D-A80095FD139B
keywords:
- MPSAMPLE_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPSAMPLE_DATA características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPSAMPLE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24a894638465c0362069b8fdcbacddf98bfdd2c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151158"
---
# <a name="mpsample_data-structure"></a><span data-ttu-id="3e7aa-105">\_Estructura de datos MPSAMPLE</span><span class="sxs-lookup"><span data-stu-id="3e7aa-105">MPSAMPLE\_DATA structure</span></span>

<span data-ttu-id="3e7aa-106">Datos de notificación pasados a la función de devolución de llamada de envío de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-106">Notification data passed to the sample submission callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e7aa-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e7aa-107">Syntax</span></span>


```C++
typedef struct tagMPSAMPLE_DATA {
  DWORD dwSampleIndex;
} MPSAMPLE_DATA, *PMPSAMPLE_DATA;
```



## <a name="members"></a><span data-ttu-id="3e7aa-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="3e7aa-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3e7aa-109">**dwSampleIndex**</span><span class="sxs-lookup"><span data-stu-id="3e7aa-109">**dwSampleIndex**</span></span>
</dt> <dd>

<span data-ttu-id="3e7aa-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3e7aa-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3e7aa-111">Índice del elemento de ejemplo para el que se registra el estado del envío.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-111">Index of the sample item for which the submission status is reported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e7aa-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e7aa-112">Requirements</span></span>



| <span data-ttu-id="3e7aa-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e7aa-113">Requirement</span></span> | <span data-ttu-id="3e7aa-114">Value</span><span class="sxs-lookup"><span data-stu-id="3e7aa-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e7aa-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e7aa-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3e7aa-116">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="3e7aa-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3e7aa-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e7aa-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3e7aa-118">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="3e7aa-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3e7aa-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e7aa-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e7aa-120"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e7aa-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





