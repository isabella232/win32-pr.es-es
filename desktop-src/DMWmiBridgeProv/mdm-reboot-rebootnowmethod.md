---
title: Método RebootNowMethod de la clase MDM_Reboot
description: Este método ejecuta un reinicio del dispositivo.
ms.assetid: b1bacad8-06db-4e56-9f3d-46c9a0036729
keywords:
- Método RebootNowMethod
- Método RebootNowMethod, clase MDM_Reboot
- Clase MDM_Reboot, método RebootNowMethod
topic_type:
- apiref
api_name:
- MDM_Reboot.RebootNowMethod
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d35d297858588ade6655ea84876c6e75abd719
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149934"
---
# <a name="rebootnowmethod-method-of-the-mdm_reboot-class"></a><span data-ttu-id="577bf-106">Método RebootNowMethod de la \_ clase de reinicio de MDM</span><span class="sxs-lookup"><span data-stu-id="577bf-106">RebootNowMethod method of the MDM\_Reboot class</span></span>

<span data-ttu-id="577bf-107">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="577bf-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="577bf-108">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="577bf-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="577bf-109">Este método ejecuta un reinicio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="577bf-109">This method executes a reboot of the device.</span></span> <span data-ttu-id="577bf-110">Vea también [RebootNow](/windows/client-management/mdm/reboot-csp).</span><span class="sxs-lookup"><span data-stu-id="577bf-110">See also, [RebootNow](/windows/client-management/mdm/reboot-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="577bf-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="577bf-111">Syntax</span></span>


```mof
uint32 RebootNowMethod();
```



## <a name="parameters"></a><span data-ttu-id="577bf-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="577bf-112">Parameters</span></span>

<span data-ttu-id="577bf-113">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="577bf-113">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="577bf-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="577bf-114">Requirements</span></span>



| <span data-ttu-id="577bf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="577bf-115">Requirement</span></span> | <span data-ttu-id="577bf-116">Value</span><span class="sxs-lookup"><span data-stu-id="577bf-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="577bf-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="577bf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="577bf-118">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="577bf-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="577bf-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="577bf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="577bf-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="577bf-120">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="577bf-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="577bf-121">Namespace</span></span><br/>                | <span data-ttu-id="577bf-122">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="577bf-122">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="577bf-123">MOF</span><span class="sxs-lookup"><span data-stu-id="577bf-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="577bf-124"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="577bf-124"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="577bf-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="577bf-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="577bf-126"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="577bf-126"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="577bf-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="577bf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="577bf-128">**Reinicio de MDM \_**</span><span class="sxs-lookup"><span data-stu-id="577bf-128">**MDM\_Reboot**</span></span>](mdm-reboot.md)
</dt> </dl>

 

