---
description: Genera un conjunto de nombres de Puerto WWPN (WWPN).
ms.assetid: 36f393eb-6f34-4ae3-a976-c5da60211f3e
title: Método GenerateWwpn de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GenerateWwpn
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b0efba6a24a7e4f7e6826f91930cb69b4b54f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686897"
---
# <a name="generatewwpn-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="af106-103">Método GenerateWwpn de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="af106-103">GenerateWwpn method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="af106-104">Genera un conjunto de nombres de Puerto WWPN (WWPN).</span><span class="sxs-lookup"><span data-stu-id="af106-104">Generates a set of World Wide Port Names (WWPNs).</span></span> <span data-ttu-id="af106-105">Los WWPN se generan desde el intervalo preconfigurado definido por las propiedades **MinimumWWPNAddress** y **MaximumWWPNAddress** de la clase [**MSVM \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="af106-105">The WWPNs are generated from within the pre-configured range defined by the **MinimumWWPNAddress** and **MaximumWWPNAddress** properties of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class.</span></span> <span data-ttu-id="af106-106">Si el número de WWPN válido que se puede generar es menor que el número solicitado, las entradas restantes de la matriz *GeneratedWwpn* tendrán la entrada no válida de "0000000000000000" y el valor devuelto indicará Success (0).</span><span class="sxs-lookup"><span data-stu-id="af106-106">If the valid number of WWPNs that can be generated is less than the requested number, then the remaining entries in the *GeneratedWwpn* array will have the invalid entry of "0000000000000000" and the return value will indicate success (0).</span></span>

## <a name="syntax"></a><span data-ttu-id="af106-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af106-107">Syntax</span></span>


```mof
uint32 GenerateWwpn(
  [in]  uint32 NumberOfWwpns,
  [out] string GeneratedWwpn[]
);
```



## <a name="parameters"></a><span data-ttu-id="af106-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af106-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af106-109">*NumberOfWwpns* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="af106-109">*NumberOfWwpns* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af106-110">Número de WWPN que se van a generar.</span><span class="sxs-lookup"><span data-stu-id="af106-110">The number of WWPNs to be generated.</span></span>

</dd> <dt>

<span data-ttu-id="af106-111">*GeneratedWwpn* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="af106-111">*GeneratedWwpn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af106-112">Matriz de cadenas, cada una de las cuales contendrá un WWPN generado.</span><span class="sxs-lookup"><span data-stu-id="af106-112">An array of strings, each of which will contain a generated WWPN.</span></span> <span data-ttu-id="af106-113">Se le aplicará el formato de cadena como "01:23:45:67:89: AB: CD: EF".</span><span class="sxs-lookup"><span data-stu-id="af106-113">It will be formatted in string form as "01:23:45:67:89:ab:cd:ef".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af106-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af106-114">Return value</span></span>

<span data-ttu-id="af106-115">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="af106-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="af106-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="af106-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="af106-117">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="af106-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="af106-118">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="af106-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="af106-119">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="af106-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="af106-120">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="af106-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="af106-121">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="af106-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="af106-122">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="af106-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="af106-123">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="af106-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="af106-124">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="af106-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="af106-125">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="af106-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="af106-126">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="af106-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="af106-127">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="af106-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="af106-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af106-128">Requirements</span></span>



| <span data-ttu-id="af106-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="af106-129">Requirement</span></span> | <span data-ttu-id="af106-130">Value</span><span class="sxs-lookup"><span data-stu-id="af106-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af106-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af106-131">Minimum supported client</span></span><br/> | <span data-ttu-id="af106-132">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="af106-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="af106-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af106-133">Minimum supported server</span></span><br/> | <span data-ttu-id="af106-134">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="af106-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="af106-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="af106-135">Namespace</span></span><br/>                | <span data-ttu-id="af106-136">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="af106-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="af106-137">MOF</span><span class="sxs-lookup"><span data-stu-id="af106-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af106-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af106-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="af106-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="af106-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af106-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="af106-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="af106-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="af106-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af106-142">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="af106-142">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




