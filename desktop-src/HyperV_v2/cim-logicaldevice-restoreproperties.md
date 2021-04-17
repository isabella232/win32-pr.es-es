---
description: Solicita que el dispositivo vuelva a establecer la configuración, la configuración o la información de estado desde una memoria auxiliar.
ms.assetid: 5a70f048-b335-4617-ae49-a99e728fa2e8
title: Método RestoreProperties de la clase CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.RestoreProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c8298b4d88e3886c0f8d1321032f09379da7c9e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668435"
---
# <a name="restoreproperties-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="627c1-103">Método RestoreProperties de la clase de LogicalDevice de CIM \_</span><span class="sxs-lookup"><span data-stu-id="627c1-103">RestoreProperties method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="627c1-104">Solicita que el dispositivo vuelva a establecer la configuración, la configuración o la información de estado desde una memoria auxiliar.</span><span class="sxs-lookup"><span data-stu-id="627c1-104">Requests that the Device re-establish its configuration, setup and/or state information from a backing store.</span></span> <span data-ttu-id="627c1-105">La intención es capturar esta información en un momento anterior (a través del método SaveProperties) y usarla para devolver un dispositivo a esta "condición" anterior.</span><span class="sxs-lookup"><span data-stu-id="627c1-105">The intent is to capture this information at an earlier time (via the SaveProperties method), and use it to return a Device to this earlier "condition".</span></span> <span data-ttu-id="627c1-106">Es posible que este método no sea compatible con todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="627c1-106">This method may not be supported by all Devices.</span></span> <span data-ttu-id="627c1-107">El método debe devolver 0 si se realiza correctamente, 1 si no se admite la solicitud y otro valor si se produjo algún otro error.</span><span class="sxs-lookup"><span data-stu-id="627c1-107">The method should return 0 if successful, 1 if the request is not supported, and some other value if any other error occurred.</span></span> <span data-ttu-id="627c1-108">En una subclase, se puede especificar el conjunto de códigos de retorno posibles mediante un calificador ValueMap en el método.</span><span class="sxs-lookup"><span data-stu-id="627c1-108">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="627c1-109">También se pueden especificar en la subclase como calificador de la matriz Values las cadenas a las que se ha traducido el contenido ValueMap.</span><span class="sxs-lookup"><span data-stu-id="627c1-109">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="627c1-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="627c1-110">Syntax</span></span>


```mof
uint32 RestoreProperties();
```



## <a name="parameters"></a><span data-ttu-id="627c1-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="627c1-111">Parameters</span></span>

<span data-ttu-id="627c1-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="627c1-112">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="627c1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="627c1-113">Requirements</span></span>



| <span data-ttu-id="627c1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="627c1-114">Requirement</span></span> | <span data-ttu-id="627c1-115">Value</span><span class="sxs-lookup"><span data-stu-id="627c1-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="627c1-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="627c1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="627c1-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="627c1-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="627c1-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="627c1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="627c1-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="627c1-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="627c1-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="627c1-120">Namespace</span></span><br/>                | <span data-ttu-id="627c1-121">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="627c1-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="627c1-122">MOF</span><span class="sxs-lookup"><span data-stu-id="627c1-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="627c1-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="627c1-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="627c1-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="627c1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="627c1-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="627c1-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="627c1-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="627c1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="627c1-127">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="627c1-127">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




