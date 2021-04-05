---
title: Tipos de datos del registro de eventos de Windows (WinEvt. h)
description: El registro de eventos de Windows define los siguientes tipos de datos
ms.assetid: 1aad25fe-7503-4ef8-a40a-63457bd9a007
keywords:
- EVT_HANDLE
- PEVT_HANDLE
- EVT_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a93794d8cc3a254fe182c439698324dccdfc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802191"
---
# <a name="windows-event-log-data-types"></a><span data-ttu-id="5172e-106">Tipos de datos del registro de eventos de Windows</span><span class="sxs-lookup"><span data-stu-id="5172e-106">Windows Event Log Data Types</span></span>

<span data-ttu-id="5172e-107">El registro de eventos de Windows define los siguientes tipos de datos:</span><span class="sxs-lookup"><span data-stu-id="5172e-107">Windows Event Log defines the following data types:</span></span>


```C++
typedef HANDLE EVT_HANDLE;
typedef HANDLE* PEVT_HANDLE;
typedef HANDLE EVT_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

<span data-ttu-id="5172e-108">**identificador de EVT \_**</span><span class="sxs-lookup"><span data-stu-id="5172e-108">**EVT\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="5172e-109">Identificador de un objeto de registro de eventos de Windows.</span><span class="sxs-lookup"><span data-stu-id="5172e-109">A handle to a Windows Event Log object.</span></span>

</dd> <dt>

<span data-ttu-id="5172e-110">**identificador de PEVT \_**</span><span class="sxs-lookup"><span data-stu-id="5172e-110">**PEVT\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="5172e-111">Puntero al identificador de un objeto de registro de eventos de Windows.</span><span class="sxs-lookup"><span data-stu-id="5172e-111">A pointer to the handle of a Windows Event Log object.</span></span>

</dd> <dt>

<span data-ttu-id="5172e-112">**identificador de la propiedad de matriz de \_ objetos evt \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5172e-112">**EVT\_OBJECT\_ARRAY\_PROPERTY\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="5172e-113">Identificador de una matriz de objetos de registro de eventos de Windows.</span><span class="sxs-lookup"><span data-stu-id="5172e-113">A handle to an array of Windows Event Log objects.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5172e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5172e-114">Requirements</span></span>



| <span data-ttu-id="5172e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5172e-115">Requirement</span></span> | <span data-ttu-id="5172e-116">Value</span><span class="sxs-lookup"><span data-stu-id="5172e-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5172e-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5172e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5172e-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5172e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5172e-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5172e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5172e-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5172e-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5172e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5172e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5172e-122"><dt>WinEvt. h</dt></span><span class="sxs-lookup"><span data-stu-id="5172e-122"><dt>WinEvt.h</dt></span></span> </dl> |



 

 





