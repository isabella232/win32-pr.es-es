---
title: Método SetDiffVHDPath de la clase Win32_RDMSDeploymentSettings
description: Actualiza la ruta de acceso al directorio en la que se implementan los discos de diferenciación para una colección de escritorios virtuales.
ms.assetid: 665ffbf9-0250-4956-9bce-f5a6714b47e4
ms.tgt_platform: multiple
keywords:
- Método SetDiffVHDPath Servicios de Escritorio remoto
- Método SetDiffVHDPath Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método SetDiffVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetDiffVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e52d206c9e0cbff19f26e38a2a02f04ea0acc03d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422264"
---
# <a name="setdiffvhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="59b4c-106">Método SetDiffVHDPath de la \_ clase RDMSDeploymentSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="59b4c-106">SetDiffVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="59b4c-107">Actualiza la ruta de acceso al directorio en la que se implementan los discos de diferenciación para una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="59b4c-107">Updates the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="59b4c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59b4c-108">Syntax</span></span>


```mof
uint32 SetDiffVHDPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="59b4c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59b4c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59b4c-110">*DirectoryPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="59b4c-110">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59b4c-111">Nueva ruta de acceso al disco de diferenciación.</span><span class="sxs-lookup"><span data-stu-id="59b4c-111">The new differencing disk path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59b4c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59b4c-112">Return value</span></span>

<span data-ttu-id="59b4c-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="59b4c-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="59b4c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59b4c-114">Requirements</span></span>



| <span data-ttu-id="59b4c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="59b4c-115">Requirement</span></span> | <span data-ttu-id="59b4c-116">Value</span><span class="sxs-lookup"><span data-stu-id="59b4c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="59b4c-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59b4c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="59b4c-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="59b4c-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="59b4c-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59b4c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="59b4c-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="59b4c-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="59b4c-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="59b4c-121">Namespace</span></span><br/>                | <span data-ttu-id="59b4c-122">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="59b4c-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="59b4c-123">MOF</span><span class="sxs-lookup"><span data-stu-id="59b4c-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59b4c-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59b4c-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="59b4c-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="59b4c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59b4c-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59b4c-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="59b4c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="59b4c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59b4c-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="59b4c-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





