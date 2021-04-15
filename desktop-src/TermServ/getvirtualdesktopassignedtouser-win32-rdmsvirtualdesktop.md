---
title: Método GetVirtualDesktopAssignedToUser de la clase Win32_RDMSVirtualDesktop
description: Recupera el escritorio virtual asignado al usuario especificado.
ms.assetid: cbc22c45-4492-4651-b164-a6fd717c5ab4
ms.tgt_platform: multiple
keywords:
- Método GetVirtualDesktopAssignedToUser Servicios de Escritorio remoto
- Método GetVirtualDesktopAssignedToUser Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop de clase Servicios de Escritorio remoto, método GetVirtualDesktopAssignedToUser
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopAssignedToUser
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcbbbed20b6b571e8867689ac901344af8e23b93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676599"
---
# <a name="getvirtualdesktopassignedtouser-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="e39c8-106">Método GetVirtualDesktopAssignedToUser de la \_ clase RDMSVirtualDesktop de Win32</span><span class="sxs-lookup"><span data-stu-id="e39c8-106">GetVirtualDesktopAssignedToUser method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="e39c8-107">Recupera el escritorio virtual asignado al usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="e39c8-107">Retrieves the virtual desktop that is assigned to the specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="e39c8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e39c8-108">Syntax</span></span>


```mof
uint32 GetVirtualDesktopAssignedToUser(
  [in]  string CollectionAlias,
  [in]  string UserName,
  [in]  string UserDomain,
  [out] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="e39c8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e39c8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e39c8-110">*CollectionAlias* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e39c8-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e39c8-111">El alias de la colección de escritorios virtuales que contiene el escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="e39c8-111">The alias of the virtual desktop collection that contain the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="e39c8-112">*Nombre de usuario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e39c8-112">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e39c8-113">Nombre de usuario del usuario.</span><span class="sxs-lookup"><span data-stu-id="e39c8-113">The username of the user.</span></span>

</dd> <dt>

<span data-ttu-id="e39c8-114">*UserDomain* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e39c8-114">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e39c8-115">El nombre de dominio del usuario.</span><span class="sxs-lookup"><span data-stu-id="e39c8-115">The domain name of the user.</span></span>

</dd> <dt>

<span data-ttu-id="e39c8-116">*VMName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e39c8-116">*VMName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e39c8-117">Recibe el nombre de la máquina virtual del escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="e39c8-117">Receives the virtual machine name of the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e39c8-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e39c8-118">Return value</span></span>

<span data-ttu-id="e39c8-119">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="e39c8-119">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e39c8-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e39c8-120">Requirements</span></span>



| <span data-ttu-id="e39c8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e39c8-121">Requirement</span></span> | <span data-ttu-id="e39c8-122">Value</span><span class="sxs-lookup"><span data-stu-id="e39c8-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e39c8-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e39c8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e39c8-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e39c8-124">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="e39c8-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e39c8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e39c8-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e39c8-126">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="e39c8-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e39c8-127">Namespace</span></span><br/>                | <span data-ttu-id="e39c8-128">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="e39c8-128">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="e39c8-129">MOF</span><span class="sxs-lookup"><span data-stu-id="e39c8-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e39c8-130"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e39c8-130"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="e39c8-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e39c8-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e39c8-132"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e39c8-132"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="e39c8-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="e39c8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e39c8-134">**Win32 \_ RDMSVirtualDesktop**</span><span class="sxs-lookup"><span data-stu-id="e39c8-134">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





