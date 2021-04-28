---
description: 'Método GetError de la Msvm_ConcreteJob clase : recupera el objeto de error para el trabajo, si existe alguno.'
ms.assetid: 7E810CBE-F18F-4EFA-B52E-631CD071D136
title: Método GetError de la Msvm_ConcreteJob clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c222a7091550b5ee831330f100292549e31ce5ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112193"
---
# <a name="geterror-method-of-the-msvm_concretejob-class"></a><span data-ttu-id="7c42b-103">Método GetError de la clase ConcreteJob de \_ Msvm</span><span class="sxs-lookup"><span data-stu-id="7c42b-103">GetError method of the Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="7c42b-104">Recupera el objeto de error para el trabajo, si existe uno.</span><span class="sxs-lookup"><span data-stu-id="7c42b-104">Retrieves the error object for the job, if one exists.</span></span> <span data-ttu-id="7c42b-105">Cuando el trabajo se está ejecutando o ha finalizado sin errores, este método no devuelve un [**objeto \_ cim error.**](/previous-versions//cc150671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7c42b-105">When the job is executing or has terminated without error, then this method does not return a [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)) object.</span></span> <span data-ttu-id="7c42b-106">Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque un cliente ha finalizado el trabajo, se devuelve una instancia **\_ de error** de CIM.</span><span class="sxs-lookup"><span data-stu-id="7c42b-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c42b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c42b-107">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="7c42b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c42b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c42b-109">*Error* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7c42b-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c42b-110">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7c42b-110">Type: **string**</span></span>

<span data-ttu-id="7c42b-111">Si el estado operativo del trabajo no es 2 (correcto), este método devuelve una instancia incrustada de la clase Error de [**Msvm, \_**](msvm-error.md) en formato CIM-XML.</span><span class="sxs-lookup"><span data-stu-id="7c42b-111">If the operational status of the job is not 2 (OK), this method returns an embedded instance of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format.</span></span> <span data-ttu-id="7c42b-112">Si el estado operativo del trabajo es 2 (correcto), se **devuelve Null.**</span><span class="sxs-lookup"><span data-stu-id="7c42b-112">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c42b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c42b-113">Return value</span></span>

<span data-ttu-id="7c42b-114">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="7c42b-114">Type: **uint32**</span></span>

<span data-ttu-id="7c42b-115">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="7c42b-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7c42b-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="7c42b-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7c42b-117">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="7c42b-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="7c42b-118">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="7c42b-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="7c42b-119">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="7c42b-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="7c42b-120">**El estado es desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="7c42b-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="7c42b-121">**Tiempo de** espera (32772)</span><span class="sxs-lookup"><span data-stu-id="7c42b-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="7c42b-122">**Parámetro no** válido (32773)</span><span class="sxs-lookup"><span data-stu-id="7c42b-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="7c42b-123">**Sistema en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="7c42b-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="7c42b-124">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="7c42b-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="7c42b-125">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="7c42b-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="7c42b-126">**El sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="7c42b-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="7c42b-127">**Memoria sin memoria** (32778)</span><span class="sxs-lookup"><span data-stu-id="7c42b-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="7c42b-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7c42b-128">Remarks</span></span>

<span data-ttu-id="7c42b-129">El acceso a [**la clase \_ Msvm ConcreteJob**](msvm-concretejob.md) podría estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="7c42b-129">Access to the [**Msvm\_ConcreteJob**](msvm-concretejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7c42b-130">Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)</span><span class="sxs-lookup"><span data-stu-id="7c42b-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c42b-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c42b-131">Requirements</span></span>



| <span data-ttu-id="7c42b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c42b-132">Requirement</span></span> | <span data-ttu-id="7c42b-133">Valor</span><span class="sxs-lookup"><span data-stu-id="7c42b-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c42b-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c42b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7c42b-135">Windows 8 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="7c42b-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7c42b-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c42b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7c42b-137">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="7c42b-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7c42b-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7c42b-138">Namespace</span></span><br/>                | <span data-ttu-id="7c42b-139">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="7c42b-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7c42b-140">MOF</span><span class="sxs-lookup"><span data-stu-id="7c42b-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c42b-141"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c42b-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c42b-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7c42b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c42b-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7c42b-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7c42b-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7c42b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c42b-145">**Msvm \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="7c42b-145">**Msvm\_ConcreteJob**</span></span>](msvm-concretejob.md)
</dt> </dl>

 

