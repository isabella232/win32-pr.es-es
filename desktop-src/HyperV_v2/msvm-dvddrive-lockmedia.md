---
description: 'Método LockMedia de la Msvm_DVDDrive : bloquea o libera el medio.'
ms.assetid: 924bc20a-901b-4618-be49-eaacf80c9465
title: Método LockMedia de la Msvm_DVDDrive clase
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
ms.openlocfilehash: e00780fbeeeec60563b31008c8e5979a09f9d173
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119153"
---
# <a name="lockmedia-method-of-the-msvm_dvddrive-class"></a><span data-ttu-id="292e4-103">Método LockMedia de la clase DVDDrive de Msvm \_</span><span class="sxs-lookup"><span data-stu-id="292e4-103">LockMedia method of the Msvm\_DVDDrive class</span></span>

<span data-ttu-id="292e4-104">Bloquea o libera el medio.</span><span class="sxs-lookup"><span data-stu-id="292e4-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="292e4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="292e4-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="292e4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="292e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="292e4-107">*Bloqueo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="292e4-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="292e4-108">**true** para bloquear el medio; **false** para liberar el medio.</span><span class="sxs-lookup"><span data-stu-id="292e4-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="292e4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="292e4-109">Return value</span></span>

<span data-ttu-id="292e4-110">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="292e4-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="292e4-111">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="292e4-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="292e4-112">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="292e4-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="292e4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="292e4-113">Requirements</span></span>



| <span data-ttu-id="292e4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="292e4-114">Requirement</span></span> | <span data-ttu-id="292e4-115">Valor</span><span class="sxs-lookup"><span data-stu-id="292e4-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="292e4-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="292e4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="292e4-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="292e4-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="292e4-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="292e4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="292e4-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="292e4-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="292e4-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="292e4-120">Namespace</span></span><br/>                | <span data-ttu-id="292e4-121">Virtualización \\ raíz \\ v2</span><span class="sxs-lookup"><span data-stu-id="292e4-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="292e4-122">MOF</span><span class="sxs-lookup"><span data-stu-id="292e4-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="292e4-123"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="292e4-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="292e4-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="292e4-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="292e4-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="292e4-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="292e4-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="292e4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="292e4-127">**Msvm \_ DVDDrive**</span><span class="sxs-lookup"><span data-stu-id="292e4-127">**Msvm\_DVDDrive**</span></span>](msvm-dvddrive.md)
</dt> </dl>

 

 




