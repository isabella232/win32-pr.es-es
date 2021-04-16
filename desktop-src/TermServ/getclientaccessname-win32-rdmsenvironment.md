---
title: Método GetClientAccessName de la clase Win32_RDMSEnvironment
description: Recupera el nombre del registro de recursos (RR) del sistema de nombres de dominio (DNS) del entorno de Escritorio remoto Management Services (RDMS).
ms.assetid: 16f9d00d-a398-4a73-a641-ac552ba6a9d3
ms.tgt_platform: multiple
keywords:
- Método GetClientAccessName Servicios de Escritorio remoto
- Método GetClientAccessName Servicios de Escritorio remoto, clase Win32_RDMSEnvironment
- Win32_RDMSEnvironment de clase Servicios de Escritorio remoto, método GetClientAccessName
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54662cf1f27c53f3bf69398a203bfdfce1e53c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685870"
---
# <a name="getclientaccessname-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="3da51-106">Método GetClientAccessName de la \_ clase RDMSEnvironment de Win32</span><span class="sxs-lookup"><span data-stu-id="3da51-106">GetClientAccessName method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="3da51-107">Recupera el nombre del registro de recursos (RR) del sistema de nombres de dominio (DNS) del entorno de Escritorio remoto Management Services (RDMS).</span><span class="sxs-lookup"><span data-stu-id="3da51-107">Retrieves the Domain Name System (DNS) resource record (RR) name of the Remote Desktop Management Services (RDMS) environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="3da51-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3da51-108">Syntax</span></span>


```mof
uint32 GetClientAccessName(
  [out] string ClientAccessName
);
```



## <a name="parameters"></a><span data-ttu-id="3da51-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3da51-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3da51-110">*ClientAccessName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3da51-110">*ClientAccessName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3da51-111">Recibe el nombre de RR recuperado.</span><span class="sxs-lookup"><span data-stu-id="3da51-111">Receives the retrieved RR name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3da51-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3da51-112">Return value</span></span>

<span data-ttu-id="3da51-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="3da51-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3da51-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3da51-114">Requirements</span></span>



| <span data-ttu-id="3da51-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3da51-115">Requirement</span></span> | <span data-ttu-id="3da51-116">Value</span><span class="sxs-lookup"><span data-stu-id="3da51-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3da51-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3da51-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3da51-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3da51-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="3da51-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3da51-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3da51-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3da51-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="3da51-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3da51-121">Namespace</span></span><br/>                | <span data-ttu-id="3da51-122">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="3da51-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="3da51-123">MOF</span><span class="sxs-lookup"><span data-stu-id="3da51-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3da51-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3da51-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="3da51-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3da51-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3da51-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3da51-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="3da51-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3da51-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3da51-128">**Win32 \_ RDMSEnvironment**</span><span class="sxs-lookup"><span data-stu-id="3da51-128">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





