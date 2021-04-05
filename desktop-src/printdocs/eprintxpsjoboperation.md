---
description: Especifica si un trabajo de impresión XPS está en la fase de puesta en cola o en la fase de representación.
ms.assetid: 14871d29-59e4-45a2-9697-12550c58396c
title: Enumeración EPrintXPSJobOperation (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobOperation
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 917993be2af6e7a78afaec1ad4749dadcaebecba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813547"
---
# <a name="eprintxpsjoboperation-enumeration"></a><span data-ttu-id="90c6c-103">Enumeración EPrintXPSJobOperation</span><span class="sxs-lookup"><span data-stu-id="90c6c-103">EPrintXPSJobOperation enumeration</span></span>

<span data-ttu-id="90c6c-104">Especifica si un trabajo de impresión XPS está en la fase de puesta en cola o en la fase de representación.</span><span class="sxs-lookup"><span data-stu-id="90c6c-104">Specifies whether an XPS print job is in the spooling or the rendering phase.</span></span>

## <a name="syntax"></a><span data-ttu-id="90c6c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90c6c-105">Syntax</span></span>


```C++
typedef enum tagEPrintXPSJobOperation { 
  kJobProduction,
  kJobConsumption
} EPrintXPSJobOperation;
```



## <a name="constants"></a><span data-ttu-id="90c6c-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="90c6c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="90c6c-107"><span id="kJobProduction"></span><span id="kjobproduction"></span><span id="KJOBPRODUCTION"></span>**kJobProduction**</span><span class="sxs-lookup"><span data-stu-id="90c6c-107"><span id="kJobProduction"></span><span id="kjobproduction"></span><span id="KJOBPRODUCTION"></span>**kJobProduction**</span></span>
</dt> <dd>

<span data-ttu-id="90c6c-108">El trabajo XPS está en cola.</span><span class="sxs-lookup"><span data-stu-id="90c6c-108">The XPS job is spooling.</span></span>

</dd> <dt>

<span data-ttu-id="90c6c-109"><span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**kJobConsumption**</span><span class="sxs-lookup"><span data-stu-id="90c6c-109"><span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**kJobConsumption**</span></span>
</dt> <dd>

<span data-ttu-id="90c6c-110">El trabajo XPS se está representando.</span><span class="sxs-lookup"><span data-stu-id="90c6c-110">The XPS job is rendering.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90c6c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90c6c-111">Remarks</span></span>

<span data-ttu-id="90c6c-112">Esta enumeración se usa principalmente como parámetro para la función [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) .</span><span class="sxs-lookup"><span data-stu-id="90c6c-112">This enumeration is primarily used as a parameter for the [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="90c6c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90c6c-113">Requirements</span></span>



| <span data-ttu-id="90c6c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="90c6c-114">Requirement</span></span> | <span data-ttu-id="90c6c-115">Value</span><span class="sxs-lookup"><span data-stu-id="90c6c-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90c6c-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90c6c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="90c6c-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="90c6c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="90c6c-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90c6c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="90c6c-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="90c6c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="90c6c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90c6c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="90c6c-121"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="90c6c-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



 

 




