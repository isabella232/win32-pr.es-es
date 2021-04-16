---
description: Recupera información adicional sobre un error.
ms.assetid: 63ce4762-e5ce-405f-b5fc-74e505b0eaf1
title: Método GetErrorEx de la clase Msvm_VirtualSystemReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4c6c392adb2b638c2d638b758696252adcb54d7e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105670059"
---
# <a name="geterrorex-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="69a2f-103">Método GetErrorEx de la \_ clase VirtualSystemReferencePointExportJob de MSVM</span><span class="sxs-lookup"><span data-stu-id="69a2f-103">GetErrorEx method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="69a2f-104">Recupera información adicional sobre un error.</span><span class="sxs-lookup"><span data-stu-id="69a2f-104">Retrieves additional information about an error.</span></span> <span data-ttu-id="69a2f-105">Cuando el trabajo se está ejecutando o ha finalizado sin errores, **GetErrorEx** no devuelve ninguna instancia de **GetErrorEx** .</span><span class="sxs-lookup"><span data-stu-id="69a2f-105">When the job is executing or has terminated without error, **GetErrorEx** returns no **GetErrorEx** instance.</span></span> <span data-ttu-id="69a2f-106">Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque el trabajo ha sido terminado por un cliente, **GetErrorEx** devuelve una o varias instancias de [**\_ error MSVM**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="69a2f-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then **GetErrorEx** returns one or more [**Msvm\_Error**](msvm-error.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="69a2f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69a2f-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="69a2f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69a2f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69a2f-109">*Errores* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="69a2f-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69a2f-110">Si el estado operativo del trabajo no es "correcto", este parámetro devuelve una matriz de instancias [**de \_ error de MSVM**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="69a2f-110">If the operational status of the job is not "OK", this parameter returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="69a2f-111">De lo contrario, si el trabajo es "OK", este parámetro contiene **null**.</span><span class="sxs-lookup"><span data-stu-id="69a2f-111">Otherwise, if the job is "OK", this parameter contains **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69a2f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69a2f-112">Return value</span></span>

<span data-ttu-id="69a2f-113">Si se ejecuta correctamente, devuelve 0; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="69a2f-113">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="69a2f-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="69a2f-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="69a2f-115">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="69a2f-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="69a2f-116">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="69a2f-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="69a2f-117">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="69a2f-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="69a2f-118">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="69a2f-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="69a2f-119">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="69a2f-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="69a2f-120">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="69a2f-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="69a2f-121">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="69a2f-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="69a2f-122">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="69a2f-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="69a2f-123">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="69a2f-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="69a2f-124">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="69a2f-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="69a2f-125">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="69a2f-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="69a2f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69a2f-126">Requirements</span></span>



| <span data-ttu-id="69a2f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="69a2f-127">Requirement</span></span> | <span data-ttu-id="69a2f-128">Value</span><span class="sxs-lookup"><span data-stu-id="69a2f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69a2f-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69a2f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="69a2f-130">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="69a2f-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="69a2f-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69a2f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="69a2f-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="69a2f-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="69a2f-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="69a2f-133">Namespace</span></span><br/>                | <span data-ttu-id="69a2f-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="69a2f-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="69a2f-135">MOF</span><span class="sxs-lookup"><span data-stu-id="69a2f-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69a2f-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="69a2f-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="69a2f-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="69a2f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69a2f-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="69a2f-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="69a2f-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="69a2f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69a2f-140">**MSVM \_ VirtualSystemReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="69a2f-140">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




