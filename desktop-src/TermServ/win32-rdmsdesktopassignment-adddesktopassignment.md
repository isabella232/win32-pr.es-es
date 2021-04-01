---
title: Método AddDesktopAssignment de la clase Win32_RDMSDesktopAssignment
description: Agregar una asignación de escritorio.
ms.assetid: 3690f70e-d0c3-444a-a0b7-cec6994eb3b8
ms.tgt_platform: multiple
keywords:
- Método AddDesktopAssignment Servicios de Escritorio remoto
- Método AddDesktopAssignment Servicios de Escritorio remoto, clase Win32_RDMSDesktopAssignment
- Win32_RDMSDesktopAssignment de clase Servicios de Escritorio remoto, método AddDesktopAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.AddDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 571273e76b0bb45b748f1587e5a831fcf1e36b0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905157"
---
# <a name="adddesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a><span data-ttu-id="e7fb2-106">Método AddDesktopAssignment de la \_ clase RDMSDesktopAssignment de Win32</span><span class="sxs-lookup"><span data-stu-id="e7fb2-106">AddDesktopAssignment method of the Win32\_RDMSDesktopAssignment class</span></span>

<span data-ttu-id="e7fb2-107">Agregar una asignación de escritorio</span><span class="sxs-lookup"><span data-stu-id="e7fb2-107">Add a desktop assignment</span></span>

## <a name="syntax"></a><span data-ttu-id="e7fb2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7fb2-108">Syntax</span></span>


```mof
uint32 AddDesktopAssignment(
  [in] string CollectionAlias,
  [in] string DesktopName,
  [in] string UserDomain,
  [in] string UserName
);
```



## <a name="parameters"></a><span data-ttu-id="e7fb2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7fb2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7fb2-110">*CollectionAlias* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e7fb2-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7fb2-111">El alias de la colección.</span><span class="sxs-lookup"><span data-stu-id="e7fb2-111">The collection alias.</span></span>

</dd> <dt>

<span data-ttu-id="e7fb2-112">*DesktopName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e7fb2-112">*DesktopName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7fb2-113">Nombre del escritorio.</span><span class="sxs-lookup"><span data-stu-id="e7fb2-113">The name of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="e7fb2-114">*UserDomain* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e7fb2-114">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7fb2-115">El nombre de dominio de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="e7fb2-115">The user account domain name.</span></span>

</dd> <dt>

<span data-ttu-id="e7fb2-116">*Nombre de usuario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e7fb2-116">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7fb2-117">El nombre de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="e7fb2-117">The user account name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7fb2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7fb2-118">Requirements</span></span>



| <span data-ttu-id="e7fb2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7fb2-119">Requirement</span></span> | <span data-ttu-id="e7fb2-120">Value</span><span class="sxs-lookup"><span data-stu-id="e7fb2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7fb2-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7fb2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e7fb2-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e7fb2-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="e7fb2-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7fb2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e7fb2-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e7fb2-124">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="e7fb2-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e7fb2-125">Namespace</span></span><br/>                | <span data-ttu-id="e7fb2-126">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="e7fb2-126">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="e7fb2-127">MOF</span><span class="sxs-lookup"><span data-stu-id="e7fb2-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7fb2-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7fb2-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7fb2-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e7fb2-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7fb2-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7fb2-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="e7fb2-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7fb2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7fb2-132">**Win32 \_ RDMSDesktopAssignment**</span><span class="sxs-lookup"><span data-stu-id="e7fb2-132">**Win32\_RDMSDesktopAssignment**</span></span>](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 





