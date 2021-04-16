---
title: Método ProvisioningJobCancel de la clase Win32_RDMSVirtualDesktopCollection
description: Cancela un trabajo de aprovisionamiento de escritorio virtual.
ms.assetid: 933ea0f3-b916-4e70-89de-597f9eb23976
ms.tgt_platform: multiple
keywords:
- Método ProvisioningJobCancel Servicios de Escritorio remoto
- Método ProvisioningJobCancel Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de clase Servicios de Escritorio remoto, método ProvisioningJobCancel
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobCancel
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f414bcdc264d682817898bae98fcf60a716452
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676810"
---
# <a name="provisioningjobcancel-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="293ac-106">Método ProvisioningJobCancel de la \_ clase RDMSVirtualDesktopCollection de Win32</span><span class="sxs-lookup"><span data-stu-id="293ac-106">ProvisioningJobCancel method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="293ac-107">Cancela un trabajo de aprovisionamiento de escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="293ac-107">Cancels a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="293ac-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="293ac-108">Syntax</span></span>


```mof
uint32 ProvisioningJobCancel(
  [in] string JobGuid
);
```



## <a name="parameters"></a><span data-ttu-id="293ac-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="293ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="293ac-110">*JobGuid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="293ac-110">*JobGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="293ac-111">**GUID** que identifica de forma única el trabajo de aprovisionamiento que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="293ac-111">The **GUID** that uniquely identifies the provisioning job to cancel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="293ac-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="293ac-112">Return value</span></span>

<span data-ttu-id="293ac-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="293ac-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="293ac-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="293ac-114">Requirements</span></span>



| <span data-ttu-id="293ac-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="293ac-115">Requirement</span></span> | <span data-ttu-id="293ac-116">Value</span><span class="sxs-lookup"><span data-stu-id="293ac-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="293ac-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="293ac-117">Minimum supported client</span></span><br/> | <span data-ttu-id="293ac-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="293ac-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="293ac-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="293ac-119">Minimum supported server</span></span><br/> | <span data-ttu-id="293ac-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="293ac-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="293ac-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="293ac-121">Namespace</span></span><br/>                | <span data-ttu-id="293ac-122">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="293ac-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="293ac-123">MOF</span><span class="sxs-lookup"><span data-stu-id="293ac-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="293ac-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="293ac-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="293ac-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="293ac-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="293ac-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="293ac-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="293ac-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="293ac-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="293ac-128">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="293ac-128">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





