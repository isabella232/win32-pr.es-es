---
title: método doWipeMethod de la clase MDM_RemoteWipe
description: Desencadena el dispositivo para iniciar el borrado remoto.
ms.assetid: dc25dc09-6a74-4c08-b452-b1d83085bb41
keywords:
- método doWipeMethod
- método doWipeMethod, clase MDM_RemoteWipe
- Clase MDM_RemoteWipe, método doWipeMethod
topic_type:
- apiref
api_name:
- MDM_RemoteWipe.doWipeMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f31dcc9dde2fe51ca0d8677df8b27637edd06c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489178"
---
# <a name="dowipemethod-method-of-the-mdm_remotewipe-class"></a><span data-ttu-id="5f054-106">método doWipeMethod de la \_ clase RemoteWipe de MDM</span><span class="sxs-lookup"><span data-stu-id="5f054-106">doWipeMethod method of the MDM\_RemoteWipe class</span></span>

<span data-ttu-id="5f054-107">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="5f054-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5f054-108">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="5f054-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5f054-109">Desencadena el dispositivo para iniciar el borrado remoto.</span><span class="sxs-lookup"><span data-stu-id="5f054-109">Triggers the device to start the remote wipe.</span></span> <span data-ttu-id="5f054-110">Vea [también.](/windows/client-management/mdm/remotewipe-csp)</span><span class="sxs-lookup"><span data-stu-id="5f054-110">See also, [doWipe](/windows/client-management/mdm/remotewipe-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="5f054-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f054-111">Syntax</span></span>


```mof
uint32 doWipeMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="5f054-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f054-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f054-113">*parámetro* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5f054-113">*param* \[in\]</span></span>
<span data-ttu-id="5f054-114"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5f054-114"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="5f054-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f054-115">Requirements</span></span>



| <span data-ttu-id="5f054-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f054-116">Requirement</span></span> | <span data-ttu-id="5f054-117">Value</span><span class="sxs-lookup"><span data-stu-id="5f054-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f054-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f054-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5f054-119">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f054-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5f054-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f054-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5f054-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5f054-121">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5f054-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5f054-122">Namespace</span></span><br/>                | <span data-ttu-id="5f054-123">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="5f054-123">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="5f054-124">MOF</span><span class="sxs-lookup"><span data-stu-id="5f054-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f054-125"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f054-125"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f054-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5f054-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f054-127"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f054-127"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f054-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f054-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f054-129">**RemoteWipe de MDM \_**</span><span class="sxs-lookup"><span data-stu-id="5f054-129">**MDM\_RemoteWipe**</span></span>](mdm-remotewipe.md)
</dt> <dt>

[<span data-ttu-id="5f054-130">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="5f054-130">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

