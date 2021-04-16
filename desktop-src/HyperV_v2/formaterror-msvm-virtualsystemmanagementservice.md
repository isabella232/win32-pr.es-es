---
description: Devuelve una cadena de mensaje de error con formato para la matriz especificada de instancias de error incrustadas MSVM \_ .
ms.assetid: 477EF4AE-00A8-4F2D-A335-E41A2EF620BB
title: Método FormatError de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.FormatError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e768a6ea968d428d7809c7c322a80f3ad233aa2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666562"
---
# <a name="formaterror-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="12877-103">Método FormatError de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="12877-103">FormatError method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="12877-104">Devuelve una cadena de mensaje de error con formato para la matriz especificada de instancias de [**\_ error**](msvm-error.md) incrustadas MSVM.</span><span class="sxs-lookup"><span data-stu-id="12877-104">Returns a formatted error message string for the specified array of embedded [**Msvm\_Error**](msvm-error.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="12877-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12877-105">Syntax</span></span>


```mof
uint32 FormatError(
  [in]  string Errors[],
  [out] string ErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="12877-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="12877-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12877-107">*Errores* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="12877-107">*Errors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12877-108">Tipo: **String \[ \]**</span><span class="sxs-lookup"><span data-stu-id="12877-108">Type: **string\[\]**</span></span>

<span data-ttu-id="12877-109">Matriz de cadenas que contiene las instancias de [**\_ error de MSVM**](msvm-error.md) utilizadas para generar el mensaje de error de salida.</span><span class="sxs-lookup"><span data-stu-id="12877-109">An array of strings containing [**Msvm\_Error**](msvm-error.md) instances used to generate the output error message.</span></span>

</dd> <dt>

<span data-ttu-id="12877-110">*ErrorMessage* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="12877-110">*ErrorMessage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12877-111">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="12877-111">Type: **string**</span></span>

<span data-ttu-id="12877-112">En la salida, cadena que contiene los mensajes de error concatenados representados por las instancias de [**\_ error MSVM**](msvm-error.md) que se han pasado en *el parámetro* Errors.</span><span class="sxs-lookup"><span data-stu-id="12877-112">On output, a string that contains the concatenated error messages represented by the [**Msvm\_Error**](msvm-error.md) instances passed in the *Errors* parameter.</span></span> <span data-ttu-id="12877-113">Cada cadena de error está separada por un par de caracteres de nueva línea (' \\ n ').</span><span class="sxs-lookup"><span data-stu-id="12877-113">Each error string is separated by a pair of newline characters ('\\n').</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12877-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="12877-114">Return value</span></span>

<span data-ttu-id="12877-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12877-115">Type: **uint32**</span></span>

<span data-ttu-id="12877-116">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="12877-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="12877-117">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="12877-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="12877-118">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="12877-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="12877-119">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="12877-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="12877-120">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="12877-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="12877-121">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="12877-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="12877-122">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="12877-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="12877-123">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="12877-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="12877-124">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="12877-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="12877-125">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="12877-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="12877-126">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="12877-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="12877-127">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="12877-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="12877-128">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="12877-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="12877-129">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="12877-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="12877-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12877-130">Remarks</span></span>

<span data-ttu-id="12877-131">El acceso a la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="12877-131">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="12877-132">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="12877-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="12877-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12877-133">Requirements</span></span>



| <span data-ttu-id="12877-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="12877-134">Requirement</span></span> | <span data-ttu-id="12877-135">Value</span><span class="sxs-lookup"><span data-stu-id="12877-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12877-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12877-136">Minimum supported client</span></span><br/> | <span data-ttu-id="12877-137">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="12877-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="12877-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12877-138">Minimum supported server</span></span><br/> | <span data-ttu-id="12877-139">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="12877-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="12877-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="12877-140">Namespace</span></span><br/>                | <span data-ttu-id="12877-141">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="12877-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="12877-142">MOF</span><span class="sxs-lookup"><span data-stu-id="12877-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12877-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12877-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="12877-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="12877-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12877-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="12877-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="12877-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="12877-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12877-147">**FormatError (V1)**</span><span class="sxs-lookup"><span data-stu-id="12877-147">**FormatError (V1)**</span></span>](/previous-versions/windows/desktop/virtual/formaterror-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="12877-148">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="12877-148">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

