---
title: Método SetSecondaryConnectionString de la clase Win32_RDMSDeploymentSettings
description: Establece la cadena de conexión secundaria de base de datos de nivel de implementación.
ms.assetid: 154c495e-564e-4d90-a4ff-de683d41aa73
ms.tgt_platform: multiple
keywords:
- Método SetSecondaryConnectionString Servicios de Escritorio remoto
- Método SetSecondaryConnectionString Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método SetSecondaryConnectionString
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetSecondaryConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8060a6f2676b5599bf44672e79ebf48e64e354
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801976"
---
# <a name="setsecondaryconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="d6185-106">Método SetSecondaryConnectionString de la \_ clase RDMSDeploymentSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="d6185-106">SetSecondaryConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="d6185-107">Establece la cadena de conexión secundaria de base de datos de nivel de implementación.</span><span class="sxs-lookup"><span data-stu-id="d6185-107">Sets the deployment level database secondary connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6185-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6185-108">Syntax</span></span>


```mof
uint32 SetSecondaryConnectionString(
  [in] string SecondaryConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="d6185-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d6185-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6185-110">*SecondaryConnectionString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d6185-110">*SecondaryConnectionString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6185-111">Cadena de conexión que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="d6185-111">The connection string to set</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6185-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d6185-112">Return value</span></span>

<span data-ttu-id="d6185-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="d6185-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6185-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6185-114">Requirements</span></span>



| <span data-ttu-id="d6185-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6185-115">Requirement</span></span> | <span data-ttu-id="d6185-116">Value</span><span class="sxs-lookup"><span data-stu-id="d6185-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6185-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6185-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d6185-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d6185-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="d6185-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6185-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d6185-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d6185-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="d6185-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d6185-121">Namespace</span></span><br/>                | <span data-ttu-id="d6185-122">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="d6185-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="d6185-123">MOF</span><span class="sxs-lookup"><span data-stu-id="d6185-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6185-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6185-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6185-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d6185-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6185-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6185-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="d6185-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6185-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6185-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="d6185-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





