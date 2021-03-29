---
description: Libera el identificador de un proveedor de servicios criptográficos (CSP) y, opcionalmente, elimina el contenedor temporal creado por la función GetCryptProvFromCert.
ms.assetid: 4462eef2-7056-4e48-aa96-c46f29b701d6
title: FreeCryptProvFromCert función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 8201de475a4224aea58267405ccde244e56d59f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912041"
---
# <a name="freecryptprovfromcert-function"></a><span data-ttu-id="7abd9-103">FreeCryptProvFromCert función)</span><span class="sxs-lookup"><span data-stu-id="7abd9-103">FreeCryptProvFromCert function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7abd9-104">Esta API está en desuso.</span><span class="sxs-lookup"><span data-stu-id="7abd9-104">This API is deprecated.</span></span> <span data-ttu-id="7abd9-105">Microsoft puede quitar esta API en futuras versiones.</span><span class="sxs-lookup"><span data-stu-id="7abd9-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="7abd9-106">La función **FreeCryptProvFromCert** libera el identificador de un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) y, opcionalmente, elimina el contenedor temporal creado por la función [**GetCryptProvFromCert**](getcryptprovfromcert.md) .</span><span class="sxs-lookup"><span data-stu-id="7abd9-106">The **FreeCryptProvFromCert** function releases the handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and optionally deletes the temporary container created by the [**GetCryptProvFromCert**](getcryptprovfromcert.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="7abd9-107">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="7abd9-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="7abd9-108">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="7abd9-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7abd9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7abd9-109">Syntax</span></span>


```C++
void WINAPI FreeCryptProvFromCert(
  _In_     BOOL       fAcquired,
  _In_     HCRYPTPROV hProv,
  _In_opt_ LPWSTR     pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="7abd9-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7abd9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7abd9-111">*fAcquired* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7abd9-111">*fAcquired* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7abd9-112">Valor que especifica si el identificador del proveedor se adquirió del [*certificado*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7abd9-112">A value that specifies whether the provider handle was acquired from the [*certificate*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="7abd9-113">*hProv* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7abd9-113">*hProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7abd9-114">Puntero a una estructura [**HCRYPTPROV**](hcryptprov.md) para el CSP.</span><span class="sxs-lookup"><span data-stu-id="7abd9-114">A pointer to an [**HCRYPTPROV**](hcryptprov.md) structure for the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="7abd9-115">*pwszCapiProvider* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7abd9-115">*pwszCapiProvider* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7abd9-116">Puntero a una cadena terminada en null para el nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="7abd9-116">A pointer to a null-terminated string for the provider name.</span></span>

</dd> <dt>

<span data-ttu-id="7abd9-117">*dwProviderType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7abd9-117">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7abd9-118">Especifica el tipo de CSP.</span><span class="sxs-lookup"><span data-stu-id="7abd9-118">Specifies the CSP type.</span></span> <span data-ttu-id="7abd9-119">Puede ser cero o uno de los [tipos de proveedor de servicios criptográficos](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="7abd9-119">This can be zero or one of the [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span> <span data-ttu-id="7abd9-120">Si este miembro es cero, el contenedor de claves es uno de los proveedores de almacenamiento de claves CNG.</span><span class="sxs-lookup"><span data-stu-id="7abd9-120">If this member is zero, the key container is one of the CNG key storage providers.</span></span>

</dd> <dt>

<span data-ttu-id="7abd9-121">*pwszTmpContainer* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7abd9-121">*pwszTmpContainer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7abd9-122">Un puntero a una cadena terminada en null para el nombre del contenedor de claves temporal.</span><span class="sxs-lookup"><span data-stu-id="7abd9-122">A pointer to a null-terminated string for the name of the temporary key container.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7abd9-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7abd9-123">Return value</span></span>

<span data-ttu-id="7abd9-124">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7abd9-124">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7abd9-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7abd9-125">Requirements</span></span>



| <span data-ttu-id="7abd9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7abd9-126">Requirement</span></span> | <span data-ttu-id="7abd9-127">Value</span><span class="sxs-lookup"><span data-stu-id="7abd9-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7abd9-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7abd9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7abd9-129">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7abd9-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7abd9-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7abd9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7abd9-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7abd9-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7abd9-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7abd9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7abd9-133"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7abd9-133"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
