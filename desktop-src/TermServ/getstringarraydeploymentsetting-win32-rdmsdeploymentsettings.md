---
title: Método GetStringArrayDeploymentSetting de la clase Win32_RDMSDeploymentSettings
description: Recupera la configuración de implementación de una colección de escritorios virtuales.
ms.assetid: ab380618-560e-425b-9bf0-a7de6b30d01a
ms.tgt_platform: multiple
keywords:
- Método GetStringArrayDeploymentSetting Servicios de Escritorio remoto
- Método GetStringArrayDeploymentSetting Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método GetStringArrayDeploymentSetting
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetStringArrayDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ac0b82441abef8af1b4f6c8e3bd48b89a8cb6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150038"
---
# <a name="getstringarraydeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="079b1-106">Método GetStringArrayDeploymentSetting de la \_ clase RDMSDeploymentSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="079b1-106">GetStringArrayDeploymentSetting method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="079b1-107">Recupera la configuración de implementación de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="079b1-107">Retrieves the deployment settings for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="079b1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="079b1-108">Syntax</span></span>


```mof
uint32 GetStringArrayDeploymentSetting(
  [in]  string Key,
  [out] string Value[]
);
```



## <a name="parameters"></a><span data-ttu-id="079b1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="079b1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="079b1-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="079b1-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="079b1-111">El alias de la colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="079b1-111">The alias of the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="079b1-112">*Valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="079b1-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="079b1-113">Recibe una matriz de cadenas que contiene los valores de implementación.</span><span class="sxs-lookup"><span data-stu-id="079b1-113">Receives an array of strings that contains the deployment settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="079b1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="079b1-114">Requirements</span></span>



| <span data-ttu-id="079b1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="079b1-115">Requirement</span></span> | <span data-ttu-id="079b1-116">Value</span><span class="sxs-lookup"><span data-stu-id="079b1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="079b1-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="079b1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="079b1-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="079b1-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="079b1-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="079b1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="079b1-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="079b1-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="079b1-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="079b1-121">Namespace</span></span><br/>                | <span data-ttu-id="079b1-122">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="079b1-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="079b1-123">MOF</span><span class="sxs-lookup"><span data-stu-id="079b1-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="079b1-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="079b1-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="079b1-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="079b1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="079b1-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="079b1-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="079b1-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="079b1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="079b1-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="079b1-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





