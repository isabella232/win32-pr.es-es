---
description: 'Método StartService de la Msvm_SecurityService : inicia el servicio.'
ms.assetid: 59918c15-7216-4cf7-9215-b27532febc72
title: Método StartService de la Msvm_SecurityService clase
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
ms.openlocfilehash: 31e16eea84cf61ace11c241b6409a5810f74b8f1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111403"
---
# <a name="startservice-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="637ac-103">Método StartService de la clase SecurityService de Msvm \_</span><span class="sxs-lookup"><span data-stu-id="637ac-103">StartService method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="637ac-104">inicia el servicio.</span><span class="sxs-lookup"><span data-stu-id="637ac-104">Starts the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="637ac-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="637ac-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="637ac-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="637ac-106">Parameters</span></span>

<span data-ttu-id="637ac-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="637ac-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="637ac-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="637ac-108">Return value</span></span>

<span data-ttu-id="637ac-109">Si se ejecuta correctamente, devuelve 0; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="637ac-109">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="637ac-110">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="637ac-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="637ac-111">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="637ac-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="637ac-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="637ac-112">Requirements</span></span>



| <span data-ttu-id="637ac-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="637ac-113">Requirement</span></span> | <span data-ttu-id="637ac-114">Valor</span><span class="sxs-lookup"><span data-stu-id="637ac-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="637ac-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="637ac-115">Minimum supported client</span></span><br/> | <span data-ttu-id="637ac-116">Windows 10, solo aplicaciones de escritorio de la versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="637ac-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="637ac-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="637ac-117">Minimum supported server</span></span><br/> | <span data-ttu-id="637ac-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="637ac-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="637ac-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="637ac-119">Namespace</span></span><br/>                | <span data-ttu-id="637ac-120">Virtualización \\ raíz \\ v2</span><span class="sxs-lookup"><span data-stu-id="637ac-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="637ac-121">MOF</span><span class="sxs-lookup"><span data-stu-id="637ac-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="637ac-122"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="637ac-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="637ac-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="637ac-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="637ac-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="637ac-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="637ac-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="637ac-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="637ac-126">**SecurityService de Msvm \_**</span><span class="sxs-lookup"><span data-stu-id="637ac-126">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




