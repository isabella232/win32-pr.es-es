---
description: Obtiene la huella digital de la clave raíz de almacenamiento para un módulo determinado de la parte pública de la clave raíz de almacenamiento de TPM.
ms.assetid: 08CBEB19-ECF5-4E43-B4A4-0F35987173E1
title: 'Win32_Tpm:: GetSrkADThumbprint (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetSrkADThumbprint
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 81e1ec53596a3d5ce469d412e9bd7ca17e1ad8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666377"
---
# <a name="win32_tpmgetsrkadthumbprint-method"></a><span data-ttu-id="ad9fa-103">Win32 \_ TPM:: GetSrkADThumbprint (método)</span><span class="sxs-lookup"><span data-stu-id="ad9fa-103">Win32\_Tpm::GetSrkADThumbprint method</span></span>

<span data-ttu-id="ad9fa-104">Obtiene la huella digital de la clave raíz de almacenamiento para un módulo determinado de la parte pública de la clave raíz de almacenamiento de TPM.</span><span class="sxs-lookup"><span data-stu-id="ad9fa-104">Gets the Storage root key thumbprint for a given modulus of the public portion of the TPM Storage Root Key.</span></span> <span data-ttu-id="ad9fa-105">La huella digital se utiliza para indizar las claves raíz de almacenamiento en el servidor de Active Directory si la Active Directory copia de seguridad de la información de autorización de propietario de TPM se habilita a través de directiva de grupo configuración.</span><span class="sxs-lookup"><span data-stu-id="ad9fa-105">The thumbprint is used to index the Storage Root Keys on the Active Directory server if the Active Directory backup of TPM owner authorization information is enabled through Group Policy setting.</span></span>

> [!Note]  
> <span data-ttu-id="ad9fa-106">A partir de Windows 10, versión 1607, nunca se realiza una copia de seguridad de la autorización de propietario de TPM en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ad9fa-106">Beginning with Windows 10, version 1607, the TPM owner authorization is never backed up to Active Directory.</span></span>

 

<span data-ttu-id="ad9fa-107">Este método solo es accesible para los administradores locales.</span><span class="sxs-lookup"><span data-stu-id="ad9fa-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad9fa-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad9fa-108">Syntax</span></span>


```C++
uint32 GetSrkADThumbprint(
  [in]  uint8 SrkPublicKeyModulus,
  [out] uint8 SrkADThumbprint
);
```



## <a name="parameters"></a><span data-ttu-id="ad9fa-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad9fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad9fa-110">*SrkPublicKeyModulus* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ad9fa-110">*SrkPublicKeyModulus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9fa-111">El módulo de la parte pública de la clave raíz de almacenamiento de TPM.</span><span class="sxs-lookup"><span data-stu-id="ad9fa-111">The modulus of the public portion of the TPM Storage Root Key.</span></span> <span data-ttu-id="ad9fa-112">También se puede obtener mediante el método [**GetSrkPublicKeyModulus**](win32-tpm-getsrkpublickeymodulus.md) de la clase [ \_ TPM de Win32](win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="ad9fa-112">It can also be obtained using the [**GetSrkPublicKeyModulus**](win32-tpm-getsrkpublickeymodulus.md) method of the [Win32\_TPM](win32-tpm.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="ad9fa-113">*SrkADThumbprint* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ad9fa-113">*SrkADThumbprint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9fa-114">Devuelve una matriz de 20 bytes que contiene la huella digital de la clave raíz de almacenamiento para el módulo especificado.</span><span class="sxs-lookup"><span data-stu-id="ad9fa-114">Returns a 20-byte array containing the storage root key thumbprint for the given modulus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad9fa-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad9fa-115">Return value</span></span>

<span data-ttu-id="ad9fa-116">Se pueden devolver todos los errores de TPM, así como los errores específicos de los [servicios base de TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="ad9fa-116">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="ad9fa-117">A continuación se enumeran los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="ad9fa-117">Common return codes are listed below.</span></span>



| <span data-ttu-id="ad9fa-118">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad9fa-118">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="ad9fa-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad9fa-119">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="ad9fa-120"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="ad9fa-120"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="ad9fa-121">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ad9fa-121">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ad9fa-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad9fa-122">Remarks</span></span>

<span data-ttu-id="ad9fa-123">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ad9fa-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ad9fa-124">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="ad9fa-124">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="ad9fa-125">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="ad9fa-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ad9fa-126">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="ad9fa-126">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad9fa-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad9fa-127">Requirements</span></span>



| <span data-ttu-id="ad9fa-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad9fa-128">Requirement</span></span> | <span data-ttu-id="ad9fa-129">Value</span><span class="sxs-lookup"><span data-stu-id="ad9fa-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad9fa-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad9fa-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ad9fa-131">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="ad9fa-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ad9fa-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad9fa-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ad9fa-133">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="ad9fa-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ad9fa-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ad9fa-134">Namespace</span></span><br/>                | <span data-ttu-id="ad9fa-135">\\\\.\\ \\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="ad9fa-135">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="ad9fa-136">MOF</span><span class="sxs-lookup"><span data-stu-id="ad9fa-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad9fa-137"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad9fa-137"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad9fa-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ad9fa-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad9fa-139"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="ad9fa-139"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad9fa-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad9fa-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad9fa-141">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="ad9fa-141">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
