---
description: Concede acceso a la sesión interactiva de la máquina virtual a la lista de confianzas especificada.
ms.assetid: 8a82170d-067b-47e5-a15f-21d6c04128d2
title: Método GrantInteractiveSessionAccess de la clase Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.GrantInteractiveSessionAccess
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b8bd49805b5fdc5545a81e4f0b816fe35a6c37b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687335"
---
# <a name="grantinteractivesessionaccess-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="57403-103">Método GrantInteractiveSessionAccess de la \_ clase TerminalService de MSVM</span><span class="sxs-lookup"><span data-stu-id="57403-103">GrantInteractiveSessionAccess method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="57403-104">Concede acceso a la sesión interactiva de la máquina virtual a la lista de confianzas especificada.</span><span class="sxs-lookup"><span data-stu-id="57403-104">Grants access to the interactive session of the virtual machine to the specified list of trustees.</span></span>

## <a name="syntax"></a><span data-ttu-id="57403-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57403-105">Syntax</span></span>


```mof
uint32 GrantInteractiveSessionAccess(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 Trustees[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="57403-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57403-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57403-107">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="57403-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57403-108">Una referencia a una instancia de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa la máquina virtual a la que se concederá el acceso.</span><span class="sxs-lookup"><span data-stu-id="57403-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to which access will be granted.</span></span>

</dd> <dt>

<span data-ttu-id="57403-109">*Confianzas* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="57403-109">*Trustees* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57403-110">Matriz de cadenas, cada una de las cuales identifica un administrador de confianza al que se concederá acceso a la sesión interactiva de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="57403-110">An array of strings, each identifying a trustee that will be granted access to the interactive session of the virtual machine.</span></span> <span data-ttu-id="57403-111">Los identificadores de confianza deben especificarse en formato compatible con SAM de Windows o en formato de cadena de SID de Windows.</span><span class="sxs-lookup"><span data-stu-id="57403-111">The trustee identifiers should be specified in Windows SAM-compatible format or Windows SID string format.</span></span>

</dd> <dt>

<span data-ttu-id="57403-112">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="57403-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57403-113">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="57403-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57403-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57403-114">Return value</span></span>

<span data-ttu-id="57403-115">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="57403-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="57403-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="57403-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="57403-117">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="57403-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="57403-118">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="57403-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="57403-119">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="57403-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="57403-120">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="57403-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="57403-121">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="57403-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="57403-122">**Parámetros incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="57403-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="57403-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="57403-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="57403-124">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="57403-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="57403-125">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="57403-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="57403-126">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="57403-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="57403-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57403-127">Requirements</span></span>



| <span data-ttu-id="57403-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="57403-128">Requirement</span></span> | <span data-ttu-id="57403-129">Value</span><span class="sxs-lookup"><span data-stu-id="57403-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57403-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57403-130">Minimum supported client</span></span><br/> | <span data-ttu-id="57403-131">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="57403-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="57403-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57403-132">Minimum supported server</span></span><br/> | <span data-ttu-id="57403-133">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="57403-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="57403-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="57403-134">Namespace</span></span><br/>                | <span data-ttu-id="57403-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="57403-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="57403-136">MOF</span><span class="sxs-lookup"><span data-stu-id="57403-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57403-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="57403-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="57403-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="57403-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57403-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="57403-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="57403-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="57403-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57403-141">**MSVM \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="57403-141">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

