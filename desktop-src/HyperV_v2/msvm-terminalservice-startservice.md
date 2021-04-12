---
description: inicia el servicio.
ms.assetid: 499e4650-255f-4c84-98fc-de81d5cd6daf
title: Método StartService de la clase Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6f1902dd17d641ae50888a23d2c2699e269a90e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543590"
---
# <a name="startservice-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="302d1-103">Método StartService de la \_ clase MSVM TerminalService</span><span class="sxs-lookup"><span data-stu-id="302d1-103">StartService method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="302d1-104">inicia el servicio.</span><span class="sxs-lookup"><span data-stu-id="302d1-104">Starts the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="302d1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="302d1-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="302d1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="302d1-106">Parameters</span></span>

<span data-ttu-id="302d1-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="302d1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="302d1-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="302d1-108">Return value</span></span>

<span data-ttu-id="302d1-109">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="302d1-109">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="302d1-110">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="302d1-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="302d1-111">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="302d1-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="302d1-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="302d1-112">Requirements</span></span>



| <span data-ttu-id="302d1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="302d1-113">Requirement</span></span> | <span data-ttu-id="302d1-114">Value</span><span class="sxs-lookup"><span data-stu-id="302d1-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="302d1-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="302d1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="302d1-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="302d1-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="302d1-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="302d1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="302d1-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="302d1-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="302d1-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="302d1-119">Namespace</span></span><br/>                | <span data-ttu-id="302d1-120">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="302d1-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="302d1-121">MOF</span><span class="sxs-lookup"><span data-stu-id="302d1-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="302d1-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="302d1-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="302d1-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="302d1-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="302d1-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="302d1-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="302d1-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="302d1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="302d1-126">**MSVM \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="302d1-126">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

 




