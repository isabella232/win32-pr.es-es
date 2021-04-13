---
title: Método ChangeProductKeyMethod de la clase MDM_WindowsLicensing
description: Este método instala una clave de producto para dispositivos de escritorio de Windows 10. No reinicie el punto. Vea también ChangeProductKey.
ms.assetid: 1d9e3243-2ca4-427b-bda2-d33e1e70c80d
keywords:
- Método ChangeProductKeyMethod
- Método ChangeProductKeyMethod, clase MDM_WindowsLicensing
- Clase MDM_WindowsLicensing, método ChangeProductKeyMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.ChangeProductKeyMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e00345fb0e23655b457e0540c70289a169c54ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491938"
---
# <a name="changeproductkeymethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="80ae7-108">Método ChangeProductKeyMethod de la \_ clase WindowsLicensing de MDM</span><span class="sxs-lookup"><span data-stu-id="80ae7-108">ChangeProductKeyMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="80ae7-109">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="80ae7-109">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="80ae7-110">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="80ae7-110">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="80ae7-111">Este método instala una clave de producto para dispositivos de escritorio de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="80ae7-111">This method installs a product key for Windows 10 desktop devices.</span></span> <span data-ttu-id="80ae7-112">No reinicie el punto.</span><span class="sxs-lookup"><span data-stu-id="80ae7-112">Dot not reboot.</span></span> <span data-ttu-id="80ae7-113">Vea también [ChangeProductKey](/windows/client-management/mdm/windowslicensing-csp)</span><span class="sxs-lookup"><span data-stu-id="80ae7-113">See also [ChangeProductKey](/windows/client-management/mdm/windowslicensing-csp)</span></span>

## <a name="syntax"></a><span data-ttu-id="80ae7-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80ae7-114">Syntax</span></span>


```mof
uint32 ChangeProductKeyMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="80ae7-115">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80ae7-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80ae7-116">*parámetro* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="80ae7-116">*param* \[in\]</span></span>
<span data-ttu-id="80ae7-117"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="80ae7-117"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="80ae7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80ae7-118">Requirements</span></span>



| <span data-ttu-id="80ae7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="80ae7-119">Requirement</span></span> | <span data-ttu-id="80ae7-120">Value</span><span class="sxs-lookup"><span data-stu-id="80ae7-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80ae7-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80ae7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="80ae7-122">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="80ae7-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="80ae7-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80ae7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="80ae7-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="80ae7-124">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="80ae7-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="80ae7-125">Namespace</span></span><br/>                | <span data-ttu-id="80ae7-126">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="80ae7-126">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="80ae7-127">MOF</span><span class="sxs-lookup"><span data-stu-id="80ae7-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80ae7-128"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80ae7-128"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="80ae7-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="80ae7-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80ae7-130"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80ae7-130"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80ae7-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="80ae7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80ae7-132">**WindowsLicensing de MDM \_**</span><span class="sxs-lookup"><span data-stu-id="80ae7-132">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> </dl>

 

