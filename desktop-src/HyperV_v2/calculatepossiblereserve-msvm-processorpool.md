---
description: Este método se usa para buscar la reserva real con el parámetro de entrada que es el número de procesadores de máquinas virtuales para los que se calcula la reserva.
ms.assetid: C0497900-00F3-4975-9D12-C82C13C03D8E
title: Método CalculatePossibleReserve de la clase Msvm_ProcessorPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorPool.CalculatePossibleReserve
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7f88bcf3295b1792fca6be88ae0c9282b72646e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813854"
---
# <a name="calculatepossiblereserve-method-of-the-msvm_processorpool-class"></a><span data-ttu-id="effac-103">Método CalculatePossibleReserve de la \_ clase ProcessorPool de MSVM</span><span class="sxs-lookup"><span data-stu-id="effac-103">CalculatePossibleReserve method of the Msvm\_ProcessorPool class</span></span>

<span data-ttu-id="effac-104">Este método se usa para buscar la reserva real con el parámetro de entrada que es el número de procesadores de máquinas virtuales para los que se calcula la reserva.</span><span class="sxs-lookup"><span data-stu-id="effac-104">This method is used to find the actual reserve with the input parameter being the number of virtual machine processors for which the reserve is calculated.</span></span> <span data-ttu-id="effac-105">Este método es necesario porque la reserva de recursos del procesador depende en gran medida del número de procesadores que se deben programar en paralelo.</span><span class="sxs-lookup"><span data-stu-id="effac-105">This method is necessary because the reservation of processor resources is highly dependent on the number of processors which must be scheduled in parallel.</span></span>

## <a name="syntax"></a><span data-ttu-id="effac-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="effac-106">Syntax</span></span>


```mof
uint32 CalculatePossibleReserve(
  [in] uint16 ProcessorCount
);
```



## <a name="parameters"></a><span data-ttu-id="effac-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="effac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="effac-108">*ProcessorCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="effac-108">*ProcessorCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="effac-109">Tipo: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="effac-109">Type: **uint16**</span></span>

<span data-ttu-id="effac-110">El número de procesadores de máquinas virtuales para los que se calcula la reserva.</span><span class="sxs-lookup"><span data-stu-id="effac-110">The number of virtual machine processors for which the reserve is calculated.</span></span> <span data-ttu-id="effac-111">El valor máximo de esta propiedad es el número de procesadores lógicos para el equipo host.</span><span class="sxs-lookup"><span data-stu-id="effac-111">The maximum value for this property is the logical processor count for the host computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="effac-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="effac-112">Return value</span></span>

<span data-ttu-id="effac-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="effac-113">Type: **uint32**</span></span>

<span data-ttu-id="effac-114">La cantidad de recursos de CPU que se pueden reservar para una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="effac-114">The amount of CPU resources that may be reserved for a virtual machine.</span></span>

## <a name="remarks"></a><span data-ttu-id="effac-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="effac-115">Remarks</span></span>

<span data-ttu-id="effac-116">El acceso a la clase [**MSVM \_ ProcessorPool**](msvm-processorpool.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="effac-116">Access to the [**Msvm\_ProcessorPool**](msvm-processorpool.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="effac-117">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="effac-117">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="effac-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="effac-118">Requirements</span></span>



| <span data-ttu-id="effac-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="effac-119">Requirement</span></span> | <span data-ttu-id="effac-120">Value</span><span class="sxs-lookup"><span data-stu-id="effac-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="effac-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="effac-121">Minimum supported client</span></span><br/> | <span data-ttu-id="effac-122">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="effac-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="effac-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="effac-123">Minimum supported server</span></span><br/> | <span data-ttu-id="effac-124">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="effac-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="effac-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="effac-125">Namespace</span></span><br/>                | <span data-ttu-id="effac-126">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="effac-126">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="effac-127">MOF</span><span class="sxs-lookup"><span data-stu-id="effac-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="effac-128"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="effac-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="effac-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="effac-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="effac-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="effac-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="effac-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="effac-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="effac-132">**MSVM \_ ProcessorPool**</span><span class="sxs-lookup"><span data-stu-id="effac-132">**Msvm\_ProcessorPool**</span></span>](msvm-processorpool.md)
</dt> </dl>

 

