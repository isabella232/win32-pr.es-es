---
description: Bloquea o Desbloquea los medios.
ms.assetid: 805efb2d-71a7-4c74-821f-942644928ff9
title: Método LockMedia de la clase Msvm_DiskDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7ddc082ca6ceb7141eaa42bdfddf7a97897a9240
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689660"
---
# <a name="lockmedia-method-of-the-msvm_diskdrive-class"></a><span data-ttu-id="0e243-103">Método LockMedia de la \_ clase DiskDrive de MSVM</span><span class="sxs-lookup"><span data-stu-id="0e243-103">LockMedia method of the Msvm\_DiskDrive class</span></span>

<span data-ttu-id="0e243-104">Bloquea o Desbloquea los medios.</span><span class="sxs-lookup"><span data-stu-id="0e243-104">Locks or unlocks the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e243-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e243-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="0e243-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0e243-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e243-107">*Bloquear* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0e243-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e243-108">**true** para bloquear el medio; **false** para liberar el medio.</span><span class="sxs-lookup"><span data-stu-id="0e243-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e243-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0e243-109">Return value</span></span>

<span data-ttu-id="0e243-110">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="0e243-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="0e243-111">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="0e243-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0e243-112">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="0e243-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0e243-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e243-113">Requirements</span></span>



| <span data-ttu-id="0e243-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e243-114">Requirement</span></span> | <span data-ttu-id="0e243-115">Value</span><span class="sxs-lookup"><span data-stu-id="0e243-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e243-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e243-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0e243-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0e243-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="0e243-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e243-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0e243-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0e243-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="0e243-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0e243-120">Namespace</span></span><br/>                | <span data-ttu-id="0e243-121">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="0e243-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0e243-122">MOF</span><span class="sxs-lookup"><span data-stu-id="0e243-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e243-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e243-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e243-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0e243-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e243-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0e243-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0e243-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e243-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e243-127">**MSVM \_ DiskDrive**</span><span class="sxs-lookup"><span data-stu-id="0e243-127">**Msvm\_DiskDrive**</span></span>](msvm-diskdrive.md)
</dt> </dl>

 

 




