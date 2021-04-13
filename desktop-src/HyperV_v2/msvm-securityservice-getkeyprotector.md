---
description: Recupera el protector de clave de un sistema virtual.
ms.assetid: fd827da8-b2fc-4c57-bb7d-7da46db8e8be
title: Método GetKeyProtector de la clase Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.GetKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 49f2479660d0402c7b3d428c76f9fe454ecf64cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361729"
---
# <a name="getkeyprotector-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="54ac5-103">Método GetKeyProtector de la \_ clase SecurityService de MSVM</span><span class="sxs-lookup"><span data-stu-id="54ac5-103">GetKeyProtector method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="54ac5-104">Recupera el protector de clave de un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="54ac5-104">Retrieves the key protector for a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="54ac5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54ac5-105">Syntax</span></span>


```mof
uint32 GetKeyProtector(
  [in]  string SecuritySettingData,
  [out] uint8  KeyProtector[]
);
```



## <a name="parameters"></a><span data-ttu-id="54ac5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54ac5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54ac5-107">*SecuritySettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="54ac5-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54ac5-108">String contiene una instancia incrustada de la clase [**MSVM \_ SecuritySettingData**](msvm-securitysettingdata.md) que representa la configuración de seguridad de un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="54ac5-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="54ac5-109">*KeyProtector* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="54ac5-109">*KeyProtector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54ac5-110">Recibe la matriz de bytes sin formato que contiene el protector de clave actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="54ac5-110">Receives the raw byte array that contains the key protector currently in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54ac5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54ac5-111">Return value</span></span>

<span data-ttu-id="54ac5-112">Si se ejecuta correctamente, devuelve 0 o 4096.</span><span class="sxs-lookup"><span data-stu-id="54ac5-112">On success, returns a 0 or 4096.</span></span> <span data-ttu-id="54ac5-113">De lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="54ac5-113">Otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="54ac5-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="54ac5-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="54ac5-115">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="54ac5-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="54ac5-116">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="54ac5-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="54ac5-117">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="54ac5-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="54ac5-118">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="54ac5-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="54ac5-119">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="54ac5-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="54ac5-120">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="54ac5-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="54ac5-121">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="54ac5-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="54ac5-122">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="54ac5-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="54ac5-123">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="54ac5-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="54ac5-124">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="54ac5-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="54ac5-125">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="54ac5-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="54ac5-126">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="54ac5-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="54ac5-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54ac5-127">Requirements</span></span>



| <span data-ttu-id="54ac5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="54ac5-128">Requirement</span></span> | <span data-ttu-id="54ac5-129">Value</span><span class="sxs-lookup"><span data-stu-id="54ac5-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54ac5-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54ac5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="54ac5-131">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="54ac5-131">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="54ac5-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54ac5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="54ac5-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="54ac5-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="54ac5-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="54ac5-134">Namespace</span></span><br/>                | <span data-ttu-id="54ac5-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="54ac5-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="54ac5-136">MOF</span><span class="sxs-lookup"><span data-stu-id="54ac5-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54ac5-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54ac5-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="54ac5-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="54ac5-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54ac5-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="54ac5-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="54ac5-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="54ac5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54ac5-141">**MSVM \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="54ac5-141">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




