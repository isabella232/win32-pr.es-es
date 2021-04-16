---
title: Método GetInt32Property de la clase Win32_RDMSDeploymentSettings (Microsoft. Diagnostics. appanalysis. h)
description: Recupera una propiedad de entero para la configuración de implementación de una colección de escritorios virtuales.
ms.assetid: 6b8174bb-ffb7-4699-a3fb-d32ab0b202fc
ms.tgt_platform: multiple
keywords:
- Método GetInt32Property Servicios de Escritorio remoto
- Método GetInt32Property Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f96374c610084c8ef7973d4ac4db603d9c28cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686038"
---
# <a name="getint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="599e0-106">Método GetInt32Property de la \_ clase RDMSDeploymentSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="599e0-106">GetInt32Property method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="599e0-107">Recupera una propiedad de entero para la configuración de implementación de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="599e0-107">Retrieves an integer property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="599e0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="599e0-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="599e0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="599e0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="599e0-110">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="599e0-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="599e0-111">El alias de la colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="599e0-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="599e0-112">*Valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="599e0-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="599e0-113">Entero que recibe el valor recuperado.</span><span class="sxs-lookup"><span data-stu-id="599e0-113">An integer that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="599e0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="599e0-114">Requirements</span></span>



| <span data-ttu-id="599e0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="599e0-115">Requirement</span></span> | <span data-ttu-id="599e0-116">Value</span><span class="sxs-lookup"><span data-stu-id="599e0-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="599e0-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="599e0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="599e0-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="599e0-118">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="599e0-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="599e0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="599e0-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="599e0-120">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="599e0-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="599e0-121">Namespace</span></span><br/>                | <span data-ttu-id="599e0-122">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="599e0-122">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="599e0-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="599e0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="599e0-124"><dt>Microsoft. Diagnostics. appanalysis. h</dt></span><span class="sxs-lookup"><span data-stu-id="599e0-124"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="599e0-125">MOF</span><span class="sxs-lookup"><span data-stu-id="599e0-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="599e0-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="599e0-126"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="599e0-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="599e0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="599e0-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="599e0-128"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="599e0-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="599e0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="599e0-130">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="599e0-130">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





