---
title: Método SetExportPath de la clase Win32_RDMSDeploymentSettings
description: Actualiza la ruta de acceso al directorio en el que se implementan las máquinas virtuales para una colección de escritorios virtuales.
ms.assetid: e52b79c8-6724-4264-93d5-4a2a14c89b6b
ms.tgt_platform: multiple
keywords:
- Método SetExportPath Servicios de Escritorio remoto
- Método SetExportPath Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método SetExportPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetExportPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32dbc844aecf86d4c62fada6c5cd68d514a69272
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676729"
---
# <a name="setexportpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="2ffbb-106">Método SetExportPath de la \_ clase RDMSDeploymentSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="2ffbb-106">SetExportPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="2ffbb-107">Actualiza la ruta de acceso al directorio en el que se implementan las máquinas virtuales para una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="2ffbb-107">Updates the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ffbb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ffbb-108">Syntax</span></span>


```mof
uint32 SetExportPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="2ffbb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ffbb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ffbb-110">*DirectoryPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ffbb-110">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ffbb-111">Nueva ruta de acceso al directorio.</span><span class="sxs-lookup"><span data-stu-id="2ffbb-111">The new directory path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ffbb-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ffbb-112">Return value</span></span>

<span data-ttu-id="2ffbb-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="2ffbb-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ffbb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ffbb-114">Requirements</span></span>



| <span data-ttu-id="2ffbb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ffbb-115">Requirement</span></span> | <span data-ttu-id="2ffbb-116">Value</span><span class="sxs-lookup"><span data-stu-id="2ffbb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ffbb-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ffbb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2ffbb-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2ffbb-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="2ffbb-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ffbb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2ffbb-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2ffbb-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="2ffbb-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2ffbb-121">Namespace</span></span><br/>                | <span data-ttu-id="2ffbb-122">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="2ffbb-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="2ffbb-123">MOF</span><span class="sxs-lookup"><span data-stu-id="2ffbb-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ffbb-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ffbb-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ffbb-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2ffbb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ffbb-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ffbb-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="2ffbb-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ffbb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ffbb-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="2ffbb-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





