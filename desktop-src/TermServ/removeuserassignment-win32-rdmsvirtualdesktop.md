---
title: Método RemoveUserAssignment de la clase Win32_RDMSVirtualDesktop
description: Quita la asignación de usuario del escritorio virtual.
ms.assetid: 7ebb34b4-94f6-4a00-87a9-44ad28d103cb
ms.tgt_platform: multiple
keywords:
- Método RemoveUserAssignment Servicios de Escritorio remoto
- Método RemoveUserAssignment Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop de clase Servicios de Escritorio remoto, método RemoveUserAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.RemoveUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01675c777603f0eab2d22c0136b1ef6cc3522b7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686014"
---
# <a name="removeuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="55571-106">Método RemoveUserAssignment de la \_ clase RDMSVirtualDesktop de Win32</span><span class="sxs-lookup"><span data-stu-id="55571-106">RemoveUserAssignment method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="55571-107">Quita la asignación de usuario del escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="55571-107">Removes the user assignment from the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="55571-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55571-108">Syntax</span></span>


```mof
uint32 RemoveUserAssignment(
  [in] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="55571-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55571-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55571-110">*VMName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="55571-110">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55571-111">El nombre de la máquina virtual del escritorio virtual.</span><span class="sxs-lookup"><span data-stu-id="55571-111">The virtual machine name of the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55571-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55571-112">Return value</span></span>

<span data-ttu-id="55571-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="55571-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="55571-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55571-114">Requirements</span></span>



| <span data-ttu-id="55571-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="55571-115">Requirement</span></span> | <span data-ttu-id="55571-116">Value</span><span class="sxs-lookup"><span data-stu-id="55571-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="55571-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55571-117">Minimum supported client</span></span><br/> | <span data-ttu-id="55571-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="55571-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="55571-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55571-119">Minimum supported server</span></span><br/> | <span data-ttu-id="55571-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="55571-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="55571-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="55571-121">Namespace</span></span><br/>                | <span data-ttu-id="55571-122">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="55571-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="55571-123">MOF</span><span class="sxs-lookup"><span data-stu-id="55571-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55571-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55571-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="55571-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="55571-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55571-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55571-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="55571-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="55571-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55571-128">**Win32 \_ RDMSVirtualDesktop**</span><span class="sxs-lookup"><span data-stu-id="55571-128">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





