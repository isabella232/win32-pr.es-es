---
description: El método EnableDevice ha quedado en desuso en lugar del método RequestStateChange más general que se superpone directamente con la funcionalidad proporcionada por este método.
ms.assetid: 1d481417-b640-437d-82ed-d45a9e420d3b
title: Método EnableDevice de la clase CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.EnableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5a6da7695d7e611223a3a257be23add16094b533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667841"
---
# <a name="enabledevice-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="e8103-103">Método EnableDevice de la clase de LogicalDevice de CIM \_</span><span class="sxs-lookup"><span data-stu-id="e8103-103">EnableDevice method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="e8103-104">El método EnableDevice ha quedado en desuso en lugar del método RequestStateChange más general que se superpone directamente con la funcionalidad proporcionada por este método.</span><span class="sxs-lookup"><span data-stu-id="e8103-104">The EnableDevice method has been deprecated in lieu of the more general RequestStateChange method that directly overlaps with the functionality provided by this method.</span></span>

<span data-ttu-id="e8103-105">Solicita que el LogicalDevice esté habilitado ("habilitado" parámetro de entrada = TRUE) o deshabilitado (= FALSE).</span><span class="sxs-lookup"><span data-stu-id="e8103-105">Requests that the LogicalDevice be enabled ("Enabled" input parameter = TRUE) or disabled (= FALSE).</span></span> <span data-ttu-id="e8103-106">Si es correcto, las propiedades de StatusInfo/EnabledState del dispositivo deben reflejar el estado deseado (habilitado o deshabilitado).</span><span class="sxs-lookup"><span data-stu-id="e8103-106">If successful, the Device's StatusInfo/EnabledState properties should reflect the desired state (enabled/disabled).</span></span> <span data-ttu-id="e8103-107">Tenga en cuenta que la función de este método se superpone con la propiedad RequestedState.</span><span class="sxs-lookup"><span data-stu-id="e8103-107">Note that this method's function overlaps with the RequestedState property.</span></span> <span data-ttu-id="e8103-108">RequestedState se ha agregado al modelo para mantener un registro (es decir, un valor almacenado) de la última solicitud de estado.</span><span class="sxs-lookup"><span data-stu-id="e8103-108">RequestedState was added to the model to maintain a record (i.e., a persisted value) of the last state request.</span></span> <span data-ttu-id="e8103-109">Al invocar el método EnableDevice se debe establecer la propiedad RequestedState adecuadamente.</span><span class="sxs-lookup"><span data-stu-id="e8103-109">Invoking the EnableDevice method should set the RequestedState property appropriately.</span></span>

<span data-ttu-id="e8103-110">El código de retorno debe ser 0 si la solicitud se ejecutó correctamente, 1 si no se admite la solicitud y otro valor si se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="e8103-110">The return code should be 0 if the request was successfully executed, 1 if the request is not supported and some other value if an error occurred.</span></span> <span data-ttu-id="e8103-111">En una subclase, se puede especificar el conjunto de códigos de retorno posibles mediante un calificador ValueMap en el método.</span><span class="sxs-lookup"><span data-stu-id="e8103-111">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="e8103-112">También se pueden especificar en la subclase como calificador de la matriz Values las cadenas a las que se ha traducido el contenido ValueMap.</span><span class="sxs-lookup"><span data-stu-id="e8103-112">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8103-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8103-113">Syntax</span></span>


```mof
uint32 EnableDevice(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="e8103-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8103-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8103-115">*Habilitado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e8103-115">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8103-116">Si es TRUE, habilite el dispositivo, si es FALSE, deshabilite el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e8103-116">If TRUE enable the device, if FALSE disable the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8103-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8103-117">Return value</span></span>

<span data-ttu-id="e8103-118">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="e8103-118">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8103-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8103-119">Requirements</span></span>



| <span data-ttu-id="e8103-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8103-120">Requirement</span></span> | <span data-ttu-id="e8103-121">Value</span><span class="sxs-lookup"><span data-stu-id="e8103-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8103-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8103-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e8103-123">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e8103-123">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="e8103-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8103-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e8103-125">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e8103-125">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="e8103-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e8103-126">Namespace</span></span><br/>                | <span data-ttu-id="e8103-127">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e8103-127">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e8103-128">MOF</span><span class="sxs-lookup"><span data-stu-id="e8103-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8103-129"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8103-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8103-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e8103-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8103-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e8103-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e8103-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8103-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8103-133">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="e8103-133">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




