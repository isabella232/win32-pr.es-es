---
description: Bloquea o libera los medios.
ms.assetid: 90f7e06c-92d0-4742-a74d-68ae6bfc00bf
title: Método LockMedia de la clase Msvm_DisketteDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4f9bce4e9e46d76c3426271af16c28026c242fa9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914150"
---
# <a name="lockmedia-method-of-the-msvm_diskettedrive-class"></a><span data-ttu-id="dd5f2-103">Método LockMedia de la \_ clase DisketteDrive de MSVM</span><span class="sxs-lookup"><span data-stu-id="dd5f2-103">LockMedia method of the Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="dd5f2-104">Bloquea o libera los medios.</span><span class="sxs-lookup"><span data-stu-id="dd5f2-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd5f2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd5f2-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="dd5f2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd5f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd5f2-107">*Bloquear* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dd5f2-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd5f2-108">**true** para bloquear el medio; **false** para liberar el medio.</span><span class="sxs-lookup"><span data-stu-id="dd5f2-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd5f2-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd5f2-109">Return value</span></span>

<span data-ttu-id="dd5f2-110">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="dd5f2-110">Returns a 0 on success; otherwise, returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="dd5f2-111">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="dd5f2-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dd5f2-112">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="dd5f2-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="dd5f2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd5f2-113">Requirements</span></span>



| <span data-ttu-id="dd5f2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd5f2-114">Requirement</span></span> | <span data-ttu-id="dd5f2-115">Value</span><span class="sxs-lookup"><span data-stu-id="dd5f2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd5f2-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd5f2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dd5f2-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dd5f2-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="dd5f2-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd5f2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dd5f2-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="dd5f2-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="dd5f2-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dd5f2-120">Namespace</span></span><br/>                | <span data-ttu-id="dd5f2-121">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="dd5f2-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dd5f2-122">MOF</span><span class="sxs-lookup"><span data-stu-id="dd5f2-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd5f2-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd5f2-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd5f2-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dd5f2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd5f2-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dd5f2-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dd5f2-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd5f2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd5f2-127">**MSVM \_ DisketteDrive**</span><span class="sxs-lookup"><span data-stu-id="dd5f2-127">**Msvm\_DisketteDrive**</span></span>](msvm-diskettedrive.md)
</dt> </dl>

 

 




