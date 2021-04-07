---
title: Método GetBaseVHDPath de la clase Win32_RDMSDeploymentSettings
description: Recupera la ruta de acceso base al directorio en el que se implementan los VHD de la colección de escritorios virtuales. | Método GetBaseVHDPath de la clase Win32_RDMSDeploymentSettings
ms.assetid: d3629a08-ef16-4aab-b74b-f837a8ba00d0
ms.tgt_platform: multiple
keywords:
- Método GetBaseVHDPath Servicios de Escritorio remoto
- Método GetBaseVHDPath Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método GetBaseVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetBaseVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 595c6459148a0270bed2328c70e15ef74a69acf3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003615"
---
# <a name="getbasevhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="6ac7f-107">Método GetBaseVHDPath de la \_ clase RDMSDeploymentSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="6ac7f-107">GetBaseVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="6ac7f-108">Recupera la ruta de acceso base al directorio en el que se implementan los VHD de la colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="6ac7f-108">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ac7f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ac7f-109">Syntax</span></span>


```mof
uint32 GetBaseVHDPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="6ac7f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ac7f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ac7f-111">*DirectoryPath* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6ac7f-111">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac7f-112">Recibe la ruta de acceso de implementación de VHD.</span><span class="sxs-lookup"><span data-stu-id="6ac7f-112">Receives the VHD deployment path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ac7f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ac7f-113">Return value</span></span>

<span data-ttu-id="6ac7f-114">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="6ac7f-114">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ac7f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ac7f-115">Requirements</span></span>



| <span data-ttu-id="6ac7f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ac7f-116">Requirement</span></span> | <span data-ttu-id="6ac7f-117">Value</span><span class="sxs-lookup"><span data-stu-id="6ac7f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ac7f-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ac7f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6ac7f-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6ac7f-119">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="6ac7f-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ac7f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6ac7f-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6ac7f-121">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="6ac7f-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6ac7f-122">Namespace</span></span><br/>                | <span data-ttu-id="6ac7f-123">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="6ac7f-123">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="6ac7f-124">MOF</span><span class="sxs-lookup"><span data-stu-id="6ac7f-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ac7f-125"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ac7f-125"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ac7f-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6ac7f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ac7f-127"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ac7f-127"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="6ac7f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ac7f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ac7f-129">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="6ac7f-129">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





