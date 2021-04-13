---
title: Método GetUserAssignment de la clase Win32_RDMSVirtualDesktop
description: Recupera el nombre de usuario y el nombre de dominio del usuario que está asignado al escritorio virtual.
ms.assetid: 1887c49d-85df-4fb4-9b40-42fb7763bf95
ms.tgt_platform: multiple
keywords:
- Método GetUserAssignment Servicios de Escritorio remoto
- Método GetUserAssignment Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop de clase Servicios de Escritorio remoto, método GetUserAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87293a471bb4f69b3f4c57de0f964fa0daa043cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422434"
---
# <a name="getuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="3bde0-106">Método GetUserAssignment de la \_ clase RDMSVirtualDesktop de Win32</span><span class="sxs-lookup"><span data-stu-id="3bde0-106">GetUserAssignment method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="3bde0-107">Recupera el nombre de usuario y el nombre de dominio del usuario que está asignado al escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="3bde0-107">Retrieves the username and domain name of the user that is assigned to the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bde0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3bde0-108">Syntax</span></span>


```mof
uint32 GetUserAssignment(
  [out] string UserName,
  [out] string UserDomain
);
```



## <a name="parameters"></a><span data-ttu-id="3bde0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3bde0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bde0-110">*Nombre de usuario* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3bde0-110">*UserName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3bde0-111">Recibe el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="3bde0-111">Receives the username.</span></span>

</dd> <dt>

<span data-ttu-id="3bde0-112">*UserDomain* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3bde0-112">*UserDomain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3bde0-113">Recibe el nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="3bde0-113">Receives the domain name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bde0-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3bde0-114">Return value</span></span>

<span data-ttu-id="3bde0-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="3bde0-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bde0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bde0-116">Requirements</span></span>



| <span data-ttu-id="3bde0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bde0-117">Requirement</span></span> | <span data-ttu-id="3bde0-118">Value</span><span class="sxs-lookup"><span data-stu-id="3bde0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bde0-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3bde0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3bde0-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3bde0-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="3bde0-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3bde0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3bde0-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3bde0-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="3bde0-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3bde0-123">Namespace</span></span><br/>                | <span data-ttu-id="3bde0-124">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="3bde0-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="3bde0-125">MOF</span><span class="sxs-lookup"><span data-stu-id="3bde0-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3bde0-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3bde0-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="3bde0-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3bde0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bde0-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bde0-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="3bde0-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="3bde0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bde0-130">**Win32 \_ RDMSVirtualDesktop**</span><span class="sxs-lookup"><span data-stu-id="3bde0-130">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





