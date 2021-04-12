---
title: Método GetActiveServer de la clase Win32_RDMSEnvironment
description: Recupera el nombre de dominio completo (FQDN) del entorno de servicios de administración de Escritorio remoto (RDMS).
ms.assetid: 87e25d11-de1d-41d1-974d-2871dde444b5
ms.tgt_platform: multiple
keywords:
- Método GetActiveServer Servicios de Escritorio remoto
- Método GetActiveServer Servicios de Escritorio remoto, clase Win32_RDMSEnvironment
- Win32_RDMSEnvironment de clase Servicios de Escritorio remoto, método GetActiveServer
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4265315e3ed2de87e564adab87c023401bbd55e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491350"
---
# <a name="getactiveserver-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="d92b6-106">Método GetActiveServer de la \_ clase RDMSEnvironment de Win32</span><span class="sxs-lookup"><span data-stu-id="d92b6-106">GetActiveServer method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="d92b6-107">Recupera el nombre de dominio completo (FQDN) del entorno de servicios de administración de Escritorio remoto (RDMS).</span><span class="sxs-lookup"><span data-stu-id="d92b6-107">Retrieves the fully qualified domain name (FQDN) of the Remote Desktop Management Services (RDMS) environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="d92b6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d92b6-108">Syntax</span></span>


```mof
uint32 GetActiveServer(
  [out] string ServerName
);
```



## <a name="parameters"></a><span data-ttu-id="d92b6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d92b6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d92b6-110">*NombreDeServidor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d92b6-110">*ServerName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d92b6-111">Recibe el FQDN recuperado.</span><span class="sxs-lookup"><span data-stu-id="d92b6-111">Receives the retrieved FQDN.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d92b6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d92b6-112">Return value</span></span>

<span data-ttu-id="d92b6-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="d92b6-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d92b6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d92b6-114">Requirements</span></span>



| <span data-ttu-id="d92b6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d92b6-115">Requirement</span></span> | <span data-ttu-id="d92b6-116">Value</span><span class="sxs-lookup"><span data-stu-id="d92b6-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d92b6-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d92b6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d92b6-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d92b6-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="d92b6-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d92b6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d92b6-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d92b6-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="d92b6-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d92b6-121">Namespace</span></span><br/>                | <span data-ttu-id="d92b6-122">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="d92b6-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="d92b6-123">MOF</span><span class="sxs-lookup"><span data-stu-id="d92b6-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d92b6-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d92b6-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="d92b6-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d92b6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d92b6-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d92b6-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="d92b6-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d92b6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d92b6-128">**Win32 \_ RDMSEnvironment**</span><span class="sxs-lookup"><span data-stu-id="d92b6-128">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





