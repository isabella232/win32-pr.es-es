---
description: 'Método ModifyServiceSettings de la Msvm_TerminalService clase : modifica los datos de configuración del servicio.'
ms.assetid: 76669180-fa95-4d6e-b89a-53e45da664c4
title: Método ModifyServiceSettings de la Msvm_TerminalService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 930b29c5c07c755b493a0aabad88ae776c0803e0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119333"
---
# <a name="modifyservicesettings-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="02bda-103">Método ModifyServiceSettings de la clase TerminalService de \_ Msvm</span><span class="sxs-lookup"><span data-stu-id="02bda-103">ModifyServiceSettings method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="02bda-104">Modifica los datos de configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="02bda-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="02bda-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02bda-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              ServiceSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="02bda-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02bda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02bda-107">*ServiceSettingData* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="02bda-107">*ServiceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02bda-108">Representación de cadena de la [**clase \_ TerminalServiceSettingData de Msvm**](msvm-terminalservicesettingdata.md) que contiene los datos de configuración modificados para el servicio.</span><span class="sxs-lookup"><span data-stu-id="02bda-108">A string representation of the [**Msvm\_TerminalServiceSettingData**](msvm-terminalservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="02bda-109">*Trabajo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="02bda-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02bda-110">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="02bda-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02bda-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02bda-111">Return value</span></span>

<span data-ttu-id="02bda-112">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="02bda-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="02bda-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="02bda-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="02bda-114">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="02bda-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="02bda-115">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="02bda-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="02bda-116">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="02bda-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="02bda-117">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="02bda-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="02bda-118">**El estado es desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="02bda-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="02bda-119">**Tiempo de** espera (32772)</span><span class="sxs-lookup"><span data-stu-id="02bda-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="02bda-120">**Parámetro no** válido (32773)</span><span class="sxs-lookup"><span data-stu-id="02bda-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="02bda-121">**El sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="02bda-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="02bda-122">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="02bda-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="02bda-123">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="02bda-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="02bda-124">**El sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="02bda-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="02bda-125">**Memoria sin memoria** (32778)</span><span class="sxs-lookup"><span data-stu-id="02bda-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="02bda-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02bda-126">Requirements</span></span>



| <span data-ttu-id="02bda-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="02bda-127">Requirement</span></span> | <span data-ttu-id="02bda-128">Valor</span><span class="sxs-lookup"><span data-stu-id="02bda-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02bda-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02bda-129">Minimum supported client</span></span><br/> | <span data-ttu-id="02bda-130">Windows 8 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="02bda-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="02bda-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02bda-131">Minimum supported server</span></span><br/> | <span data-ttu-id="02bda-132">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="02bda-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="02bda-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="02bda-133">Namespace</span></span><br/>                | <span data-ttu-id="02bda-134">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="02bda-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="02bda-135">MOF</span><span class="sxs-lookup"><span data-stu-id="02bda-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02bda-136"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="02bda-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="02bda-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="02bda-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02bda-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="02bda-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="02bda-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="02bda-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02bda-140">**TerminalService de Msvm \_**</span><span class="sxs-lookup"><span data-stu-id="02bda-140">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

