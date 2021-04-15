---
title: Método ProvisioningJobGetReport de la clase Win32_RDMSVirtualDesktopCollection
description: Obtiene un informe sobre el estado de un trabajo de aprovisionamiento de escritorio virtual.
ms.assetid: 8fc03fed-0838-4530-9b0f-0f561d76769d
ms.tgt_platform: multiple
keywords:
- Método ProvisioningJobGetReport Servicios de Escritorio remoto
- Método ProvisioningJobGetReport Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de clase Servicios de Escritorio remoto, método ProvisioningJobGetReport
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobGetReport
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6605402c6ed6c0269b9971922bdefd48f265c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676809"
---
# <a name="provisioningjobgetreport-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="1a65a-106">Método ProvisioningJobGetReport de la \_ clase RDMSVirtualDesktopCollection de Win32</span><span class="sxs-lookup"><span data-stu-id="1a65a-106">ProvisioningJobGetReport method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="1a65a-107">Obtiene un informe sobre el estado de un trabajo de aprovisionamiento de escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="1a65a-107">Gets a report about the status of a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a65a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a65a-108">Syntax</span></span>


```mof
uint32 ProvisioningJobGetReport(
  [in]  string JobGuid,
  [out] string JobReportXml
);
```



## <a name="parameters"></a><span data-ttu-id="1a65a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a65a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a65a-110">*JobGuid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1a65a-110">*JobGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a65a-111">**GUID** que identifica de forma única el trabajo de aprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="1a65a-111">The **GUID** that uniquely identifies the provisioning job.</span></span>

</dd> <dt>

<span data-ttu-id="1a65a-112">*JobReportXml* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1a65a-112">*JobReportXml* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a65a-113">Cadena que contiene el informe en formato XML.</span><span class="sxs-lookup"><span data-stu-id="1a65a-113">A string that contains the report in XML format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a65a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a65a-114">Return value</span></span>

<span data-ttu-id="1a65a-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="1a65a-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a65a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a65a-116">Requirements</span></span>



| <span data-ttu-id="1a65a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a65a-117">Requirement</span></span> | <span data-ttu-id="1a65a-118">Value</span><span class="sxs-lookup"><span data-stu-id="1a65a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a65a-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a65a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1a65a-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1a65a-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="1a65a-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a65a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1a65a-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1a65a-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="1a65a-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1a65a-123">Namespace</span></span><br/>                | <span data-ttu-id="1a65a-124">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="1a65a-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="1a65a-125">MOF</span><span class="sxs-lookup"><span data-stu-id="1a65a-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a65a-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a65a-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a65a-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1a65a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a65a-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a65a-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="1a65a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a65a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a65a-130">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="1a65a-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





