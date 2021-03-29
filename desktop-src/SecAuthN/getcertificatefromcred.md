---
description: Obtiene el certificado de la credencial de usuario.
ms.assetid: 3C79D049-89DC-4AF5-8C0A-5B7EBBBD69D3
title: Función GetCertificateFromCred (Lsaidprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificateFromCred
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: 1120e7859080657e2a04202e01a01464694a3450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648303"
---
# <a name="getcertificatefromcred-function"></a><span data-ttu-id="5d317-103">GetCertificateFromCred función)</span><span class="sxs-lookup"><span data-stu-id="5d317-103">GetCertificateFromCred function</span></span>

<span data-ttu-id="5d317-104">Obtiene el certificado de la credencial de usuario.</span><span class="sxs-lookup"><span data-stu-id="5d317-104">Gets the certificate from the user credential.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d317-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d317-105">Syntax</span></span>


```C++
NTSTATUS GetCertificateFromCred(
  _In_  PVOID  ProviderHandle,
  _In_  HANDLE ClientToken,
  _In_  PVOID  SuppliedCred,
  _In_  ULONG  SuppliedCredSize,
  _Out_ PVOID  *CertContext
);
```



## <a name="parameters"></a><span data-ttu-id="5d317-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d317-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d317-107">*ProviderHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5d317-107">*ProviderHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d317-108">Identificador del proveedor de identidades.</span><span class="sxs-lookup"><span data-stu-id="5d317-108">Identity provider handle.</span></span>

</dd> <dt>

<span data-ttu-id="5d317-109">*ClientToken* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5d317-109">*ClientToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d317-110">Token del llamador que está recuperando el certificado.</span><span class="sxs-lookup"><span data-stu-id="5d317-110">Token of the caller who is retrieving the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="5d317-111">*SuppliedCred* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5d317-111">*SuppliedCred* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d317-112">Puntero a una estructura [**de \_ \_ credenciales proporcionada por SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) que contiene la credencial de un identificador en línea cuyo certificado se solicita.</span><span class="sxs-lookup"><span data-stu-id="5d317-112">A pointer to a [**SECPKG\_SUPPLIED\_CREDENTIAL**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) structure that contains the credential of an online ID whose certificate is requested.</span></span> <span data-ttu-id="5d317-113">El proveedor de identidades debe validar los datos de entrada como si provinieran de un origen que no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="5d317-113">The identity provider must validate the input data as if it is coming from an untrusted source.</span></span>

</dd> <dt>

<span data-ttu-id="5d317-114">*SuppliedCredSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5d317-114">*SuppliedCredSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d317-115">Tamaño, en bytes, del búfer *SuppliedCred* .</span><span class="sxs-lookup"><span data-stu-id="5d317-115">The size, in bytes, of the *SuppliedCred* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5d317-116">*CertContext* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5d317-116">*CertContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d317-117">Si la función se ejecuta correctamente, este parámetro es un puntero al puntero de contexto CCERT devuelto \_ .</span><span class="sxs-lookup"><span data-stu-id="5d317-117">If the function succeeds, this parameter is a pointer to the returned CCERT\_CONTEXT pointer.</span></span> <span data-ttu-id="5d317-118">Cuando haya terminado de usar el contexto del certificado, suéltelo llamando a la función [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) .</span><span class="sxs-lookup"><span data-stu-id="5d317-118">When you have finished using the certificate context, release it by calling the [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d317-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d317-119">Return value</span></span>

<span data-ttu-id="5d317-120">Si la función se ejecuta correctamente, la función devuelve el estado \_ Success.</span><span class="sxs-lookup"><span data-stu-id="5d317-120">If the function succeeds, the function returns STATUS\_SUCCESS.</span></span>

<span data-ttu-id="5d317-121">Si se produce un error en la función, la función puede devolver uno de los siguientes códigos de error de NTSTATUS.</span><span class="sxs-lookup"><span data-stu-id="5d317-121">If the function fails, the function may return one of the following NTSTATUS error codes.</span></span>



| <span data-ttu-id="5d317-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d317-122">Return value</span></span>                                                                                            | <span data-ttu-id="5d317-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d317-123">Description</span></span>                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5d317-124"><dt>ESTADO \_ no \_ admitido</dt></span><span class="sxs-lookup"><span data-stu-id="5d317-124"><dt>STATUS\_NOT\_SUPPORTED</dt></span></span> </dl>       | <span data-ttu-id="5d317-125">El proveedor de identidades no reconoce el tipo de credencial de la credencial proporcionada.</span><span class="sxs-lookup"><span data-stu-id="5d317-125">The identity provider does not recognize the credential type of the supplied credential.</span></span> <span data-ttu-id="5d317-126">LSA probará el siguiente proveedor de identidades.</span><span class="sxs-lookup"><span data-stu-id="5d317-126">LSA will try the next identity provider.</span></span><br/>                                           |
| <dl> <span data-ttu-id="5d317-127"><dt>error de inicio de sesión de estado \_ \_</dt></span><span class="sxs-lookup"><span data-stu-id="5d317-127"><dt>STATUS\_LOGON\_FAILURE</dt></span></span> </dl>       | <span data-ttu-id="5d317-128">La credencial es incorrecta.</span><span class="sxs-lookup"><span data-stu-id="5d317-128">The credential is incorrect.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="5d317-129"><dt>ESTADO \_ parámetro no válido \_</dt></span><span class="sxs-lookup"><span data-stu-id="5d317-129"><dt>STATUS\_INVALID\_PARAMETER</dt></span></span> </dl>   | <span data-ttu-id="5d317-130">Un parámetro no es válido.</span><span class="sxs-lookup"><span data-stu-id="5d317-130">A parameter is not valid.</span></span> <span data-ttu-id="5d317-131">La credencial puede tener un formato incorrecto y no estar en la estructura [**de \_ \_ credenciales proporcionada por SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) definida.</span><span class="sxs-lookup"><span data-stu-id="5d317-131">The credential may be in an incorrect format and not in the defined [**SECPKG\_SUPPLIED\_CREDENTIAL**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) structure.</span></span><br/> |
| <dl> <span data-ttu-id="5d317-132"><dt>Estado de \_ red no \_ accesible</dt></span><span class="sxs-lookup"><span data-stu-id="5d317-132"><dt>STATUS\_NETWORK\_UNREACHABLE</dt></span></span> </dl> | <span data-ttu-id="5d317-133">El proveedor de identidades no puede ponerse en contacto con la nube para obtener el certificado.</span><span class="sxs-lookup"><span data-stu-id="5d317-133">The identity provider cannot contact the cloud to obtain the certificate.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="5d317-134"><dt>contraseña de estado \_ \_ expirada</dt></span><span class="sxs-lookup"><span data-stu-id="5d317-134"><dt>STATUS\_PASSWORD\_EXPIRED</dt></span></span> </dl>    | <span data-ttu-id="5d317-135">La contraseña de la cuenta ha caducado.</span><span class="sxs-lookup"><span data-stu-id="5d317-135">The account password has expired.</span></span><br/>                                                                                                                                           |
| <dl> <span data-ttu-id="5d317-136"><dt>cuenta de estado \_ \_ bloqueada \_</dt></span><span class="sxs-lookup"><span data-stu-id="5d317-136"><dt>STATUS\_ACCOUNT\_LOCKED\_OUT</dt></span></span> </dl> | <span data-ttu-id="5d317-137">La cuenta se ha bloqueado.</span><span class="sxs-lookup"><span data-stu-id="5d317-137">The account has been locked out.</span></span> <br/>                                                                                                                                           |
| <dl> <span data-ttu-id="5d317-138"><dt>Otros</dt></span><span class="sxs-lookup"><span data-stu-id="5d317-138"><dt>Others</dt></span></span> </dl>                       | <span data-ttu-id="5d317-139">Otros códigos de error específicos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="5d317-139">Other provider-specific error codes.</span></span> <br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="5d317-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d317-140">Remarks</span></span>

<span data-ttu-id="5d317-141">Antes de recuperar el certificado de la nube, el proveedor de identidades debe comprobar que hay un certificado válido para este usuario en el almacén de certificados "mi" del usuario.</span><span class="sxs-lookup"><span data-stu-id="5d317-141">Before fetching the certificate from the cloud, the identity provider should check that there is a valid certificate for this user in the user's "MY" certificate store.</span></span> <span data-ttu-id="5d317-142">Si existe un certificado válido, el proveedor debe devolver este certificado para evitar el tráfico de red innecesario.</span><span class="sxs-lookup"><span data-stu-id="5d317-142">If a valid certificate exists, the provider should return this certificate to avoid unnecessary network traffic.</span></span>

<span data-ttu-id="5d317-143">El proveedor de identidades también puede almacenar en caché el certificado localmente siempre que esté protegido por el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="5d317-143">The identity provider can also cache the certificate locally as long as it is protected from the current user.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d317-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d317-144">Requirements</span></span>



| <span data-ttu-id="5d317-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d317-145">Requirement</span></span> | <span data-ttu-id="5d317-146">Value</span><span class="sxs-lookup"><span data-stu-id="5d317-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d317-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d317-147">Minimum supported client</span></span><br/> | <span data-ttu-id="5d317-148">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="5d317-148">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5d317-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d317-149">Minimum supported server</span></span><br/> | <span data-ttu-id="5d317-150">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="5d317-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5d317-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d317-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d317-152"><dt>Lsaidprov. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d317-152"><dt>Lsaidprov.h</dt></span></span> </dl> |



 

