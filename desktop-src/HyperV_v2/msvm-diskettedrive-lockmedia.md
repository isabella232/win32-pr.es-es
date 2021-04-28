---
description: 'Método LockMedia de la Msvm_DisketteDrive : bloquea o libera el medio.'
ms.assetid: 90f7e06c-92d0-4742-a74d-68ae6bfc00bf
title: Método LockMedia de la Msvm_DisketteDrive clase
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
ms.openlocfilehash: 5f5f87354aa7c39534e8b32c8985c5d18b55caa9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111983"
---
# <a name="lockmedia-method-of-the-msvm_diskettedrive-class"></a><span data-ttu-id="6e392-103">Método LockMedia de la clase \_ DisketteDrive de Msvm</span><span class="sxs-lookup"><span data-stu-id="6e392-103">LockMedia method of the Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="6e392-104">Bloquea o libera el medio.</span><span class="sxs-lookup"><span data-stu-id="6e392-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e392-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e392-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="6e392-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e392-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e392-107">*Bloqueo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="6e392-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e392-108">**true** para bloquear el medio; **false** para liberar el medio.</span><span class="sxs-lookup"><span data-stu-id="6e392-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e392-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e392-109">Return value</span></span>

<span data-ttu-id="6e392-110">Devuelve un 0 si se ejecuta correctamente; de lo contrario, devuelve uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="6e392-110">Returns a 0 on success; otherwise, returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="6e392-111">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="6e392-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6e392-112">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="6e392-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6e392-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e392-113">Requirements</span></span>



| <span data-ttu-id="6e392-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e392-114">Requirement</span></span> | <span data-ttu-id="6e392-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6e392-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e392-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e392-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6e392-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6e392-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="6e392-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e392-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6e392-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6e392-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="6e392-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6e392-120">Namespace</span></span><br/>                | <span data-ttu-id="6e392-121">Virtualización \\ raíz \\ v2</span><span class="sxs-lookup"><span data-stu-id="6e392-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6e392-122">MOF</span><span class="sxs-lookup"><span data-stu-id="6e392-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e392-123"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e392-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e392-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6e392-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e392-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6e392-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6e392-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6e392-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e392-127">**DisketteDrive de Msvm \_**</span><span class="sxs-lookup"><span data-stu-id="6e392-127">**Msvm\_DisketteDrive**</span></span>](msvm-diskettedrive.md)
</dt> </dl>

 

 




