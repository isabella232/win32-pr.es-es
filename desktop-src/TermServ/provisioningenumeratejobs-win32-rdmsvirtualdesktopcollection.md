---
title: Método ProvisioningEnumerateJobs de la clase Win32_RDMSVirtualDesktopCollection
description: Enumera los trabajos de aprovisionamiento de escritorio virtual para este servicio.
ms.assetid: 4bd2b03f-ba8c-483e-af09-270424f9b1ed
ms.tgt_platform: multiple
keywords:
- Método ProvisioningEnumerateJobs Servicios de Escritorio remoto
- Método ProvisioningEnumerateJobs Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de clase Servicios de Escritorio remoto, método ProvisioningEnumerateJobs
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningEnumerateJobs
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa2b54a0599c2bbcaf6b0f9a9acb3ab3028389b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535385"
---
# <a name="provisioningenumeratejobs-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="1189f-106">Método ProvisioningEnumerateJobs de la \_ clase RDMSVirtualDesktopCollection de Win32</span><span class="sxs-lookup"><span data-stu-id="1189f-106">ProvisioningEnumerateJobs method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="1189f-107">Enumera los trabajos de aprovisionamiento de escritorio virtual para este servicio.</span><span class="sxs-lookup"><span data-stu-id="1189f-107">Enumerates virtual desktop provisioning jobs for this service.</span></span>

## <a name="syntax"></a><span data-ttu-id="1189f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1189f-108">Syntax</span></span>


```mof
uint32 ProvisioningEnumerateJobs(
  [in]  uint32 JobType,
  [in]  string CollectionAlias,
  [out] string JobGuids[]
);
```



## <a name="parameters"></a><span data-ttu-id="1189f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1189f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1189f-110">*JobType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1189f-110">*JobType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1189f-111">Entero que especifica el tipo de trabajo que se va a enumerar.</span><span class="sxs-lookup"><span data-stu-id="1189f-111">An integer that specifies the type of job to enumerate.</span></span>

<span data-ttu-id="1189f-112">Este parámetro se puede establecer en uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="1189f-112">This parameter can be set to one of the following values:</span></span>

<dt>

<span data-ttu-id="1189f-113">0</span><span class="sxs-lookup"><span data-stu-id="1189f-113">0</span></span>
</dt> <dd>

<span data-ttu-id="1189f-114">Trabajos en ejecución</span><span class="sxs-lookup"><span data-stu-id="1189f-114">Running jobs</span></span>

</dd> <dt>

<span data-ttu-id="1189f-115">1</span><span class="sxs-lookup"><span data-stu-id="1189f-115">1</span></span>
</dt> <dd>

<span data-ttu-id="1189f-116">Trabajos completados</span><span class="sxs-lookup"><span data-stu-id="1189f-116">Completed jobs</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1189f-117">*CollectionAlias* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1189f-117">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1189f-118">El alias de la colección de escritorios virtuales que se va a enumerar.</span><span class="sxs-lookup"><span data-stu-id="1189f-118">The alias of the virtual desktop collection to enumerate.</span></span> <span data-ttu-id="1189f-119">El valor predeterminado de este parámetro es FALSE, que especifica que se deben enumerar todos los trabajos en ejecución.</span><span class="sxs-lookup"><span data-stu-id="1189f-119">The default value for this parameter is FALSE, which specifies that all running jobs are to be enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="1189f-120">*JobGuids* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1189f-120">*JobGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1189f-121">Una matriz que contiene los **GUID** de los trabajos de aprovisionamiento que se van a enumerar.</span><span class="sxs-lookup"><span data-stu-id="1189f-121">An array that contains the **GUIDs** of provisioning jobs to enumerate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1189f-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1189f-122">Return value</span></span>

<span data-ttu-id="1189f-123">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="1189f-123">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1189f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1189f-124">Requirements</span></span>



| <span data-ttu-id="1189f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1189f-125">Requirement</span></span> | <span data-ttu-id="1189f-126">Value</span><span class="sxs-lookup"><span data-stu-id="1189f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1189f-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1189f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1189f-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1189f-128">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="1189f-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1189f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1189f-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1189f-130">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="1189f-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1189f-131">Namespace</span></span><br/>                | <span data-ttu-id="1189f-132">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="1189f-132">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="1189f-133">MOF</span><span class="sxs-lookup"><span data-stu-id="1189f-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1189f-134"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1189f-134"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="1189f-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1189f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1189f-136"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1189f-136"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="1189f-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="1189f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1189f-138">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="1189f-138">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





