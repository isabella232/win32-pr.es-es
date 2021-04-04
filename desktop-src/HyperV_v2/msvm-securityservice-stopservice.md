---
description: detiene el servicio.
ms.assetid: cf100cea-b0e1-42e9-831e-6422aded47c5
title: Método StopService de la clase Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 68e88e2c88d4f75f4d7671c389bab0cd81d0deb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277575"
---
# <a name="stopservice-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="0727e-103">Método StopService de la \_ clase MSVM SecurityService</span><span class="sxs-lookup"><span data-stu-id="0727e-103">StopService method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="0727e-104">detiene el servicio.</span><span class="sxs-lookup"><span data-stu-id="0727e-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="0727e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0727e-105">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="0727e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0727e-106">Parameters</span></span>

<span data-ttu-id="0727e-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0727e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0727e-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0727e-108">Return value</span></span>

<span data-ttu-id="0727e-109">Si se ejecuta correctamente, devuelve un 0; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="0727e-109">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="0727e-110">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="0727e-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0727e-111">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="0727e-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0727e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0727e-112">Requirements</span></span>



| <span data-ttu-id="0727e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0727e-113">Requirement</span></span> | <span data-ttu-id="0727e-114">Value</span><span class="sxs-lookup"><span data-stu-id="0727e-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0727e-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0727e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0727e-116">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="0727e-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0727e-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0727e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0727e-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0727e-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0727e-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0727e-119">Namespace</span></span><br/>                | <span data-ttu-id="0727e-120">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="0727e-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0727e-121">MOF</span><span class="sxs-lookup"><span data-stu-id="0727e-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0727e-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0727e-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0727e-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0727e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0727e-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0727e-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0727e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0727e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0727e-126">**MSVM \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="0727e-126">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




