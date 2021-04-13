---
title: Método GetDiffVHDPath de la clase Win32_RDMSDeploymentSettings
description: Recupera la ruta de acceso al directorio en la que se implementan los discos de diferenciación para una colección de escritorios virtuales.
ms.assetid: 4340c817-2276-48a1-a856-b4c9e91ea981
ms.tgt_platform: multiple
keywords:
- Método GetDiffVHDPath Servicios de Escritorio remoto
- Método GetDiffVHDPath Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método GetDiffVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetDiffVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7391315013cf8487d93b32f645933d14f06db2d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422011"
---
# <a name="getdiffvhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="6730a-106">Método GetDiffVHDPath de la \_ clase RDMSDeploymentSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="6730a-106">GetDiffVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="6730a-107">Recupera la ruta de acceso al directorio en la que se implementan los discos de diferenciación para una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="6730a-107">Retrieves the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6730a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6730a-108">Syntax</span></span>


```mof
uint32 GetDiffVHDPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="6730a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6730a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6730a-110">*DirectoryPath* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6730a-110">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6730a-111">Recibe la nueva ruta de acceso del disco de diferenciación.</span><span class="sxs-lookup"><span data-stu-id="6730a-111">Receives the new differencing disk path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6730a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6730a-112">Return value</span></span>

<span data-ttu-id="6730a-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="6730a-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6730a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6730a-114">Requirements</span></span>



| <span data-ttu-id="6730a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6730a-115">Requirement</span></span> | <span data-ttu-id="6730a-116">Value</span><span class="sxs-lookup"><span data-stu-id="6730a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6730a-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6730a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6730a-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6730a-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="6730a-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6730a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6730a-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6730a-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="6730a-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6730a-121">Namespace</span></span><br/>                | <span data-ttu-id="6730a-122">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="6730a-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="6730a-123">MOF</span><span class="sxs-lookup"><span data-stu-id="6730a-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6730a-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6730a-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="6730a-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6730a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6730a-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6730a-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="6730a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="6730a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6730a-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="6730a-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





