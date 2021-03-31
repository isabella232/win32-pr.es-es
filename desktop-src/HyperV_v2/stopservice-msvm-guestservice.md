---
description: Detiene el servicio invitado.
ms.assetid: 67FFA46C-0B61-4845-A617-BA10F4D42CBC
title: 'Msvm_GuestService:: StopService (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6c396078e2bd623a768f391a645091679694f453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907847"
---
# <a name="msvm_guestservicestopservice-method"></a><span data-ttu-id="5a556-103">MSVM \_ GuestService:: StopService (método)</span><span class="sxs-lookup"><span data-stu-id="5a556-103">Msvm\_GuestService::StopService method</span></span>

<span data-ttu-id="5a556-104">Detiene el servicio invitado.</span><span class="sxs-lookup"><span data-stu-id="5a556-104">Stops the guest service.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a556-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a556-105">Syntax</span></span>


```C++
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="5a556-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5a556-106">Parameters</span></span>

<span data-ttu-id="5a556-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5a556-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5a556-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5a556-108">Return value</span></span>

<span data-ttu-id="5a556-109">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5a556-109">This method returns one of the following values.</span></span>



| <span data-ttu-id="5a556-110">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5a556-110">Return code/value</span></span>                                                                                                                                             | <span data-ttu-id="5a556-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a556-111">Description</span></span>         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="5a556-112"><dt>**Completado sin error**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5a556-112"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="5a556-113">Correcto.</span><span class="sxs-lookup"><span data-stu-id="5a556-113">Success.</span></span><br/> |
| <dl> <span data-ttu-id="5a556-114"><dt>**No compatible**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5a556-114"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>           |                     |



 

## <a name="requirements"></a><span data-ttu-id="5a556-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a556-115">Requirements</span></span>



| <span data-ttu-id="5a556-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a556-116">Requirement</span></span> | <span data-ttu-id="5a556-117">Value</span><span class="sxs-lookup"><span data-stu-id="5a556-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a556-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a556-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5a556-119">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="5a556-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="5a556-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a556-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5a556-121">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a556-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5a556-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5a556-122">Namespace</span></span><br/>                | <span data-ttu-id="5a556-123">\\\\\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="5a556-123">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="5a556-124">MOF</span><span class="sxs-lookup"><span data-stu-id="5a556-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a556-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a556-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5a556-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5a556-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a556-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5a556-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5a556-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a556-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a556-129">**MSVM \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="5a556-129">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




