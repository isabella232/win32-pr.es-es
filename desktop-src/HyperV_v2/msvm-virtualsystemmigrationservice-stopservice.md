---
description: 'Método StopService de la clase Msvm_VirtualSystemMigrationService : detiene el servicio.'
ms.assetid: cf0dde8d-b6cf-4a52-905f-c686ac41e314
title: Método StopService de la Msvm_VirtualSystemMigrationService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f945f20e86c25b89bf935e46140c1f994e8735b8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109353"
---
# <a name="stopservice-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="8af39-103">Método StopService de la clase Msvm \_ VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="8af39-103">StopService method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="8af39-104">detiene el servicio.</span><span class="sxs-lookup"><span data-stu-id="8af39-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="8af39-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8af39-105">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="8af39-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8af39-106">Parameters</span></span>

<span data-ttu-id="8af39-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8af39-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8af39-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8af39-108">Return value</span></span>

<span data-ttu-id="8af39-109">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="8af39-109">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="8af39-110">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="8af39-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8af39-111">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="8af39-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8af39-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8af39-112">Requirements</span></span>



| <span data-ttu-id="8af39-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8af39-113">Requirement</span></span> | <span data-ttu-id="8af39-114">Valor</span><span class="sxs-lookup"><span data-stu-id="8af39-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8af39-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8af39-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8af39-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8af39-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="8af39-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8af39-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8af39-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8af39-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="8af39-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8af39-119">Namespace</span></span><br/>                | <span data-ttu-id="8af39-120">Virtualización \\ raíz \\ v2</span><span class="sxs-lookup"><span data-stu-id="8af39-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8af39-121">MOF</span><span class="sxs-lookup"><span data-stu-id="8af39-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8af39-122"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="8af39-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8af39-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8af39-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8af39-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8af39-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8af39-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8af39-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8af39-126">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="8af39-126">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




