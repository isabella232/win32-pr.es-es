---
description: Indica el estado actual de un experto en ejecución.
ms.assetid: 49107459-599c-4710-8935-4b2c789081de
title: Estructura EXPERTSTATUS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a9e201b692bb82c78f88a35f22f2688d096f1771
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540235"
---
# <a name="expertstatus-structure"></a><span data-ttu-id="10150-103">Estructura EXPERTSTATUS</span><span class="sxs-lookup"><span data-stu-id="10150-103">EXPERTSTATUS structure</span></span>

<span data-ttu-id="10150-104">La estructura **EXPERTSTATUS** indica el estado actual de un experto en ejecución.</span><span class="sxs-lookup"><span data-stu-id="10150-104">The **EXPERTSTATUS** structure indicates the current status of a running expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="10150-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10150-105">Syntax</span></span>


```C++
typedef struct {
  EXPERTSTATUSENUMERATION Status;
  DWORD                   SubStatus;
  DWORD                   PercentDone;
  DWORD                   Frame;
  char                    szStatusText[EXPERTSTRINGLENGTH];
} EXPERTSTATUS, *PEXPERTSTATUS;
```



## <a name="members"></a><span data-ttu-id="10150-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="10150-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="10150-107">**Estado**</span><span class="sxs-lookup"><span data-stu-id="10150-107">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="10150-108">Valor de estado de experto actual definido por la enumeración [**EXPERTSTATUSENUMERATION**](expertstatusenumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="10150-108">Current expert status value defined by the [**EXPERTSTATUSENUMERATION**](expertstatusenumeration.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="10150-109">**Subestado**</span><span class="sxs-lookup"><span data-stu-id="10150-109">**SubStatus**</span></span>
</dt> <dd>

<span data-ttu-id="10150-110">Valor de subestado.</span><span class="sxs-lookup"><span data-stu-id="10150-110">Sub-status value.</span></span>

</dd> <dt>

<span data-ttu-id="10150-111">**PercentDone**</span><span class="sxs-lookup"><span data-stu-id="10150-111">**PercentDone**</span></span>
</dt> <dd>

<span data-ttu-id="10150-112">Porcentaje de finalización del análisis experto de datos de red.</span><span class="sxs-lookup"><span data-stu-id="10150-112">Percentage completion of the expert analysis of network data.</span></span>

</dd> <dt>

<span data-ttu-id="10150-113">**Frame**</span><span class="sxs-lookup"><span data-stu-id="10150-113">**Frame**</span></span>
</dt> <dd>

<span data-ttu-id="10150-114">Número de marco.</span><span class="sxs-lookup"><span data-stu-id="10150-114">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="10150-115">**Szstatustext del**</span><span class="sxs-lookup"><span data-stu-id="10150-115">**szStatusText**</span></span>
</dt> <dd>

<span data-ttu-id="10150-116">Texto que describe el estado del experto.</span><span class="sxs-lookup"><span data-stu-id="10150-116">Text that describes the expert status.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="10150-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10150-117">Requirements</span></span>



| <span data-ttu-id="10150-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="10150-118">Requirement</span></span> | <span data-ttu-id="10150-119">Value</span><span class="sxs-lookup"><span data-stu-id="10150-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="10150-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10150-120">Minimum supported client</span></span><br/> | <span data-ttu-id="10150-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="10150-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="10150-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10150-122">Minimum supported server</span></span><br/> | <span data-ttu-id="10150-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="10150-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="10150-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10150-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="10150-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="10150-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




