---
description: Solicita un restablecimiento del LogicalDevice.
ms.assetid: f7655825-3de5-421f-a3e9-97d2f605affd
title: Método Reset de la clase CIM_LogicalDevice (administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 851332103143e84863762d8cc1183ec3ad841ca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361158"
---
# <a name="reset-method-of-the-cim_logicaldevice-class-hyper-v-management"></a><span data-ttu-id="01d65-103">Método Reset de la clase CIM_LogicalDevice (administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="01d65-103">Reset method of the CIM_LogicalDevice class (Hyper-V management)</span></span>

<span data-ttu-id="01d65-104">Solicita un restablecimiento del LogicalDevice.</span><span class="sxs-lookup"><span data-stu-id="01d65-104">Requests a reset of the LogicalDevice.</span></span> <span data-ttu-id="01d65-105">En una subclase, se puede especificar el conjunto de códigos de retorno posibles mediante un calificador ValueMap en el método.</span><span class="sxs-lookup"><span data-stu-id="01d65-105">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="01d65-106">También se pueden especificar en la subclase como calificador de la matriz Values las cadenas a las que se ha traducido el contenido ValueMap.</span><span class="sxs-lookup"><span data-stu-id="01d65-106">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="01d65-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01d65-107">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="01d65-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01d65-108">Parameters</span></span>

<span data-ttu-id="01d65-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="01d65-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="01d65-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01d65-110">Return value</span></span>

<span data-ttu-id="01d65-111">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="01d65-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="01d65-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01d65-112">Requirements</span></span>



| <span data-ttu-id="01d65-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="01d65-113">Requirement</span></span> | <span data-ttu-id="01d65-114">Value</span><span class="sxs-lookup"><span data-stu-id="01d65-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01d65-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01d65-115">Minimum supported client</span></span><br/> | <span data-ttu-id="01d65-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="01d65-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="01d65-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01d65-117">Minimum supported server</span></span><br/> | <span data-ttu-id="01d65-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="01d65-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="01d65-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="01d65-119">Namespace</span></span><br/>                | <span data-ttu-id="01d65-120">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="01d65-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="01d65-121">MOF</span><span class="sxs-lookup"><span data-stu-id="01d65-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01d65-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01d65-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="01d65-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="01d65-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01d65-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="01d65-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="01d65-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="01d65-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01d65-126">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="01d65-126">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




