---
title: Método SetActiveServer de la clase Win32_RDMSEnvironment
description: Establece el FQDN del entorno de los servicios de administración de Escritorio remoto (RDMS) en el nodo actual.
ms.assetid: ed7b71cf-c3a4-4d2f-856a-31332f94fac9
ms.tgt_platform: multiple
keywords:
- Método SetActiveServer Servicios de Escritorio remoto
- Método SetActiveServer Servicios de Escritorio remoto, clase Win32_RDMSEnvironment
- Win32_RDMSEnvironment de clase Servicios de Escritorio remoto, método SetActiveServer
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f11b378b15e271200c730691c3654fd10e80f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490312"
---
# <a name="setactiveserver-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="16eb0-106">Método SetActiveServer de la \_ clase RDMSEnvironment de Win32</span><span class="sxs-lookup"><span data-stu-id="16eb0-106">SetActiveServer method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="16eb0-107">Establece el FQDN del entorno de los servicios de administración de Escritorio remoto (RDMS) en el nodo actual.</span><span class="sxs-lookup"><span data-stu-id="16eb0-107">Sets the FQDN of the Remote Desktop Management Services (RDMS) environment to the current node.</span></span>

## <a name="syntax"></a><span data-ttu-id="16eb0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16eb0-108">Syntax</span></span>


```mof
uint32 SetActiveServer();
```



## <a name="parameters"></a><span data-ttu-id="16eb0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="16eb0-109">Parameters</span></span>

<span data-ttu-id="16eb0-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="16eb0-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="16eb0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16eb0-111">Return value</span></span>

<span data-ttu-id="16eb0-112">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="16eb0-112">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="16eb0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16eb0-113">Requirements</span></span>



| <span data-ttu-id="16eb0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="16eb0-114">Requirement</span></span> | <span data-ttu-id="16eb0-115">Value</span><span class="sxs-lookup"><span data-stu-id="16eb0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="16eb0-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16eb0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="16eb0-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="16eb0-117">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="16eb0-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16eb0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="16eb0-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="16eb0-119">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="16eb0-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="16eb0-120">Namespace</span></span><br/>                | <span data-ttu-id="16eb0-121">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="16eb0-121">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="16eb0-122">MOF</span><span class="sxs-lookup"><span data-stu-id="16eb0-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16eb0-123"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="16eb0-123"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="16eb0-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="16eb0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16eb0-125"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16eb0-125"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="16eb0-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="16eb0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16eb0-127">**Win32 \_ RDMSEnvironment**</span><span class="sxs-lookup"><span data-stu-id="16eb0-127">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





