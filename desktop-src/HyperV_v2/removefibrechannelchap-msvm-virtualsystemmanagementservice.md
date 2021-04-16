---
description: Quita los parámetros DH-CHAP (Diffie Hellman-desafío de autenticación por desafío mutuo) de un puerto de Canal de fibra sintético en una máquina virtual.
ms.assetid: f15673e2-287d-4e87-bee4-6c0f5f9178c8
title: Método RemoveFibreChannelChap de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 06e944c3c592b0b61ace8a72b5d42a801ab0f5df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686929"
---
# <a name="removefibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="fe5f1-103">Método RemoveFibreChannelChap de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="fe5f1-103">RemoveFibreChannelChap method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="fe5f1-104">Quita los parámetros DH-CHAP (Diffie Hellman-desafío de autenticación por desafío mutuo) de un puerto de Canal de fibra sintético en una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fe5f1-104">Removes DH-CHAP (Diffie Hellman - Challenge Handshake Authentication Protocol) parameters from a synthetic Fibre Channel port in a virtual machine.</span></span> <span data-ttu-id="fe5f1-105">Este método producirá un error si la máquina virtual se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="fe5f1-105">This method will fail if the virtual machine is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe5f1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe5f1-106">Syntax</span></span>


```mof
uint32 RemoveFibreChannelChap(
  [in] string FcPortSettings[]
);
```



## <a name="parameters"></a><span data-ttu-id="fe5f1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe5f1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe5f1-108">*FcPortSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fe5f1-108">*FcPortSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe5f1-109">Matriz de cadenas que contiene una instancia incrustada de la clase [**MSVM \_ SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) que define los puertos canal de fibra sintéticos de los que se van a quitar los parámetros DH-CHAP.</span><span class="sxs-lookup"><span data-stu-id="fe5f1-109">An array of strings that contain an embedded instance of the [**Msvm\_SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) class that define the synthetic Fibre Channel ports to remove the DH-CHAP parameters from.</span></span> <span data-ttu-id="fe5f1-110">La propiedad **InstanceID** de cada una de estas instancias identifica los elementos que se van a modificar.</span><span class="sxs-lookup"><span data-stu-id="fe5f1-110">The **InstanceID** property of each of these instances identifies the elements to be modified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe5f1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe5f1-111">Return value</span></span>

<span data-ttu-id="fe5f1-112">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="fe5f1-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="fe5f1-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="fe5f1-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fe5f1-114">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="fe5f1-114">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="fe5f1-115">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="fe5f1-115">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="fe5f1-116">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="fe5f1-116">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="fe5f1-117">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="fe5f1-117">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="fe5f1-118">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="fe5f1-118">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="fe5f1-119">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="fe5f1-119">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="fe5f1-120">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="fe5f1-120">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="fe5f1-121">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="fe5f1-121">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="fe5f1-122">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="fe5f1-122">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="fe5f1-123">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="fe5f1-123">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="fe5f1-124">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="fe5f1-124">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fe5f1-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe5f1-125">Requirements</span></span>



| <span data-ttu-id="fe5f1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe5f1-126">Requirement</span></span> | <span data-ttu-id="fe5f1-127">Value</span><span class="sxs-lookup"><span data-stu-id="fe5f1-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe5f1-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe5f1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fe5f1-129">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="fe5f1-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fe5f1-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe5f1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fe5f1-131">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="fe5f1-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fe5f1-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fe5f1-132">Namespace</span></span><br/>                | <span data-ttu-id="fe5f1-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="fe5f1-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fe5f1-134">MOF</span><span class="sxs-lookup"><span data-stu-id="fe5f1-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe5f1-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe5f1-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe5f1-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fe5f1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe5f1-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fe5f1-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fe5f1-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe5f1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe5f1-139">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="fe5f1-139">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




