---
title: Método GetSecondaryConnectionString de la clase Win32_RDMSDeploymentSettings
description: Recupera la cadena de conexión secundaria de base de datos de nivel de implementación, que se puede usar para admitir la expiración de contraseña.
ms.assetid: 0de02752-6cbf-4c21-b752-a57ed58aeef1
ms.tgt_platform: multiple
keywords:
- Método GetSecondaryConnectionString Servicios de Escritorio remoto
- Método GetSecondaryConnectionString Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método GetSecondaryConnectionString
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetSecondaryConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2c09f4fcacabbe928fcda00447e252077bd8a51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359726"
---
# <a name="getsecondaryconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="336b0-106">Método GetSecondaryConnectionString de la \_ clase RDMSDeploymentSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="336b0-106">GetSecondaryConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="336b0-107">Recupera la cadena de conexión secundaria de base de datos de nivel de implementación, que se puede usar para admitir la expiración de contraseña.</span><span class="sxs-lookup"><span data-stu-id="336b0-107">Retrieves the deployment-level database secondary connection string, which may be used to support password expiration.</span></span>

## <a name="syntax"></a><span data-ttu-id="336b0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="336b0-108">Syntax</span></span>


```mof
uint32 GetSecondaryConnectionString(
  [out] string SecondaryConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="336b0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="336b0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="336b0-110">*SecondaryConnectionString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="336b0-110">*SecondaryConnectionString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="336b0-111">Cadena de conexión que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="336b0-111">The connection string to retrieve</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="336b0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="336b0-112">Return value</span></span>

<span data-ttu-id="336b0-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="336b0-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="336b0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="336b0-114">Requirements</span></span>



| <span data-ttu-id="336b0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="336b0-115">Requirement</span></span> | <span data-ttu-id="336b0-116">Value</span><span class="sxs-lookup"><span data-stu-id="336b0-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="336b0-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="336b0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="336b0-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="336b0-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="336b0-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="336b0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="336b0-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="336b0-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="336b0-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="336b0-121">Namespace</span></span><br/>                | <span data-ttu-id="336b0-122">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="336b0-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="336b0-123">MOF</span><span class="sxs-lookup"><span data-stu-id="336b0-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="336b0-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="336b0-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="336b0-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="336b0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="336b0-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="336b0-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="336b0-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="336b0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="336b0-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="336b0-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





