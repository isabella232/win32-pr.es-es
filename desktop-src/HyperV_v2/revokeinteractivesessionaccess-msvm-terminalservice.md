---
description: Revoca el acceso a la sesión interactiva de la máquina virtual a partir de la lista de confianzas especificada.
ms.assetid: c6d3df04-c31e-404a-9a04-3e8653bdc14f
title: Método RevokeInteractiveSessionAccess de la clase Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.RevokeInteractiveSessionAccess
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ab92f375f082d3af1f04b3fe52db5cb7964e3d4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813691"
---
# <a name="revokeinteractivesessionaccess-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="64214-103">Método RevokeInteractiveSessionAccess de la \_ clase TerminalService de MSVM</span><span class="sxs-lookup"><span data-stu-id="64214-103">RevokeInteractiveSessionAccess method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="64214-104">Revoca el acceso a la sesión interactiva de la máquina virtual a partir de la lista de confianzas especificada.</span><span class="sxs-lookup"><span data-stu-id="64214-104">Revokes access to the interactive session of the virtual machine from the specified list of trustees.</span></span>

## <a name="syntax"></a><span data-ttu-id="64214-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64214-105">Syntax</span></span>


```mof
uint32 RevokeInteractiveSessionAccess(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 Trustees[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="64214-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="64214-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64214-107">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="64214-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64214-108">Una referencia a una instancia de la clase de [**\_ ComputerSystem de CIM**](cim-computersystem.md) que representa la máquina virtual a la que se revocará el acceso.</span><span class="sxs-lookup"><span data-stu-id="64214-108">A reference to an instance of the [**CIM\_ComputerSystem**](cim-computersystem.md) class that represents the virtual machine to which access will be revoked.</span></span>

</dd> <dt>

<span data-ttu-id="64214-109">*Confianzas* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="64214-109">*Trustees* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64214-110">Matriz de cadenas, cada una de las cuales identifica un administrador de confianza cuyos derechos de acceso se revocarán.</span><span class="sxs-lookup"><span data-stu-id="64214-110">An array of strings, each identifying a trustee whose access rights will be revoked.</span></span> <span data-ttu-id="64214-111">Los identificadores de confianza deben especificarse en formato compatible con SAM de Windows o en formato de cadena de SID de Windows.</span><span class="sxs-lookup"><span data-stu-id="64214-111">The trustee identifiers should be specified in Windows SAM-compatible format or Windows SID string format.</span></span>

</dd> <dt>

<span data-ttu-id="64214-112">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="64214-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64214-113">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="64214-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64214-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64214-114">Return value</span></span>

<span data-ttu-id="64214-115">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="64214-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="64214-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="64214-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="64214-117">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="64214-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="64214-118">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="64214-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="64214-119">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="64214-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="64214-120">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="64214-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="64214-121">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="64214-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="64214-122">**Parámetros incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="64214-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="64214-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="64214-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="64214-124">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="64214-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="64214-125">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="64214-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="64214-126">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="64214-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="64214-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64214-127">Requirements</span></span>



| <span data-ttu-id="64214-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="64214-128">Requirement</span></span> | <span data-ttu-id="64214-129">Value</span><span class="sxs-lookup"><span data-stu-id="64214-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64214-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64214-130">Minimum supported client</span></span><br/> | <span data-ttu-id="64214-131">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="64214-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="64214-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64214-132">Minimum supported server</span></span><br/> | <span data-ttu-id="64214-133">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="64214-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="64214-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="64214-134">Namespace</span></span><br/>                | <span data-ttu-id="64214-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="64214-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="64214-136">MOF</span><span class="sxs-lookup"><span data-stu-id="64214-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64214-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64214-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="64214-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="64214-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64214-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="64214-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="64214-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="64214-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64214-141">**MSVM \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="64214-141">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

