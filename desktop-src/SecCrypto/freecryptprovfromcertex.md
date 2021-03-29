---
description: 'Libera el identificador de un proveedor de servicios criptográficos (CSP) o de una clave Cryptography API: Next Generation (CNG).'
ms.assetid: 76cbf8ae-c4ab-43d9-b06d-ea0b2a66368a
title: FreeCryptProvFromCertEx función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCertEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1be6270ebf9320a9c7527736b9fc4894cd50de9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912038"
---
# <a name="freecryptprovfromcertex-function"></a><span data-ttu-id="2a518-103">FreeCryptProvFromCertEx función)</span><span class="sxs-lookup"><span data-stu-id="2a518-103">FreeCryptProvFromCertEx function</span></span>

<span data-ttu-id="2a518-104">La función **FreeCryptProvFromCertEx** libera el identificador de un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) o de una clave Cryptography API: Next Generation (CNG).</span><span class="sxs-lookup"><span data-stu-id="2a518-104">The **FreeCryptProvFromCertEx** function releases the handle either to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) or to a Cryptography API: Next Generation (CNG) key.</span></span>

> [!Note]  
> <span data-ttu-id="2a518-105">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="2a518-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="2a518-106">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="2a518-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2a518-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a518-107">Syntax</span></span>


```C++
void WINAPI FreeCryptProvFromCertEx(
  _In_     BOOL                            fAcquired,
  _In_     HCRYPTPROV_OR_NCRYPT_KEY_HANDLE hProv,
           DWORD                           dwKeySpec,
  _In_opt_ LPWSTR                          pwszCapiProvider,
  _In_     DWORD                           dwProviderType,
  _In_opt_ LPWSTR                          pwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="2a518-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a518-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a518-109">*fAcquired* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2a518-109">*fAcquired* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a518-110">Valor que especifica si el identificador del proveedor se adquirió del [*certificado*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2a518-110">A value that specifies whether the provider handle was acquired from the [*certificate*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a518-111">*hProv* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2a518-111">*hProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a518-112">Identificador de un CSP de CAPICOM o un identificador para una clave CNG.</span><span class="sxs-lookup"><span data-stu-id="2a518-112">A handle to a CAPICOM CSP or a handle to a CNG key.</span></span>

</dd> <dt>

<span data-ttu-id="2a518-113">*dwKeySpec*</span><span class="sxs-lookup"><span data-stu-id="2a518-113">*dwKeySpec*</span></span> 
</dt> <dd>

<span data-ttu-id="2a518-114">Dirección de una variable **DWORD** que recibe información adicional sobre la clave.</span><span class="sxs-lookup"><span data-stu-id="2a518-114">The address of a **DWORD** variable that receives additional information about the key.</span></span> <span data-ttu-id="2a518-115">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2a518-115">This can be one of the following values.</span></span>



| <span data-ttu-id="2a518-116">Value</span><span class="sxs-lookup"><span data-stu-id="2a518-116">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="2a518-117">Significado</span><span class="sxs-lookup"><span data-stu-id="2a518-117">Meaning</span></span>                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <span data-ttu-id="2a518-118"><dt>**EN \_ KEYEXCHANGE**</dt></span><span class="sxs-lookup"><span data-stu-id="2a518-118"><dt>**AT\_KEYEXCHANGE**</dt></span></span> </dl>                     | <span data-ttu-id="2a518-119">El par de claves es un par de intercambio de claves.</span><span class="sxs-lookup"><span data-stu-id="2a518-119">The key pair is a key exchange pair.</span></span><br/>                                                                  |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <span data-ttu-id="2a518-120"><dt>**EN la \_ Signatura**</dt></span><span class="sxs-lookup"><span data-stu-id="2a518-120"><dt>**AT\_SIGNATURE**</dt></span></span> </dl>                           | <span data-ttu-id="2a518-121">El par de claves es un par de firmas.</span><span class="sxs-lookup"><span data-stu-id="2a518-121">The key pair is a signature pair.</span></span><br/>                                                                     |
| <span id="CERT_NCRYPT_KEY_SPEC"></span><span id="cert_ncrypt_key_spec"></span><dl> <span data-ttu-id="2a518-122"><dt>**\_especificación de \_ clave del NCRYPT de CERT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2a518-122"><dt>**CERT\_NCRYPT\_KEY\_SPEC**</dt></span></span> </dl> | <span data-ttu-id="2a518-123">La clave es una clave CNG.</span><span class="sxs-lookup"><span data-stu-id="2a518-123">The key is a CNG key.</span></span><br/> <span data-ttu-id="2a518-124">**Windows Server 2003 y Windows XP:** Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="2a518-124">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2a518-125">*pwszCapiProvider* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2a518-125">*pwszCapiProvider* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a518-126">Puntero a una cadena terminada en null para el nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="2a518-126">A pointer to a null-terminated string for the provider name.</span></span>

</dd> <dt>

<span data-ttu-id="2a518-127">*dwProviderType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2a518-127">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a518-128">Especifica el tipo de CSP.</span><span class="sxs-lookup"><span data-stu-id="2a518-128">Specifies the CSP type.</span></span> <span data-ttu-id="2a518-129">Puede ser cero o uno de los [tipos de proveedor de servicios criptográficos](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="2a518-129">This can be zero or one of the [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span> <span data-ttu-id="2a518-130">Si este miembro es cero, el contenedor de claves es uno de los proveedores de almacenamiento de claves CNG.</span><span class="sxs-lookup"><span data-stu-id="2a518-130">If this member is zero, the key container is one of the CNG key storage providers.</span></span>

</dd> <dt>

<span data-ttu-id="2a518-131">*pwszTmpContainer* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2a518-131">*pwszTmpContainer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2a518-132">Un puntero a una cadena terminada en null para el nombre del contenedor de claves temporal.</span><span class="sxs-lookup"><span data-stu-id="2a518-132">A pointer to a null-terminated string for the name of the temporary key container.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a518-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a518-133">Return value</span></span>

<span data-ttu-id="2a518-134">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2a518-134">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a518-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a518-135">Requirements</span></span>



| <span data-ttu-id="2a518-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a518-136">Requirement</span></span> | <span data-ttu-id="2a518-137">Value</span><span class="sxs-lookup"><span data-stu-id="2a518-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a518-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a518-138">Minimum supported client</span></span><br/> | <span data-ttu-id="2a518-139">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a518-139">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="2a518-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a518-140">Minimum supported server</span></span><br/> | <span data-ttu-id="2a518-141">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a518-141">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2a518-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2a518-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a518-143"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a518-143"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
