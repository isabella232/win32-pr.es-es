---
description: Recupera la lista de control de acceso discrecional (DACL) actual que controla el acceso a la sesión interactiva de una máquina virtual.
ms.assetid: 9b81f6d5-20fa-4277-b943-756d85359fd2
title: Método GetInteractiveSessionACL de la clase Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.GetInteractiveSessionACL
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f08c8514a2f65a08b4b9350b38988da8e49b4985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810327"
---
# <a name="getinteractivesessionacl-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="9c289-103">Método GetInteractiveSessionACL de la \_ clase TerminalService de MSVM</span><span class="sxs-lookup"><span data-stu-id="9c289-103">GetInteractiveSessionACL method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="9c289-104">Recupera la lista de *control de acceso discrecional* (DACL) actual que controla el acceso a la sesión interactiva de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9c289-104">Retrieves the current *discretionary access control list* (DACL) that controls access to the interactive session of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c289-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c289-105">Syntax</span></span>


```mof
uint32 GetInteractiveSessionACL(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 AccessControlList[]
);
```



## <a name="parameters"></a><span data-ttu-id="9c289-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c289-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c289-107">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9c289-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c289-108">Una referencia a una instancia de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa la máquina virtual cuya DACL se recuperará.</span><span class="sxs-lookup"><span data-stu-id="9c289-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine whose DACL will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="9c289-109">*AccessControlList* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9c289-109">*AccessControlList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c289-110">Matriz de cadenas, cada una de las cuales contiene una instancia incrustada de la clase [**MSVM \_ InteractiveSessionACE**](msvm-interactivesessionace.md) que representa una *entrada de control de acceso* (ACE) en la DACL de la sesión interactiva de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9c289-110">An array of strings, each containing an embedded instance of the [**Msvm\_InteractiveSessionACE**](msvm-interactivesessionace.md) class that represents an *access control entry* (ACE) in the virtual machine interactive session DACL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c289-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c289-111">Return value</span></span>

<span data-ttu-id="9c289-112">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="9c289-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9c289-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="9c289-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9c289-114">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="9c289-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9c289-115">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="9c289-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9c289-116">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="9c289-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9c289-117">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="9c289-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9c289-118">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="9c289-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9c289-119">**Parámetros incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="9c289-119">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9c289-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9c289-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9c289-121">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="9c289-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9c289-122">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="9c289-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="9c289-123">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="9c289-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9c289-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c289-124">Requirements</span></span>



| <span data-ttu-id="9c289-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c289-125">Requirement</span></span> | <span data-ttu-id="9c289-126">Value</span><span class="sxs-lookup"><span data-stu-id="9c289-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c289-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c289-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9c289-128">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c289-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9c289-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c289-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9c289-130">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c289-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9c289-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9c289-131">Namespace</span></span><br/>                | <span data-ttu-id="9c289-132">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="9c289-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9c289-133">MOF</span><span class="sxs-lookup"><span data-stu-id="9c289-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c289-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c289-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c289-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9c289-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c289-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9c289-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9c289-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c289-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c289-138">**MSVM \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="9c289-138">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

 




