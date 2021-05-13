---
description: Establece u obtiene el estado de las cuotas de disco del volumen.
title: Propiedad DiskQuotaControl.QuotaState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaState
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b0766ecf-6e22-4481-a6a7-df873a277bc2
ms.openlocfilehash: 3580ad47a5ec6a5d0276dc0e30a4a6463aca2fb3
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843196"
---
# <a name="diskquotacontrolquotastate-property"></a><span data-ttu-id="a22bb-103">Propiedad DiskQuotaControl.QuotaState</span><span class="sxs-lookup"><span data-stu-id="a22bb-103">DiskQuotaControl.QuotaState property</span></span>

<span data-ttu-id="a22bb-104">Establece u obtiene el estado de las cuotas de disco del volumen.</span><span class="sxs-lookup"><span data-stu-id="a22bb-104">Sets or gets the state of the volume's disk quotas.</span></span>

<span data-ttu-id="a22bb-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a22bb-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a22bb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a22bb-106">Syntax</span></span>


```JScript
iQuotaState = DiskQuotaControl.QuotaState
DiskQuotaControl.QuotaState = iQuotaState
```



## <a name="property-value"></a><span data-ttu-id="a22bb-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a22bb-107">Property value</span></span>

<span data-ttu-id="a22bb-108">Esta propiedad se puede establecer en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a22bb-108">This property can be set to one of the following values.</span></span>



| <span data-ttu-id="a22bb-109">Estado</span><span class="sxs-lookup"><span data-stu-id="a22bb-109">State</span></span>          | <span data-ttu-id="a22bb-110">Value</span><span class="sxs-lookup"><span data-stu-id="a22bb-110">Value</span></span> | <span data-ttu-id="a22bb-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a22bb-111">Description</span></span>               |
|----------------|-------|---------------------------|
| <span data-ttu-id="a22bb-112">dqStateDisable</span><span class="sxs-lookup"><span data-stu-id="a22bb-112">dqStateDisable</span></span> | <span data-ttu-id="a22bb-113">0</span><span class="sxs-lookup"><span data-stu-id="a22bb-113">0</span></span>     | <span data-ttu-id="a22bb-114">Las cuotas de disco están deshabilitadas.</span><span class="sxs-lookup"><span data-stu-id="a22bb-114">Disk quotas are disabled.</span></span> |
| <span data-ttu-id="a22bb-115">dqStateTrack</span><span class="sxs-lookup"><span data-stu-id="a22bb-115">dqStateTrack</span></span>   | <span data-ttu-id="a22bb-116">1</span><span class="sxs-lookup"><span data-stu-id="a22bb-116">1</span></span>     | <span data-ttu-id="a22bb-117">Las cuotas de disco están deshabilitadas.</span><span class="sxs-lookup"><span data-stu-id="a22bb-117">Disk quotas are disabled.</span></span> |
| <span data-ttu-id="a22bb-118">dqStateEnforce</span><span class="sxs-lookup"><span data-stu-id="a22bb-118">dqStateEnforce</span></span> | <span data-ttu-id="a22bb-119">2</span><span class="sxs-lookup"><span data-stu-id="a22bb-119">2</span></span>     | <span data-ttu-id="a22bb-120">Exigir límite de cuota.</span><span class="sxs-lookup"><span data-stu-id="a22bb-120">Enforce quota limit.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="a22bb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a22bb-121">Requirements</span></span>



| <span data-ttu-id="a22bb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a22bb-122">Requirement</span></span> | <span data-ttu-id="a22bb-123">Value</span><span class="sxs-lookup"><span data-stu-id="a22bb-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a22bb-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a22bb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a22bb-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a22bb-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a22bb-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a22bb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a22bb-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a22bb-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a22bb-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a22bb-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a22bb-129"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="a22bb-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a22bb-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a22bb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a22bb-131">**DiskQuotaControl (objeto)**</span><span class="sxs-lookup"><span data-stu-id="a22bb-131">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




