---
description: Restablece el dispositivo.
ms.assetid: 4ac8ee27-0629-45aa-80ee-f308c044d7fc
title: Método Reset de la clase Msvm_SerialController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialController.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bf5fd2ff0218a4a4f39e64921e41fd497753d04e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687627"
---
# <a name="reset-method-of-the-msvm_serialcontroller-class"></a><span data-ttu-id="bf00d-103">Método Reset de la \_ clase MSVM SerialController</span><span class="sxs-lookup"><span data-stu-id="bf00d-103">Reset method of the Msvm\_SerialController class</span></span>

<span data-ttu-id="bf00d-104">Restablece el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bf00d-104">Resets the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf00d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf00d-105">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="bf00d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf00d-106">Parameters</span></span>

<span data-ttu-id="bf00d-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="bf00d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bf00d-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf00d-108">Return value</span></span>

<span data-ttu-id="bf00d-109">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="bf00d-109">Returns 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="bf00d-110">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="bf00d-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bf00d-111">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="bf00d-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bf00d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf00d-112">Requirements</span></span>



| <span data-ttu-id="bf00d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf00d-113">Requirement</span></span> | <span data-ttu-id="bf00d-114">Value</span><span class="sxs-lookup"><span data-stu-id="bf00d-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf00d-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf00d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bf00d-116">Windows 8.1, versión 1703</span><span class="sxs-lookup"><span data-stu-id="bf00d-116">Windows 8.1, version 1703</span></span><br/>                                                                    |
| <span data-ttu-id="bf00d-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf00d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bf00d-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="bf00d-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="bf00d-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bf00d-119">Namespace</span></span><br/>                | <span data-ttu-id="bf00d-120">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="bf00d-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bf00d-121">MOF</span><span class="sxs-lookup"><span data-stu-id="bf00d-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf00d-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf00d-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf00d-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bf00d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf00d-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bf00d-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bf00d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf00d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf00d-126">**MSVM \_ SerialController**</span><span class="sxs-lookup"><span data-stu-id="bf00d-126">**Msvm\_SerialController**</span></span>](msvm-serialcontroller.md)
</dt> </dl>

 

 




