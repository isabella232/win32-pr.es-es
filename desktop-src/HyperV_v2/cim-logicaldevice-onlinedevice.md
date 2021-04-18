---
description: El método OnlineDevice ha quedado en desuso en lugar del método RequestStateChange más general que se superpone directamente con la funcionalidad proporcionada por este método.
ms.assetid: c96b5653-1e5e-421a-b2fe-65ee9ee94ee4
title: Método OnlineDevice de la clase CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.OnlineDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 56e5fae557198a713aec338f92ad8f2865b2c351
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688377"
---
# <a name="onlinedevice-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="96a14-103">Método OnlineDevice de la clase de LogicalDevice de CIM \_</span><span class="sxs-lookup"><span data-stu-id="96a14-103">OnlineDevice method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="96a14-104">El método **OnlineDevice** ha quedado en desuso en lugar del método **RequestStateChange** más general que se superpone directamente con la funcionalidad proporcionada por este método.</span><span class="sxs-lookup"><span data-stu-id="96a14-104">The **OnlineDevice** method has been deprecated in lieu of the more general **RequestStateChange** method that directly overlaps with the functionality provided by this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="96a14-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96a14-105">Syntax</span></span>


```mof
uint32 OnlineDevice(
  [in] boolean Online
);
```



## <a name="parameters"></a><span data-ttu-id="96a14-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96a14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96a14-107">*En línea* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="96a14-107">*Online* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96a14-108">Si **es true**, ponga el dispositivo en línea; si **es false**, ponga el dispositivo sin conexión.</span><span class="sxs-lookup"><span data-stu-id="96a14-108">If **TRUE**, take the device online, if **FALSE**, take the device offline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96a14-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96a14-109">Return value</span></span>

<span data-ttu-id="96a14-110">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="96a14-110">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="96a14-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96a14-111">Requirements</span></span>



| <span data-ttu-id="96a14-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="96a14-112">Requirement</span></span> | <span data-ttu-id="96a14-113">Value</span><span class="sxs-lookup"><span data-stu-id="96a14-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96a14-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96a14-114">Minimum supported client</span></span><br/> | <span data-ttu-id="96a14-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="96a14-115">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="96a14-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96a14-116">Minimum supported server</span></span><br/> | <span data-ttu-id="96a14-117">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="96a14-117">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="96a14-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="96a14-118">Namespace</span></span><br/>                | <span data-ttu-id="96a14-119">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="96a14-119">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="96a14-120">MOF</span><span class="sxs-lookup"><span data-stu-id="96a14-120">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96a14-121"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="96a14-121"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="96a14-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="96a14-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96a14-123"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="96a14-123"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="96a14-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="96a14-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96a14-125">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="96a14-125">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




