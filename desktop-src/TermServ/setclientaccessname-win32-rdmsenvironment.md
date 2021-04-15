---
title: Método SetClientAccessName de la clase Win32_RDMSEnvironment
description: Actualiza el nombre del registro de recursos (RR) del sistema de nombres de dominio (DNS) de un entorno de Escritorio remoto Management Services (RDMS).
ms.assetid: bbce3fc1-d2c5-4874-bdd0-be27fb5981d1
ms.tgt_platform: multiple
keywords:
- Método SetClientAccessName Servicios de Escritorio remoto
- Método SetClientAccessName Servicios de Escritorio remoto, clase Win32_RDMSEnvironment
- Win32_RDMSEnvironment de clase Servicios de Escritorio remoto, método SetClientAccessName
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13f9087fe2c2139833baeb21bc62da508c6e5989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676966"
---
# <a name="setclientaccessname-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="8722e-106">Método SetClientAccessName de la \_ clase RDMSEnvironment de Win32</span><span class="sxs-lookup"><span data-stu-id="8722e-106">SetClientAccessName method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="8722e-107">Actualiza el nombre del registro de recursos (RR) del sistema de nombres de dominio (DNS) de un entorno de Escritorio remoto Management Services (RDMS).</span><span class="sxs-lookup"><span data-stu-id="8722e-107">Updates the Domain Name System (DNS) resource record (RR) name of an Remote Desktop Management Services (RDMS) environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="8722e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8722e-108">Syntax</span></span>


```mof
uint32 SetClientAccessName(
  [in] string ClientAccessName
);
```



## <a name="parameters"></a><span data-ttu-id="8722e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8722e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8722e-110">*ClientAccessName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8722e-110">*ClientAccessName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8722e-111">Nombre del nuevo RR.</span><span class="sxs-lookup"><span data-stu-id="8722e-111">The new RR name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8722e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8722e-112">Return value</span></span>

<span data-ttu-id="8722e-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="8722e-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8722e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8722e-114">Requirements</span></span>



| <span data-ttu-id="8722e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8722e-115">Requirement</span></span> | <span data-ttu-id="8722e-116">Value</span><span class="sxs-lookup"><span data-stu-id="8722e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8722e-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8722e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8722e-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8722e-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="8722e-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8722e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8722e-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8722e-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="8722e-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8722e-121">Namespace</span></span><br/>                | <span data-ttu-id="8722e-122">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="8722e-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="8722e-123">MOF</span><span class="sxs-lookup"><span data-stu-id="8722e-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8722e-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8722e-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="8722e-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8722e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8722e-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8722e-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="8722e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="8722e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8722e-128">**Win32 \_ RDMSEnvironment**</span><span class="sxs-lookup"><span data-stu-id="8722e-128">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





