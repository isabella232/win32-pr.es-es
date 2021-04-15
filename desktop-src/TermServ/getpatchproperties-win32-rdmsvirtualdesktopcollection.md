---
title: Método GetPatchProperties de la clase Win32_RDMSVirtualDesktopCollection
description: Recupera las propiedades de un trabajo de aprovisionamiento de actualizaciones de software para las máquinas virtuales de una colección de escritorios virtuales.
ms.assetid: 9f228d89-0613-49c7-8169-48491c3a2d9b
ms.tgt_platform: multiple
keywords:
- Método GetPatchProperties Servicios de Escritorio remoto
- Método GetPatchProperties Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de clase Servicios de Escritorio remoto, método GetPatchProperties
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetPatchProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f0ca45c97512818aa5f8a9ea851d18fa5554c32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534570"
---
# <a name="getpatchproperties-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="51390-106">Método GetPatchProperties de la \_ clase RDMSVirtualDesktopCollection de Win32</span><span class="sxs-lookup"><span data-stu-id="51390-106">GetPatchProperties method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="51390-107">Recupera las propiedades de un trabajo de aprovisionamiento de actualizaciones de software para las máquinas virtuales de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="51390-107">Retrieves the properties of a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="51390-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51390-108">Syntax</span></span>


```mof
uint32 GetPatchProperties(
  [out] DATETIME StartTime,
  [out] DATETIME ForceLogOffTime,
  [out] string   JobGuid,
  [out] uint32   State
);
```



## <a name="parameters"></a><span data-ttu-id="51390-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51390-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51390-110">*StartTime* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="51390-110">*StartTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51390-111">Fecha y hora de instalación de las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="51390-111">The date and time to install the updates.</span></span>

</dd> <dt>

<span data-ttu-id="51390-112">*ForceLogOffTime* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="51390-112">*ForceLogOffTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51390-113">Fecha y hora en que el sistema cerrará la sesión de los usuarios de las máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="51390-113">The date and time on which the system will log off users of the virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="51390-114">*JobGuid* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="51390-114">*JobGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51390-115">**GUID** que identifica de forma única el trabajo de aprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="51390-115">A **GUID** that uniquely identifies the provisioning job.</span></span>

</dd> <dt>

<span data-ttu-id="51390-116">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="51390-116">*State* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51390-117">Estado del trabajo de aprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="51390-117">The state of the provisioning job.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51390-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51390-118">Return value</span></span>

<span data-ttu-id="51390-119">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="51390-119">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="51390-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51390-120">Requirements</span></span>



| <span data-ttu-id="51390-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="51390-121">Requirement</span></span> | <span data-ttu-id="51390-122">Value</span><span class="sxs-lookup"><span data-stu-id="51390-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="51390-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51390-123">Minimum supported client</span></span><br/> | <span data-ttu-id="51390-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="51390-124">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="51390-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51390-125">Minimum supported server</span></span><br/> | <span data-ttu-id="51390-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="51390-126">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="51390-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="51390-127">Namespace</span></span><br/>                | <span data-ttu-id="51390-128">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="51390-128">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="51390-129">MOF</span><span class="sxs-lookup"><span data-stu-id="51390-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51390-130"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51390-130"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="51390-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="51390-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51390-132"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51390-132"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="51390-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="51390-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51390-134">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="51390-134">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





