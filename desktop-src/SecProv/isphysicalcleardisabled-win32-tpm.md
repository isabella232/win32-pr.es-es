---
description: El método IsPhysicalClearDisabled de la clase de Win32 \_ TPM indica si solo el propietario del dispositivo puede borrar el dispositivo.
ms.assetid: b87f1c4f-8735-45c5-9256-53dbb9579f95
title: Método IsPhysicalClearDisabled de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsPhysicalClearDisabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 9179aae2f4902ce29e2bab98b4c9c0b793804de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688017"
---
# <a name="isphysicalcleardisabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="43eba-103">Método IsPhysicalClearDisabled de la \_ clase Win32 TPM</span><span class="sxs-lookup"><span data-stu-id="43eba-103">IsPhysicalClearDisabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="43eba-104">El método **IsPhysicalClearDisabled** de la clase de [**Win32 \_ TPM**](win32-tpm.md) indica si solo el propietario del dispositivo puede borrar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43eba-104">The **IsPhysicalClearDisabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether only the device owner may be able to clear the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="43eba-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43eba-105">Syntax</span></span>


```mof
uint32 IsPhysicalClearDisabled(
  [out] boolean IsPhysicalClearDisabled
);
```



## <a name="parameters"></a><span data-ttu-id="43eba-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43eba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43eba-107">*IsPhysicalClearDisabled* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="43eba-107">*IsPhysicalClearDisabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43eba-108">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="43eba-108">Type: **boolean**</span></span>

<span data-ttu-id="43eba-109">Si es **true**, solo el propietario del dispositivo puede borrar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43eba-109">If **true**, only the device owner is able to clear the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43eba-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43eba-110">Return value</span></span>

<span data-ttu-id="43eba-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43eba-111">Type: **uint32**</span></span>

<span data-ttu-id="43eba-112">Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.</span><span class="sxs-lookup"><span data-stu-id="43eba-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="43eba-113">A continuación se enumeran los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="43eba-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="43eba-114">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43eba-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="43eba-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="43eba-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="43eba-116"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="43eba-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="43eba-117">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="43eba-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="43eba-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="43eba-118">Remarks</span></span>

<span data-ttu-id="43eba-119">Este valor se restablece en **false** al principio de cada ciclo de inicio.</span><span class="sxs-lookup"><span data-stu-id="43eba-119">This value is reset to **false** at the beginning of each startup cycle.</span></span>

<span data-ttu-id="43eba-120">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="43eba-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="43eba-121">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="43eba-121">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="43eba-122">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="43eba-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="43eba-123">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="43eba-123">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="43eba-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43eba-124">Requirements</span></span>



| <span data-ttu-id="43eba-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="43eba-125">Requirement</span></span> | <span data-ttu-id="43eba-126">Value</span><span class="sxs-lookup"><span data-stu-id="43eba-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="43eba-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43eba-127">Minimum supported client</span></span><br/> | <span data-ttu-id="43eba-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="43eba-128">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="43eba-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43eba-129">Minimum supported server</span></span><br/> | <span data-ttu-id="43eba-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="43eba-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="43eba-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="43eba-131">Namespace</span></span><br/>                | <span data-ttu-id="43eba-132">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="43eba-132">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="43eba-133">MOF</span><span class="sxs-lookup"><span data-stu-id="43eba-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43eba-134"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43eba-134"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="43eba-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="43eba-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43eba-136"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="43eba-136"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43eba-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="43eba-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43eba-138">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="43eba-138">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
