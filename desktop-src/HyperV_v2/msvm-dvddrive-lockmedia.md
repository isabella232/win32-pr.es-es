---
description: Bloquea o libera los medios.
ms.assetid: 924bc20a-901b-4618-be49-eaacf80c9465
title: Método LockMedia de la clase Msvm_DVDDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DVDDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 650a868d8e25e2ccc47271e49634827fe7d3d967
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104157040"
---
# <a name="lockmedia-method-of-the-msvm_dvddrive-class"></a><span data-ttu-id="bc294-103">Método LockMedia de la \_ clase DVDDrive de MSVM</span><span class="sxs-lookup"><span data-stu-id="bc294-103">LockMedia method of the Msvm\_DVDDrive class</span></span>

<span data-ttu-id="bc294-104">Bloquea o libera los medios.</span><span class="sxs-lookup"><span data-stu-id="bc294-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc294-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc294-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="bc294-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc294-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc294-107">*Bloquear* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc294-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc294-108">**true** para bloquear el medio; **false** para liberar el medio.</span><span class="sxs-lookup"><span data-stu-id="bc294-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc294-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc294-109">Return value</span></span>

<span data-ttu-id="bc294-110">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="bc294-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="bc294-111">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="bc294-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bc294-112">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="bc294-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bc294-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc294-113">Requirements</span></span>



| <span data-ttu-id="bc294-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc294-114">Requirement</span></span> | <span data-ttu-id="bc294-115">Value</span><span class="sxs-lookup"><span data-stu-id="bc294-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc294-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc294-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bc294-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="bc294-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="bc294-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc294-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bc294-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="bc294-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="bc294-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bc294-120">Namespace</span></span><br/>                | <span data-ttu-id="bc294-121">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="bc294-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bc294-122">MOF</span><span class="sxs-lookup"><span data-stu-id="bc294-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc294-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc294-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc294-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bc294-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc294-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bc294-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bc294-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc294-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc294-127">**MSVM \_ DVDDrive**</span><span class="sxs-lookup"><span data-stu-id="bc294-127">**Msvm\_DVDDrive**</span></span>](msvm-dvddrive.md)
</dt> </dl>

 

 




