---
title: Método RemoveDesktopAssignment de la clase Win32_RDMSDesktopAssignment
description: Quita una asignación de escritorio.
ms.assetid: e1a8cf03-1d21-4bf4-a868-3da4d5bbf43b
ms.tgt_platform: multiple
keywords:
- Método RemoveDesktopAssignment Servicios de Escritorio remoto
- Método RemoveDesktopAssignment Servicios de Escritorio remoto, clase Win32_RDMSDesktopAssignment
- Win32_RDMSDesktopAssignment de clase Servicios de Escritorio remoto, método RemoveDesktopAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.RemoveDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6645a79efc970cf7c3288d0765e9aac8cac68a89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686200"
---
# <a name="removedesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a><span data-ttu-id="f0d04-106">Método RemoveDesktopAssignment de la \_ clase RDMSDesktopAssignment de Win32</span><span class="sxs-lookup"><span data-stu-id="f0d04-106">RemoveDesktopAssignment method of the Win32\_RDMSDesktopAssignment class</span></span>

<span data-ttu-id="f0d04-107">Quita una asignación de escritorio</span><span class="sxs-lookup"><span data-stu-id="f0d04-107">Removes a desktop assignment</span></span>

## <a name="syntax"></a><span data-ttu-id="f0d04-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0d04-108">Syntax</span></span>


```mof
uint32 RemoveDesktopAssignment(
  [in] string CollectionAlias,
  [in] string DesktopName,
  [in] string UserDomain,
  [in] string UserName
);
```



## <a name="parameters"></a><span data-ttu-id="f0d04-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0d04-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0d04-110">*CollectionAlias* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0d04-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0d04-111">El alias de la colección.</span><span class="sxs-lookup"><span data-stu-id="f0d04-111">The collection alias.</span></span>

</dd> <dt>

<span data-ttu-id="f0d04-112">*DesktopName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0d04-112">*DesktopName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0d04-113">Nombre del escritorio.</span><span class="sxs-lookup"><span data-stu-id="f0d04-113">The name of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="f0d04-114">*UserDomain* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0d04-114">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0d04-115">El nombre de dominio de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="f0d04-115">The user account domain name.</span></span>

</dd> <dt>

<span data-ttu-id="f0d04-116">*Nombre de usuario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0d04-116">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0d04-117">El nombre de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="f0d04-117">The user account name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0d04-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0d04-118">Requirements</span></span>



| <span data-ttu-id="f0d04-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0d04-119">Requirement</span></span> | <span data-ttu-id="f0d04-120">Value</span><span class="sxs-lookup"><span data-stu-id="f0d04-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0d04-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0d04-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f0d04-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f0d04-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="f0d04-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0d04-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f0d04-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f0d04-124">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="f0d04-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f0d04-125">Namespace</span></span><br/>                | <span data-ttu-id="f0d04-126">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="f0d04-126">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="f0d04-127">MOF</span><span class="sxs-lookup"><span data-stu-id="f0d04-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0d04-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0d04-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0d04-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f0d04-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0d04-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0d04-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="f0d04-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0d04-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0d04-132">**Win32 \_ RDMSDesktopAssignment**</span><span class="sxs-lookup"><span data-stu-id="f0d04-132">**Win32\_RDMSDesktopAssignment**</span></span>](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 





