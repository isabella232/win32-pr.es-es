---
description: Solicita que el dispositivo Capture su configuración actual, la configuración o la información de estado en una memoria auxiliar.
ms.assetid: e47aea90-06f9-441c-bb30-aa742b49ce72
title: Método SaveProperties de la clase CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SaveProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b9a30c955dca01b57238c3e2f8b0315d1d6fc25a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688455"
---
# <a name="saveproperties-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="64d57-103">Método SaveProperties de la clase de LogicalDevice de CIM \_</span><span class="sxs-lookup"><span data-stu-id="64d57-103">SaveProperties method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="64d57-104">Solicita que el dispositivo Capture su configuración actual, la configuración o la información de estado en una memoria auxiliar.</span><span class="sxs-lookup"><span data-stu-id="64d57-104">Requests that the Device capture its current configuration, setup and/or state information in a backing store.</span></span> <span data-ttu-id="64d57-105">El objetivo sería usar esta información más adelante (a través del método RestoreProperties) para devolver un dispositivo a su "condición" actual.</span><span class="sxs-lookup"><span data-stu-id="64d57-105">The goal would be to use this information at a later time (via the RestoreProperties method), to return a Device to its present "condition".</span></span> <span data-ttu-id="64d57-106">Es posible que este método no sea compatible con todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="64d57-106">This method may not be supported by all Devices.</span></span> <span data-ttu-id="64d57-107">El método debe devolver 0 si se realiza correctamente, 1 si no se admite la solicitud y otro valor si se produjo algún otro error.</span><span class="sxs-lookup"><span data-stu-id="64d57-107">The method should return 0 if successful, 1 if the request is not supported, and some other value if any other error occurred.</span></span> <span data-ttu-id="64d57-108">En una subclase, se puede especificar el conjunto de códigos de retorno posibles mediante un calificador ValueMap en el método.</span><span class="sxs-lookup"><span data-stu-id="64d57-108">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="64d57-109">También se pueden especificar en la subclase como calificador de la matriz Values las cadenas a las que se ha traducido el contenido ValueMap.</span><span class="sxs-lookup"><span data-stu-id="64d57-109">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="64d57-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64d57-110">Syntax</span></span>


```mof
uint32 SaveProperties();
```



## <a name="parameters"></a><span data-ttu-id="64d57-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="64d57-111">Parameters</span></span>

<span data-ttu-id="64d57-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="64d57-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="64d57-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64d57-113">Return value</span></span>

<span data-ttu-id="64d57-114">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="64d57-114">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="64d57-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64d57-115">Requirements</span></span>



| <span data-ttu-id="64d57-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="64d57-116">Requirement</span></span> | <span data-ttu-id="64d57-117">Value</span><span class="sxs-lookup"><span data-stu-id="64d57-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64d57-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64d57-118">Minimum supported client</span></span><br/> | <span data-ttu-id="64d57-119">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="64d57-119">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="64d57-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64d57-120">Minimum supported server</span></span><br/> | <span data-ttu-id="64d57-121">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="64d57-121">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="64d57-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="64d57-122">Namespace</span></span><br/>                | <span data-ttu-id="64d57-123">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="64d57-123">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="64d57-124">MOF</span><span class="sxs-lookup"><span data-stu-id="64d57-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64d57-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64d57-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="64d57-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="64d57-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64d57-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="64d57-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="64d57-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="64d57-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64d57-129">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="64d57-129">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




