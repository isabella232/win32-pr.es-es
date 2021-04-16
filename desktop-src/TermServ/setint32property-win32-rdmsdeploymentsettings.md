---
title: Método SetInt32Property de la clase Win32_RDMSDeploymentSettings
description: Actualiza una propiedad de entero para la configuración de implementación de una colección de escritorios virtuales.
ms.assetid: c5e6dbd5-7db7-4409-bf53-c2680e4a5319
ms.tgt_platform: multiple
keywords:
- Método SetInt32Property Servicios de Escritorio remoto
- Método SetInt32Property Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fecdc42031514d5219fc03172b951602ad021ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686165"
---
# <a name="setint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="cc616-106">Método SetInt32Property de la \_ clase RDMSDeploymentSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="cc616-106">SetInt32Property method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="cc616-107">Actualiza una propiedad de entero para la configuración de implementación de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="cc616-107">Updates an integer property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc616-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc616-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="cc616-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc616-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc616-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="cc616-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc616-111">El alias de la colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="cc616-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="cc616-112">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="cc616-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc616-113">Nuevo valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cc616-113">The new property value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc616-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc616-114">Requirements</span></span>



| <span data-ttu-id="cc616-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc616-115">Requirement</span></span> | <span data-ttu-id="cc616-116">Value</span><span class="sxs-lookup"><span data-stu-id="cc616-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc616-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc616-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cc616-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cc616-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="cc616-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc616-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cc616-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cc616-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="cc616-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cc616-121">Namespace</span></span><br/>                | <span data-ttu-id="cc616-122">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="cc616-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="cc616-123">MOF</span><span class="sxs-lookup"><span data-stu-id="cc616-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc616-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc616-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="cc616-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cc616-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc616-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc616-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="cc616-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc616-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc616-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="cc616-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





