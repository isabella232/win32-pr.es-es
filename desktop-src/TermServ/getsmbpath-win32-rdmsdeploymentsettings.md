---
title: Método GetSMBPath de la clase Win32_RDMSDeploymentSettings
description: Recupera la ruta de acceso UNC al recurso compartido de SMB en el que se implementan las máquinas virtuales de la colección de escritorios virtuales.
ms.assetid: 0a5d3c11-6a77-48f7-a3ea-6f82725ff01f
ms.tgt_platform: multiple
keywords:
- Método GetSMBPath Servicios de Escritorio remoto
- Método GetSMBPath Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método GetSMBPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetSMBPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1738faf82a6405018495dd762ba9585daa3e1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422629"
---
# <a name="getsmbpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="9b851-106">Método GetSMBPath de la \_ clase RDMSDeploymentSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="9b851-106">GetSMBPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="9b851-107">Recupera la ruta de acceso UNC al recurso compartido de SMB en el que se implementan las máquinas virtuales de la colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="9b851-107">Retrieves the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b851-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b851-108">Syntax</span></span>


```mof
uint32 GetSMBPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="9b851-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b851-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b851-110">*DirectoryPath* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9b851-110">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b851-111">Recibe una ruta de acceso con formato UNC al recurso compartido de SMB.</span><span class="sxs-lookup"><span data-stu-id="9b851-111">Receives a UNC formatted path to the SMB share.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b851-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b851-112">Return value</span></span>

<span data-ttu-id="9b851-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="9b851-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b851-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b851-114">Requirements</span></span>



| <span data-ttu-id="9b851-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b851-115">Requirement</span></span> | <span data-ttu-id="9b851-116">Value</span><span class="sxs-lookup"><span data-stu-id="9b851-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b851-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b851-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9b851-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9b851-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="9b851-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b851-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9b851-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9b851-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="9b851-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9b851-121">Namespace</span></span><br/>                | <span data-ttu-id="9b851-122">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="9b851-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="9b851-123">MOF</span><span class="sxs-lookup"><span data-stu-id="9b851-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b851-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b851-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b851-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9b851-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b851-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b851-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="9b851-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b851-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b851-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="9b851-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





