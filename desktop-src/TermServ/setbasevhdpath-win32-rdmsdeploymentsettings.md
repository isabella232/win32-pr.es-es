---
title: Método SetBaseVHDPath de la clase Win32_RDMSDeploymentSettings
description: Recupera la ruta de acceso base al directorio en el que se implementan los VHD de la colección de escritorios virtuales. | Método SetBaseVHDPath de la clase Win32_RDMSDeploymentSettings
ms.assetid: 1ea4cd93-ef17-4ec9-82f9-382c549f189c
ms.tgt_platform: multiple
keywords:
- Método SetBaseVHDPath Servicios de Escritorio remoto
- Método SetBaseVHDPath Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método SetBaseVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetBaseVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7907640a9641cff3c94475318bf499415b25184
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678679"
---
# <a name="setbasevhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="cd942-107">Método SetBaseVHDPath de la \_ clase RDMSDeploymentSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="cd942-107">SetBaseVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="cd942-108">Recupera la ruta de acceso base al directorio en el que se implementan los VHD de la colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="cd942-108">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd942-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd942-109">Syntax</span></span>


```mof
uint32 SetBaseVHDPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="cd942-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd942-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd942-111">*DirectoryPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cd942-111">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd942-112">La nueva ruta de implementación de VHD.</span><span class="sxs-lookup"><span data-stu-id="cd942-112">The new VHD deployment path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd942-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd942-113">Return value</span></span>

<span data-ttu-id="cd942-114">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="cd942-114">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd942-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd942-115">Requirements</span></span>



| <span data-ttu-id="cd942-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd942-116">Requirement</span></span> | <span data-ttu-id="cd942-117">Value</span><span class="sxs-lookup"><span data-stu-id="cd942-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd942-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd942-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cd942-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cd942-119">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="cd942-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd942-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cd942-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd942-121">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="cd942-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cd942-122">Namespace</span></span><br/>                | <span data-ttu-id="cd942-123">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="cd942-123">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="cd942-124">MOF</span><span class="sxs-lookup"><span data-stu-id="cd942-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd942-125"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd942-125"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd942-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cd942-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd942-127"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd942-127"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="cd942-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd942-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd942-129">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="cd942-129">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





