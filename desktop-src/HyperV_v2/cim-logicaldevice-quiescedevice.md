---
description: El método QuiesceDevice ha quedado en desuso en lugar del método RequestStateChange más general que se superpone directamente con la funcionalidad proporcionada por este método.
ms.assetid: c5154c00-ff9c-40d8-bb76-41ae72ce86ae
title: Método QuiesceDevice de la clase CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.QuiesceDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 82041b36592f00bf71dc7e2d744fcf94b7a666c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361160"
---
# <a name="quiescedevice-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="06f9c-103">Método QuiesceDevice de la clase de LogicalDevice de CIM \_</span><span class="sxs-lookup"><span data-stu-id="06f9c-103">QuiesceDevice method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="06f9c-104">El método **QuiesceDevice** ha quedado en desuso en lugar del método **RequestStateChange** más general que se superpone directamente con la funcionalidad proporcionada por este método.</span><span class="sxs-lookup"><span data-stu-id="06f9c-104">The **QuiesceDevice** method has been deprecated in lieu of the more general **RequestStateChange** method that directly overlaps with the functionality provided by this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="06f9c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06f9c-105">Syntax</span></span>


```mof
uint32 QuiesceDevice(
  [in] boolean Quiesce
);
```



## <a name="parameters"></a><span data-ttu-id="06f9c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06f9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06f9c-107">Modo *inactivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06f9c-107">*Quiesce* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06f9c-108">Si se establece en **true** , se detiene correctamente toda la actividad, si la actividad de reanudación **es falsa** .</span><span class="sxs-lookup"><span data-stu-id="06f9c-108">If set to **TRUE** then cleanly cease all activity, if **FALSE** resume activity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06f9c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06f9c-109">Return value</span></span>

<span data-ttu-id="06f9c-110">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="06f9c-110">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="06f9c-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06f9c-111">Requirements</span></span>



| <span data-ttu-id="06f9c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="06f9c-112">Requirement</span></span> | <span data-ttu-id="06f9c-113">Value</span><span class="sxs-lookup"><span data-stu-id="06f9c-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06f9c-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06f9c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="06f9c-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="06f9c-115">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="06f9c-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06f9c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="06f9c-117">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="06f9c-117">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="06f9c-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="06f9c-118">Namespace</span></span><br/>                | <span data-ttu-id="06f9c-119">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="06f9c-119">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="06f9c-120">MOF</span><span class="sxs-lookup"><span data-stu-id="06f9c-120">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06f9c-121"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06f9c-121"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="06f9c-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="06f9c-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06f9c-123"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="06f9c-123"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="06f9c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="06f9c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06f9c-125">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="06f9c-125">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




