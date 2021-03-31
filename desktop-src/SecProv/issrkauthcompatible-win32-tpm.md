---
description: El método IsSrkAuthCompatible de la clase de Win32 \_ TPM indica si la autorización de la clave raíz de almacenamiento (SRK) es compatible con el valor esperado por Windows Vista.
ms.assetid: ce6d05b8-673a-40ab-a1d7-3fedfd099306
title: Método IsSrkAuthCompatible de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsSrkAuthCompatible
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: f5250f8d3f9ad38f9d4c46350e06e0fe32f756dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911574"
---
# <a name="issrkauthcompatible-method-of-the-win32_tpm-class"></a><span data-ttu-id="f56b5-103">Método IsSrkAuthCompatible de la \_ clase Win32 TPM</span><span class="sxs-lookup"><span data-stu-id="f56b5-103">IsSrkAuthCompatible method of the Win32\_Tpm class</span></span>

<span data-ttu-id="f56b5-104">El método **IsSrkAuthCompatible** de la clase de [**Win32 \_ TPM**](win32-tpm.md) indica si la autorización de la clave raíz de almacenamiento (SRK) es compatible con el valor esperado por Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f56b5-104">The **IsSrkAuthCompatible** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the Storage Root Key (SRK) authorization is compatible with the value expected by Windows Vista.</span></span>

## <a name="syntax"></a><span data-ttu-id="f56b5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f56b5-105">Syntax</span></span>


```mof
uint32 IsSrkAuthCompatible(
  [out] boolean IsSrkAuthCompatible
);
```



## <a name="parameters"></a><span data-ttu-id="f56b5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f56b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f56b5-107">*IsSrkAuthCompatible* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f56b5-107">*IsSrkAuthCompatible* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f56b5-108">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f56b5-108">Type: **boolean**</span></span>

<span data-ttu-id="f56b5-109">Si **es true**, el valor de autorización de la SRK tiene un valor de cero.</span><span class="sxs-lookup"><span data-stu-id="f56b5-109">If **true**, the SRK authorization value has a value of zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f56b5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f56b5-110">Return value</span></span>

<span data-ttu-id="f56b5-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f56b5-111">Type: **uint32**</span></span>

<span data-ttu-id="f56b5-112">Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.</span><span class="sxs-lookup"><span data-stu-id="f56b5-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="f56b5-113">A continuación se enumeran los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="f56b5-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="f56b5-114">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f56b5-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="f56b5-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="f56b5-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="f56b5-116"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="f56b5-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="f56b5-117">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f56b5-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f56b5-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f56b5-118">Remarks</span></span>

<span data-ttu-id="f56b5-119">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f56b5-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f56b5-120">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f56b5-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f56b5-121">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="f56b5-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f56b5-122">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f56b5-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f56b5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f56b5-123">Requirements</span></span>



| <span data-ttu-id="f56b5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f56b5-124">Requirement</span></span> | <span data-ttu-id="f56b5-125">Value</span><span class="sxs-lookup"><span data-stu-id="f56b5-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f56b5-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f56b5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f56b5-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f56b5-127">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f56b5-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f56b5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f56b5-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f56b5-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f56b5-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f56b5-130">Namespace</span></span><br/>                | <span data-ttu-id="f56b5-131">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="f56b5-131">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="f56b5-132">MOF</span><span class="sxs-lookup"><span data-stu-id="f56b5-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f56b5-133"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f56b5-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="f56b5-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f56b5-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f56b5-135"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="f56b5-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f56b5-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f56b5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f56b5-137">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="f56b5-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
