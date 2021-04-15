---
title: Método ProvisioningJobExecute de la clase Win32_RDMSVirtualDesktopCollection
description: Ejecuta un trabajo de aprovisionamiento de escritorio virtual.
ms.assetid: 69f0cc6a-7eef-4cd9-94ac-f0c7e52d02d8
ms.tgt_platform: multiple
keywords:
- Método ProvisioningJobExecute Servicios de Escritorio remoto
- Método ProvisioningJobExecute Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de clase Servicios de Escritorio remoto, método ProvisioningJobExecute
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobExecute
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c632a6bdc5fc5c4a128941d8a6c8b4379ddf9629
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492761"
---
# <a name="provisioningjobexecute-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="05aed-106">Método ProvisioningJobExecute de la \_ clase RDMSVirtualDesktopCollection de Win32</span><span class="sxs-lookup"><span data-stu-id="05aed-106">ProvisioningJobExecute method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="05aed-107">Ejecuta un trabajo de aprovisionamiento de escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="05aed-107">Runs a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="05aed-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05aed-108">Syntax</span></span>


```mof
uint32 ProvisioningJobExecute(
  [in]  string JobInputXml,
  [out] string JobGuid
);
```



## <a name="parameters"></a><span data-ttu-id="05aed-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05aed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05aed-110">*JobInputXml* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="05aed-110">*JobInputXml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05aed-111">Cadena que contiene la información de aprovisionamiento en formato XML.</span><span class="sxs-lookup"><span data-stu-id="05aed-111">A string that contains the provisioning information in XML format.</span></span>

</dd> <dt>

<span data-ttu-id="05aed-112">*JobGuid* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="05aed-112">*JobGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05aed-113">**GUID** que identifica de forma única el trabajo de aprovisionamiento que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="05aed-113">The **GUID** that uniquely identifies the provisioning job to run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05aed-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05aed-114">Return value</span></span>

<span data-ttu-id="05aed-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="05aed-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="05aed-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05aed-116">Requirements</span></span>



| <span data-ttu-id="05aed-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="05aed-117">Requirement</span></span> | <span data-ttu-id="05aed-118">Value</span><span class="sxs-lookup"><span data-stu-id="05aed-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="05aed-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05aed-119">Minimum supported client</span></span><br/> | <span data-ttu-id="05aed-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="05aed-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="05aed-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05aed-121">Minimum supported server</span></span><br/> | <span data-ttu-id="05aed-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="05aed-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="05aed-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="05aed-123">Namespace</span></span><br/>                | <span data-ttu-id="05aed-124">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="05aed-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="05aed-125">MOF</span><span class="sxs-lookup"><span data-stu-id="05aed-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05aed-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="05aed-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="05aed-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="05aed-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05aed-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05aed-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="05aed-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="05aed-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05aed-130">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="05aed-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





