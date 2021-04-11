---
description: Solicita el Servicios de Escritorio remoto dispositivo virtual para iniciar una conexión de canalización con la máquina virtual.
ms.assetid: e53238ee-8264-416b-8855-193c28089cfa
title: Método EnableEndPoints de la clase Msvm_RdvComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponent.EnableEndPoints
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a668e6a2605a52c7021f630145d6e4897e1c76ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275553"
---
# <a name="enableendpoints-method-of-the-msvm_rdvcomponent-class"></a><span data-ttu-id="c4d44-103">Método EnableEndPoints de la \_ clase RdvComponent de MSVM</span><span class="sxs-lookup"><span data-stu-id="c4d44-103">EnableEndPoints method of the Msvm\_RdvComponent class</span></span>

<span data-ttu-id="c4d44-104">Solicita el Servicios de Escritorio remoto dispositivo virtual para iniciar una conexión de canalización con la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c4d44-104">Requests the Remote Desktop Services virtual device to start a pipe connection with the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4d44-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4d44-105">Syntax</span></span>


```mof
uint32 EnableEndPoints();
```



## <a name="parameters"></a><span data-ttu-id="c4d44-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4d44-106">Parameters</span></span>

<span data-ttu-id="c4d44-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c4d44-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c4d44-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4d44-108">Return value</span></span>

<span data-ttu-id="c4d44-109">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c4d44-109">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c4d44-110">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="c4d44-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c4d44-111">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="c4d44-111">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c4d44-112">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="c4d44-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c4d44-113">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="c4d44-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c4d44-114">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="c4d44-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c4d44-115">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="c4d44-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c4d44-116">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="c4d44-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c4d44-117">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="c4d44-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c4d44-118">**Memoria insuficiente** (32774)</span><span class="sxs-lookup"><span data-stu-id="c4d44-118">**Out of memory** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c4d44-119">**No se encontró el archivo** (32775)</span><span class="sxs-lookup"><span data-stu-id="c4d44-119">**File not found** (32775)</span></span>
</dt> <dt>

 <span data-ttu-id="c4d44-120">(32776)</span><span class="sxs-lookup"><span data-stu-id="c4d44-120">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="c4d44-121">(32777)</span><span class="sxs-lookup"><span data-stu-id="c4d44-121">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="c4d44-122">(32778)</span><span class="sxs-lookup"><span data-stu-id="c4d44-122">(32778)</span></span>
</dt> <dt>

 <span data-ttu-id="c4d44-123">(32779)</span><span class="sxs-lookup"><span data-stu-id="c4d44-123">(32779)</span></span>
</dt> <dt>

 <span data-ttu-id="c4d44-124">(32780)</span><span class="sxs-lookup"><span data-stu-id="c4d44-124">(32780)</span></span>
</dt> <dt>

 <span data-ttu-id="c4d44-125">(32781)</span><span class="sxs-lookup"><span data-stu-id="c4d44-125">(32781)</span></span>
</dt> <dt>

 <span data-ttu-id="c4d44-126">(32782)</span><span class="sxs-lookup"><span data-stu-id="c4d44-126">(32782)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c4d44-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4d44-127">Requirements</span></span>



| <span data-ttu-id="c4d44-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4d44-128">Requirement</span></span> | <span data-ttu-id="c4d44-129">Value</span><span class="sxs-lookup"><span data-stu-id="c4d44-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4d44-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4d44-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c4d44-131">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="c4d44-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c4d44-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4d44-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c4d44-133">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="c4d44-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c4d44-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c4d44-134">Namespace</span></span><br/>                | <span data-ttu-id="c4d44-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="c4d44-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c4d44-136">MOF</span><span class="sxs-lookup"><span data-stu-id="c4d44-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4d44-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4d44-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4d44-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c4d44-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4d44-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c4d44-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c4d44-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4d44-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4d44-141">**MSVM \_ RdvComponent**</span><span class="sxs-lookup"><span data-stu-id="c4d44-141">**Msvm\_RdvComponent**</span></span>](msvm-rdvcomponent.md)
</dt> </dl>

 

 




