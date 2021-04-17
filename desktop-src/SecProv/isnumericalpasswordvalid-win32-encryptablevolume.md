---
description: Indica si la contraseña numérica cumple los requisitos de formato especiales para este valor de autenticación.
ms.assetid: 3995405f-db4d-4f72-98dc-133a09f9cf65
title: Método IsNumericalPasswordValid de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsNumericalPasswordValid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7cec4aa31ae9ff6aee90c0f46ded935b3d553783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688018"
---
# <a name="isnumericalpasswordvalid-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f97a0-103">Método IsNumericalPasswordValid de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="f97a0-103">IsNumericalPasswordValid method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f97a0-104">El método **IsNumericalPasswordValid** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) indica si la contraseña numérica cumple los requisitos de formato especiales para este valor de autenticación.</span><span class="sxs-lookup"><span data-stu-id="f97a0-104">The **IsNumericalPasswordValid** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the numerical password meets the special format requirements for this authentication value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f97a0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f97a0-105">Syntax</span></span>


```mof
uint32 IsNumericalPasswordValid(
  [in]  string  NumericalPassword,
  [out] boolean IsNumericalPasswordValid
);
```



## <a name="parameters"></a><span data-ttu-id="f97a0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f97a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f97a0-107">*NumericalPassword* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f97a0-107">*NumericalPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f97a0-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="f97a0-108">Type: **string**</span></span>

<span data-ttu-id="f97a0-109">Cadena que especifica la contraseña numérica.</span><span class="sxs-lookup"><span data-stu-id="f97a0-109">A string that specifies the numerical password.</span></span>

<span data-ttu-id="f97a0-110">La contraseña numérica debe contener 48 dígitos.</span><span class="sxs-lookup"><span data-stu-id="f97a0-110">The numerical password must contain 48 digits.</span></span> <span data-ttu-id="f97a0-111">Estos dígitos se pueden dividir en 8 grupos de 6 dígitos, con el último dígito de cada grupo que indica un valor de suma de comprobación para el grupo.</span><span class="sxs-lookup"><span data-stu-id="f97a0-111">These digits can be divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="f97a0-112">Cada grupo de 6 dígitos debe ser divisible entre 11 y debe ser inferior a 720896.</span><span class="sxs-lookup"><span data-stu-id="f97a0-112">Each group of 6 digits must be divisible by 11 and must be less than 720896.</span></span> <span data-ttu-id="f97a0-113">Suponiendo que un grupo de seis dígitos se etiquete como x1, x2, x3, x4, X5 y x6, la suma de comprobación de dígito x6 se calcula como – x1 + x2 – x3 + x4 – X5 mod 11.</span><span class="sxs-lookup"><span data-stu-id="f97a0-113">Assuming a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="f97a0-114">Los grupos de dígitos se pueden separar opcionalmente con un espacio o un guión.</span><span class="sxs-lookup"><span data-stu-id="f97a0-114">The groups of digits can optionally be separated by a space or hyphen.</span></span> <span data-ttu-id="f97a0-115">Por lo tanto, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" o "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" también pueden contener contraseñas numéricas válidas.</span><span class="sxs-lookup"><span data-stu-id="f97a0-115">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" or "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" may also contain valid numerical passwords.</span></span>

</dd> <dt>

<span data-ttu-id="f97a0-116">*IsNumericalPasswordValid* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f97a0-116">*IsNumericalPasswordValid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f97a0-117">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f97a0-117">Type: **boolean**</span></span>

<span data-ttu-id="f97a0-118">Valor booleano que es true si la contraseña numérica cumple los requisitos de formato especiales para este valor de autenticación; de lo contrario, el valor es false.</span><span class="sxs-lookup"><span data-stu-id="f97a0-118">A Boolean value that is true if the numerical password meets the special format requirements for this authentication value, otherwise the value is false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f97a0-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f97a0-119">Return value</span></span>

<span data-ttu-id="f97a0-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f97a0-120">Type: **uint32**</span></span>

<span data-ttu-id="f97a0-121">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="f97a0-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="f97a0-122">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f97a0-122">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="f97a0-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="f97a0-123">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="f97a0-124"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="f97a0-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="f97a0-125">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f97a0-125">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f97a0-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f97a0-126">Remarks</span></span>

<span data-ttu-id="f97a0-127">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f97a0-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f97a0-128">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f97a0-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f97a0-129">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="f97a0-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f97a0-130">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f97a0-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f97a0-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f97a0-131">Requirements</span></span>



| <span data-ttu-id="f97a0-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f97a0-132">Requirement</span></span> | <span data-ttu-id="f97a0-133">Value</span><span class="sxs-lookup"><span data-stu-id="f97a0-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f97a0-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f97a0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f97a0-135">Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="f97a0-135">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f97a0-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f97a0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f97a0-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f97a0-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f97a0-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f97a0-138">Namespace</span></span><br/>                | <span data-ttu-id="f97a0-139">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="f97a0-139">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f97a0-140">MOF</span><span class="sxs-lookup"><span data-stu-id="f97a0-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f97a0-141"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f97a0-141"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f97a0-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="f97a0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f97a0-143">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="f97a0-143">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
