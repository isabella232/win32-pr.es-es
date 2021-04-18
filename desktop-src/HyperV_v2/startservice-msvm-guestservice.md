---
description: Pone el servicio invitado en un estado Iniciado.
ms.assetid: 1DC6A5B3-0F91-4AC1-99D5-0E8CF5ED35A2
title: 'Msvm_GuestService:: StartService (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1a87bc9933bd7b3a54bd59169b0099e34eb04c52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689569"
---
# <a name="msvm_guestservicestartservice-method"></a><span data-ttu-id="f059d-103">MSVM \_ GuestService:: StartService (método)</span><span class="sxs-lookup"><span data-stu-id="f059d-103">Msvm\_GuestService::StartService method</span></span>

<span data-ttu-id="f059d-104">Pone el servicio invitado en un estado Iniciado.</span><span class="sxs-lookup"><span data-stu-id="f059d-104">Puts the guest service in a started state.</span></span>

## <a name="syntax"></a><span data-ttu-id="f059d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f059d-105">Syntax</span></span>


```C++
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="f059d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f059d-106">Parameters</span></span>

<span data-ttu-id="f059d-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f059d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f059d-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f059d-108">Return value</span></span>

<span data-ttu-id="f059d-109">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f059d-109">This method returns one of the following values.</span></span>



| <span data-ttu-id="f059d-110">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f059d-110">Return code/value</span></span>                                                                                                                                             | <span data-ttu-id="f059d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f059d-111">Description</span></span>         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="f059d-112"><dt>**Completado sin error**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f059d-112"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="f059d-113">Correcto.</span><span class="sxs-lookup"><span data-stu-id="f059d-113">Success.</span></span><br/> |
| <dl> <span data-ttu-id="f059d-114"><dt>**No compatible**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f059d-114"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>           |                     |



 

## <a name="requirements"></a><span data-ttu-id="f059d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f059d-115">Requirements</span></span>



| <span data-ttu-id="f059d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f059d-116">Requirement</span></span> | <span data-ttu-id="f059d-117">Value</span><span class="sxs-lookup"><span data-stu-id="f059d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f059d-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f059d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f059d-119">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="f059d-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f059d-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f059d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f059d-121">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f059d-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f059d-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f059d-122">Namespace</span></span><br/>                | <span data-ttu-id="f059d-123">\\\\\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f059d-123">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="f059d-124">MOF</span><span class="sxs-lookup"><span data-stu-id="f059d-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f059d-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f059d-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f059d-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f059d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f059d-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f059d-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f059d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f059d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f059d-129">**MSVM \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="f059d-129">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




