---
title: Método SetSMBPath de la clase Win32_RDMSDeploymentSettings
description: Actualiza la ruta de acceso UNC al recurso compartido de SMB en el que se implementan las máquinas virtuales de la colección de escritorios virtuales.
ms.assetid: 0b0b5b17-7b52-41e5-b9c6-c5f3e51c7853
ms.tgt_platform: multiple
keywords:
- Método SetSMBPath Servicios de Escritorio remoto
- Método SetSMBPath Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método SetSMBPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetSMBPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40598a3217ff1ca7c6082b3af09097352962309
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996672"
---
# <a name="setsmbpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="70a50-106">Método SetSMBPath de la \_ clase RDMSDeploymentSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="70a50-106">SetSMBPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="70a50-107">Actualiza la ruta de acceso UNC al recurso compartido de SMB en el que se implementan las máquinas virtuales de la colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="70a50-107">Updates the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="70a50-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70a50-108">Syntax</span></span>


```mof
uint32 SetSMBPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="70a50-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="70a50-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70a50-110">*DirectoryPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="70a50-110">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70a50-111">La nueva ruta de acceso al recurso compartido de SMB, en formato UNC.</span><span class="sxs-lookup"><span data-stu-id="70a50-111">The new path to the SMB share, in UNC format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70a50-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70a50-112">Return value</span></span>

<span data-ttu-id="70a50-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="70a50-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="70a50-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70a50-114">Requirements</span></span>



| <span data-ttu-id="70a50-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="70a50-115">Requirement</span></span> | <span data-ttu-id="70a50-116">Value</span><span class="sxs-lookup"><span data-stu-id="70a50-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="70a50-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70a50-117">Minimum supported client</span></span><br/> | <span data-ttu-id="70a50-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="70a50-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="70a50-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70a50-119">Minimum supported server</span></span><br/> | <span data-ttu-id="70a50-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="70a50-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="70a50-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="70a50-121">Namespace</span></span><br/>                | <span data-ttu-id="70a50-122">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="70a50-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="70a50-123">MOF</span><span class="sxs-lookup"><span data-stu-id="70a50-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70a50-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70a50-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="70a50-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="70a50-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70a50-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70a50-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="70a50-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="70a50-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70a50-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="70a50-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





