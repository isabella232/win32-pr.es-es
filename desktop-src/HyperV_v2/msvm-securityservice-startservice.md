---
description: inicia el servicio.
ms.assetid: 59918c15-7216-4cf7-9215-b27532febc72
title: Método StartService de la clase Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bff2721b942b6bb145f2d57492f27d1cabb722bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105670017"
---
# <a name="startservice-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="d4007-103">Método StartService de la \_ clase MSVM SecurityService</span><span class="sxs-lookup"><span data-stu-id="d4007-103">StartService method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="d4007-104">inicia el servicio.</span><span class="sxs-lookup"><span data-stu-id="d4007-104">Starts the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4007-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4007-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="d4007-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4007-106">Parameters</span></span>

<span data-ttu-id="d4007-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d4007-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d4007-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4007-108">Return value</span></span>

<span data-ttu-id="d4007-109">Si se ejecuta correctamente, devuelve un 0; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="d4007-109">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="d4007-110">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="d4007-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d4007-111">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="d4007-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d4007-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4007-112">Requirements</span></span>



| <span data-ttu-id="d4007-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4007-113">Requirement</span></span> | <span data-ttu-id="d4007-114">Value</span><span class="sxs-lookup"><span data-stu-id="d4007-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4007-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4007-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d4007-116">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="d4007-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d4007-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4007-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d4007-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d4007-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d4007-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d4007-119">Namespace</span></span><br/>                | <span data-ttu-id="d4007-120">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="d4007-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d4007-121">MOF</span><span class="sxs-lookup"><span data-stu-id="d4007-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4007-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d4007-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4007-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d4007-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4007-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d4007-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d4007-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4007-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4007-126">**MSVM \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="d4007-126">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




