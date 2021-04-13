---
title: Método GetStringProperty de la clase Win32_RDMSDeploymentSettings
description: Recupera una propiedad de cadena para la configuración de implementación de una colección de escritorios virtuales.
ms.assetid: 468ffdea-57a9-4478-adae-3629e4522762
ms.tgt_platform: multiple
keywords:
- Método GetStringProperty Servicios de Escritorio remoto
- Método GetStringProperty Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método GetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f26a570becbbae6b0d768c399acd3dd2954ecdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422147"
---
# <a name="getstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="151c8-106">Método GetStringProperty de la \_ clase RDMSDeploymentSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="151c8-106">GetStringProperty method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="151c8-107">Recupera una propiedad de cadena para la configuración de implementación de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="151c8-107">Retrieves a string property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="151c8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="151c8-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="151c8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="151c8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="151c8-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="151c8-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="151c8-111">El alias de la colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="151c8-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="151c8-112">*Valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="151c8-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="151c8-113">Cadena que recibe el valor recuperado.</span><span class="sxs-lookup"><span data-stu-id="151c8-113">A string that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="151c8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="151c8-114">Requirements</span></span>



| <span data-ttu-id="151c8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="151c8-115">Requirement</span></span> | <span data-ttu-id="151c8-116">Value</span><span class="sxs-lookup"><span data-stu-id="151c8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="151c8-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="151c8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="151c8-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="151c8-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="151c8-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="151c8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="151c8-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="151c8-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="151c8-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="151c8-121">Namespace</span></span><br/>                | <span data-ttu-id="151c8-122">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="151c8-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="151c8-123">MOF</span><span class="sxs-lookup"><span data-stu-id="151c8-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="151c8-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="151c8-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="151c8-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="151c8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="151c8-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="151c8-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="151c8-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="151c8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="151c8-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="151c8-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





