---
title: Método RemoveDeploymentSetting de la clase Win32_RDMSDeploymentSettings
description: Elimina la configuración de implementación de una colección de escritorios virtuales.
ms.assetid: 68e102a3-8f3f-4997-bdf0-c2ae3640ed42
ms.tgt_platform: multiple
keywords:
- Método RemoveDeploymentSetting Servicios de Escritorio remoto
- Método RemoveDeploymentSetting Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método RemoveDeploymentSetting
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.RemoveDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 336b93f86d6b96074341dde4851813b26eb66fe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905611"
---
# <a name="removedeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="a9031-106">Método RemoveDeploymentSetting de la \_ clase RDMSDeploymentSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="a9031-106">RemoveDeploymentSetting method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="a9031-107">Elimina la configuración de implementación de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="a9031-107">Deletes the deployment settings for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9031-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9031-108">Syntax</span></span>


```mof
uint32 RemoveDeploymentSetting(
  [in] string Key
);
```



## <a name="parameters"></a><span data-ttu-id="a9031-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a9031-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9031-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a9031-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9031-111">El alias de la colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="a9031-111">The alias of the virtual desktop collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a9031-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9031-112">Requirements</span></span>



| <span data-ttu-id="a9031-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9031-113">Requirement</span></span> | <span data-ttu-id="a9031-114">Value</span><span class="sxs-lookup"><span data-stu-id="a9031-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9031-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9031-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a9031-116">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a9031-116">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="a9031-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9031-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a9031-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a9031-118">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="a9031-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a9031-119">Namespace</span></span><br/>                | <span data-ttu-id="a9031-120">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="a9031-120">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="a9031-121">MOF</span><span class="sxs-lookup"><span data-stu-id="a9031-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9031-122"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9031-122"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9031-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a9031-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9031-124"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9031-124"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="a9031-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9031-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9031-126">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="a9031-126">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





