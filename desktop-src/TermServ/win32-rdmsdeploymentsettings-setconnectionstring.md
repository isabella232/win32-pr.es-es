---
title: Método SetConnectionString de la clase Win32_RDMSDeploymentSettings
description: Establece la cadena de conexión de base de datos de nivel de implementación.
ms.assetid: c8902ab9-72a6-4d69-ab22-f6074205deb4
ms.tgt_platform: multiple
keywords:
- Método SetConnectionString Servicios de Escritorio remoto
- Método SetConnectionString Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método SetConnectionString
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ccb3f618f6a08dcb95bb7dc04c1494be6a7b5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422207"
---
# <a name="setconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="b70cd-106">Método SetConnectionString de la \_ clase RDMSDeploymentSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="b70cd-106">SetConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="b70cd-107">Establece la cadena de conexión de base de datos de nivel de implementación.</span><span class="sxs-lookup"><span data-stu-id="b70cd-107">Sets the deployment-level database connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="b70cd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b70cd-108">Syntax</span></span>


```mof
uint32 SetConnectionString(
  [in] string ConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="b70cd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b70cd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b70cd-110">*ConnectionString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b70cd-110">*ConnectionString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b70cd-111">Cadena de conexión que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="b70cd-111">The connection string to set</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b70cd-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b70cd-112">Return value</span></span>

<span data-ttu-id="b70cd-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="b70cd-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b70cd-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b70cd-114">Requirements</span></span>



| <span data-ttu-id="b70cd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b70cd-115">Requirement</span></span> | <span data-ttu-id="b70cd-116">Value</span><span class="sxs-lookup"><span data-stu-id="b70cd-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b70cd-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b70cd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b70cd-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b70cd-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="b70cd-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b70cd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b70cd-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b70cd-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="b70cd-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b70cd-121">Namespace</span></span><br/>                | <span data-ttu-id="b70cd-122">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="b70cd-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="b70cd-123">MOF</span><span class="sxs-lookup"><span data-stu-id="b70cd-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b70cd-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="b70cd-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b70cd-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b70cd-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="b70cd-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b70cd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b70cd-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="b70cd-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





