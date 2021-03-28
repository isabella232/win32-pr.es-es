---
description: Establece u obtiene el estado de las cuotas de disco del volumen.
title: Propiedad DiskQuotaControl. QuotaState
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
ms.openlocfilehash: 460decc1068642ae797723b31f7350082f591d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497896"
---
# <a name="diskquotacontrolquotastate-property"></a><span data-ttu-id="2f398-103">Propiedad DiskQuotaControl. QuotaState</span><span class="sxs-lookup"><span data-stu-id="2f398-103">DiskQuotaControl.QuotaState property</span></span>

<span data-ttu-id="2f398-104">Establece u obtiene el estado de las cuotas de disco del volumen.</span><span class="sxs-lookup"><span data-stu-id="2f398-104">Sets or gets the state of the volume's disk quotas.</span></span>

<span data-ttu-id="2f398-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="2f398-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f398-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f398-106">Syntax</span></span>


```JScript
iQuotaState = DiskQuotaControl.QuotaState
DiskQuotaControl.QuotaState = iQuotaState
```



## <a name="property-value"></a><span data-ttu-id="2f398-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2f398-107">Property value</span></span>

<span data-ttu-id="2f398-108">Esta propiedad se puede establecer en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2f398-108">This property can be set to one of the following values.</span></span>



| <span data-ttu-id="2f398-109">Estado</span><span class="sxs-lookup"><span data-stu-id="2f398-109">State</span></span>          | <span data-ttu-id="2f398-110">Value</span><span class="sxs-lookup"><span data-stu-id="2f398-110">Value</span></span> | <span data-ttu-id="2f398-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f398-111">Description</span></span>               |
|----------------|-------|---------------------------|
| <span data-ttu-id="2f398-112">dqStateDisable</span><span class="sxs-lookup"><span data-stu-id="2f398-112">dqStateDisable</span></span> | <span data-ttu-id="2f398-113">0</span><span class="sxs-lookup"><span data-stu-id="2f398-113">0</span></span>     | <span data-ttu-id="2f398-114">Las cuotas de disco están deshabilitadas.</span><span class="sxs-lookup"><span data-stu-id="2f398-114">Disk quotas are disabled.</span></span> |
| <span data-ttu-id="2f398-115">dqStateTrack</span><span class="sxs-lookup"><span data-stu-id="2f398-115">dqStateTrack</span></span>   | <span data-ttu-id="2f398-116">1</span><span class="sxs-lookup"><span data-stu-id="2f398-116">1</span></span>     | <span data-ttu-id="2f398-117">Las cuotas de disco están deshabilitadas.</span><span class="sxs-lookup"><span data-stu-id="2f398-117">Disk quotas are disabled.</span></span> |
| <span data-ttu-id="2f398-118">dqStateEnforce</span><span class="sxs-lookup"><span data-stu-id="2f398-118">dqStateEnforce</span></span> | <span data-ttu-id="2f398-119">2</span><span class="sxs-lookup"><span data-stu-id="2f398-119">2</span></span>     | <span data-ttu-id="2f398-120">Aplique el límite de cuota.</span><span class="sxs-lookup"><span data-stu-id="2f398-120">Enforce quota limit.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="2f398-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f398-121">Requirements</span></span>



| <span data-ttu-id="2f398-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f398-122">Requirement</span></span> | <span data-ttu-id="2f398-123">Value</span><span class="sxs-lookup"><span data-stu-id="2f398-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f398-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f398-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2f398-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2f398-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f398-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f398-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2f398-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2f398-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2f398-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2f398-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f398-129"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="2f398-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f398-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f398-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f398-131">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="2f398-131">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




