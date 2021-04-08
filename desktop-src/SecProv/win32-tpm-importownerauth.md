---
description: Importa la información de autorización del propietario de un TPM que ya es propiedad del registro del sistema operativo.
ms.assetid: 9611D363-6F10-48B9-B417-97133E975257
title: 'Win32_Tpm:: ImportOwnerAuth (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ImportOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: c74d99ab5cf101aa424dcf1921da774f53e21de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001042"
---
# <a name="win32_tpmimportownerauth-method"></a><span data-ttu-id="d075b-103">Win32 \_ TPM:: ImportOwnerAuth (método)</span><span class="sxs-lookup"><span data-stu-id="d075b-103">Win32\_Tpm::ImportOwnerAuth method</span></span>

<span data-ttu-id="d075b-104">Importa la información de autorización del propietario de un TPM que ya es propiedad del registro del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d075b-104">Imports the owner authorization information for a TPM that is already owned into the operating system registry.</span></span> <span data-ttu-id="d075b-105">Esta operación validará primero si la información de autorización de propietario proporcionada es correcta.</span><span class="sxs-lookup"><span data-stu-id="d075b-105">This operation will first validate if the supplied owner authorization information is correct.</span></span> <span data-ttu-id="d075b-106">Si es correcto, el método importa esta información en el registro.</span><span class="sxs-lookup"><span data-stu-id="d075b-106">If correct, the method imports this information to the registry.</span></span>

<span data-ttu-id="d075b-107">Este método solo es accesible para los administradores locales.</span><span class="sxs-lookup"><span data-stu-id="d075b-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="d075b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d075b-108">Syntax</span></span>


```C++
uint32 ImportOwnerAuth(
  [in] STRING OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="d075b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d075b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d075b-110">*OwnerAuth* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d075b-110">*OwnerAuth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d075b-111">Información de autorización de propietario válida para el TPM.</span><span class="sxs-lookup"><span data-stu-id="d075b-111">The valid owner authorization information for the TPM.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d075b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d075b-112">Return value</span></span>

<span data-ttu-id="d075b-113">Se pueden devolver todos los errores de TPM, así como los errores específicos de los [servicios base de TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="d075b-113">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="d075b-114">A continuación se enumeran los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="d075b-114">Common return codes are listed below.</span></span>



| <span data-ttu-id="d075b-115">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d075b-115">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="d075b-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="d075b-116">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="d075b-117"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="d075b-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="d075b-118">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d075b-118">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d075b-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d075b-119">Remarks</span></span>

<span data-ttu-id="d075b-120">Este método es especialmente útil en los escenarios en los que el TPM se encuentra en un estado de funcionalidad reducida y requiere que la importación de la autorización del propietario esté totalmente preparada o en escenarios de arranque dual, donde uno de los sistemas operativos posee el TPM y la información de autorización del propietario para TPM no está disponible en el otro sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d075b-120">This method is particularly useful in the scenarios where the TPM is in a "ready with reduced functionality state " and requires the importing of the owner authorization to be fully ready or in a dual-boot scenarios where one of the operating systems has owned the TPM and the owner authorization information for TPM is not available in the other operating system.</span></span>

<span data-ttu-id="d075b-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d075b-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d075b-122">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d075b-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="d075b-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="d075b-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d075b-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="d075b-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d075b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d075b-125">Requirements</span></span>



| <span data-ttu-id="d075b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d075b-126">Requirement</span></span> | <span data-ttu-id="d075b-127">Value</span><span class="sxs-lookup"><span data-stu-id="d075b-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d075b-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d075b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d075b-129">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="d075b-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d075b-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d075b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d075b-131">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d075b-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d075b-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d075b-132">Namespace</span></span><br/>                | <span data-ttu-id="d075b-133">\\\\.\\ \\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="d075b-133">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="d075b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d075b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d075b-135"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d075b-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="d075b-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d075b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d075b-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="d075b-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d075b-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="d075b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d075b-139">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="d075b-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
