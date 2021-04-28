---
description: 'Método GetErrorEx de la Msvm_CollectionReferencePointExportJob clase : recupera información adicional sobre un error.'
ms.assetid: 64a90f18-3ae7-4021-857f-64adf8c40430
title: Método GetErrorEx de la Msvm_CollectionReferencePointExportJob clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3b84c41776c081c302078773d9402145b0fe41e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112093"
---
# <a name="geterrorex-method-of-the-msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="7acf9-103">Método GetErrorEx de la clase \_ CollectionReferencePointExportJob de Msvm</span><span class="sxs-lookup"><span data-stu-id="7acf9-103">GetErrorEx method of the Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="7acf9-104">Recupera información adicional sobre un error.</span><span class="sxs-lookup"><span data-stu-id="7acf9-104">Retrieves additional information about an error.</span></span> <span data-ttu-id="7acf9-105">Cuando el trabajo se está ejecutando o ha finalizado sin errores, **GetErrorEx** no devuelve ninguna [**instancia de \_ error de Msvm.**](msvm-error.md)</span><span class="sxs-lookup"><span data-stu-id="7acf9-105">When the job is executing or has terminated without error, **GetErrorEx** returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="7acf9-106">Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque un cliente ha finalizado el trabajo, **GetErrorEx** devuelve una o varias instancias de error de **\_ Msvm.**</span><span class="sxs-lookup"><span data-stu-id="7acf9-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then **GetErrorEx** returns one or more **Msvm\_Error** instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="7acf9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7acf9-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="7acf9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7acf9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7acf9-109">*Errores* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7acf9-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7acf9-110">Si el estado operativo del trabajo no es "Correcto", este parámetro devuelve una matriz de instancias de error de [**Msvm. \_**](msvm-error.md)</span><span class="sxs-lookup"><span data-stu-id="7acf9-110">If the operational status of the job is not "OK", this parameter returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="7acf9-111">De lo contrario, si el trabajo es "OK", este parámetro contiene **NULL.**</span><span class="sxs-lookup"><span data-stu-id="7acf9-111">Otherwise, if the job is "OK", this parameter contains **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7acf9-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7acf9-112">Return value</span></span>

<span data-ttu-id="7acf9-113">Si se ejecuta correctamente, devuelve 0; de lo contrario, devuelve uno de los siguientes valores de error:</span><span class="sxs-lookup"><span data-stu-id="7acf9-113">On success, returns 0; otherwise, returns one of the following error values:</span></span>

<dl> <dt>

<span data-ttu-id="7acf9-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="7acf9-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7acf9-115">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="7acf9-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="7acf9-116">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="7acf9-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="7acf9-117">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="7acf9-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="7acf9-118">**El estado es desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="7acf9-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="7acf9-119">**Tiempo de** espera (32772)</span><span class="sxs-lookup"><span data-stu-id="7acf9-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="7acf9-120">**Parámetro no** válido (32773)</span><span class="sxs-lookup"><span data-stu-id="7acf9-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="7acf9-121">**Sistema en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="7acf9-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="7acf9-122">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="7acf9-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="7acf9-123">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="7acf9-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="7acf9-124">**El sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="7acf9-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="7acf9-125">**Memoria sin memoria** (32778)</span><span class="sxs-lookup"><span data-stu-id="7acf9-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7acf9-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7acf9-126">Requirements</span></span>



| <span data-ttu-id="7acf9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7acf9-127">Requirement</span></span> | <span data-ttu-id="7acf9-128">Valor</span><span class="sxs-lookup"><span data-stu-id="7acf9-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7acf9-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7acf9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7acf9-130">Windows 10, solo aplicaciones de escritorio de la versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="7acf9-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7acf9-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7acf9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7acf9-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7acf9-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7acf9-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7acf9-133">Namespace</span></span><br/>                | <span data-ttu-id="7acf9-134">Virtualización \\ raíz \\ v2</span><span class="sxs-lookup"><span data-stu-id="7acf9-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7acf9-135">MOF</span><span class="sxs-lookup"><span data-stu-id="7acf9-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7acf9-136"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="7acf9-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7acf9-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7acf9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7acf9-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7acf9-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7acf9-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7acf9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7acf9-140">**Msvm \_ CollectionReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="7acf9-140">**Msvm\_CollectionReferencePointExportJob**</span></span>](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




