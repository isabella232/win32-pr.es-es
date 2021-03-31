---
description: Obtiene un identificador para un proveedor de servicios criptográficos (CSP) basado en un archivo de clave privada o un nombre de contenedor de claves.
ms.assetid: 82cdaa6f-e747-4c9d-8d2d-5fa206891eed
title: PvkGetCryptProv función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkGetCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 026b31d021dc6ff2569ad9ce8f17d2e7f0d17b29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913618"
---
# <a name="pvkgetcryptprov-function"></a><span data-ttu-id="34a67-103">PvkGetCryptProv función)</span><span class="sxs-lookup"><span data-stu-id="34a67-103">PvkGetCryptProv function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="34a67-104">Esta API está en desuso.</span><span class="sxs-lookup"><span data-stu-id="34a67-104">This API is deprecated.</span></span> <span data-ttu-id="34a67-105">Microsoft puede quitar esta API en futuras versiones.</span><span class="sxs-lookup"><span data-stu-id="34a67-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="34a67-106">La función **PvkGetCryptProv** obtiene un identificador de un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) basado en un archivo de [*clave privada*](../secgloss/p-gly.md) o un nombre de contenedor de claves.</span><span class="sxs-lookup"><span data-stu-id="34a67-106">The **PvkGetCryptProv** function gets a handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) based on either a [*private key*](../secgloss/p-gly.md) file or a key container name.</span></span>

> [!Note]  
> <span data-ttu-id="34a67-107">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="34a67-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="34a67-108">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="34a67-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="34a67-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="34a67-109">Syntax</span></span>


```C++
HRESULT WINAPI PvkGetCryptProv(
  _In_      HWND       hwnd,
  _In_      LPCWSTR    pwszCaption,
  _In_      LPCWSTR    pwszCapiProvider,
  _In_      DWORD      dwProviderType,
  _In_      LPCWSTR    pwszPvkFile,
  _In_      LPCWSTR    pwszKeyContainerName,
  _Out_     DWORD      *pdwKeySpec,
  _Out_opt_ LPWSTR     *ppwszTmpContainer,
  _Out_     HCRYPTPROV *phCryptProv
);
```



## <a name="parameters"></a><span data-ttu-id="34a67-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34a67-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34a67-111">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="34a67-111">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34a67-112">Si se requiere una contraseña para descifrar el archivo de clave privada, este parámetro es un identificador del cuadro de diálogo de contraseña principal. de lo contrario, es **null**.</span><span class="sxs-lookup"><span data-stu-id="34a67-112">If a password is required to decrypt the private key file, this parameter is a handle to the parent of the password dialog box; otherwise, it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="34a67-113">*pwszCaption* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="34a67-113">*pwszCaption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34a67-114">Puntero a una cadena terminada en null para la leyenda del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="34a67-114">A pointer to a null-terminated string for the dialog box caption.</span></span>

</dd> <dt>

<span data-ttu-id="34a67-115">*pwszCapiProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="34a67-115">*pwszCapiProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34a67-116">Un puntero a una cadena terminada en null para el nombre de CSP.</span><span class="sxs-lookup"><span data-stu-id="34a67-116">A pointer to a null-terminated string for the CSP name.</span></span>

</dd> <dt>

<span data-ttu-id="34a67-117">*dwProviderType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="34a67-117">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34a67-118">Valor **DWORD** que representa el tipo de proveedor de servicios criptográficos.</span><span class="sxs-lookup"><span data-stu-id="34a67-118">A **DWORD** value that represents the cryptographic provider type.</span></span> <span data-ttu-id="34a67-119">Para obtener más información, vea [tipos de proveedor de servicios criptográficos](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="34a67-119">For more information, see [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="34a67-120">*pwszPvkFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="34a67-120">*pwszPvkFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34a67-121">Puntero a una cadena terminada en null que contiene el nombre de un archivo de clave privada.</span><span class="sxs-lookup"><span data-stu-id="34a67-121">A pointer to a null-terminated string that contains the name of a private key file.</span></span>

</dd> <dt>

<span data-ttu-id="34a67-122">*pwszKeyContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="34a67-122">*pwszKeyContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34a67-123">Un puntero a una cadena terminada en null para el nombre del contenedor de claves privadas.</span><span class="sxs-lookup"><span data-stu-id="34a67-123">A pointer to a null-terminated string for the private key container name.</span></span>

</dd> <dt>

<span data-ttu-id="34a67-124">*pdwKeySpec* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="34a67-124">*pdwKeySpec* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34a67-125">Un puntero a un valor **DWORD** para el tipo de clave del contenedor devuelto con *phCryptProv* y *ppwszTmpContainer*.</span><span class="sxs-lookup"><span data-stu-id="34a67-125">A pointer to a **DWORD** value for the type of key of the container returned with *phCryptProv* and *ppwszTmpContainer*.</span></span>

</dd> <dt>

<span data-ttu-id="34a67-126">*ppwszTmpContainer* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="34a67-126">*ppwszTmpContainer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="34a67-127">Dirección de un puntero a una cadena terminada en null para el nombre del contenedor de claves temporal.</span><span class="sxs-lookup"><span data-stu-id="34a67-127">The address of a pointer to a null-terminated string for the temporary key container name.</span></span> <span data-ttu-id="34a67-128">La función **PvkGetCryptProv** proporciona e inicializa el contenedor temporal.</span><span class="sxs-lookup"><span data-stu-id="34a67-128">The **PvkGetCryptProv** function provides and initializes the temporary container.</span></span> <span data-ttu-id="34a67-129">Al llamar a **PvkGetCryptProv**, la dirección debe apuntar a un valor **null** .</span><span class="sxs-lookup"><span data-stu-id="34a67-129">When calling **PvkGetCryptProv**, the address should point to a **NULL** value.</span></span>

</dd> <dt>

<span data-ttu-id="34a67-130">*phCryptProv* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="34a67-130">*phCryptProv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34a67-131">Un puntero a un identificador para el CSP.</span><span class="sxs-lookup"><span data-stu-id="34a67-131">A pointer to a handle for the CSP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34a67-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34a67-132">Return value</span></span>

<span data-ttu-id="34a67-133">Si el método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="34a67-133">If the method succeeds, it returns **S\_OK**.</span></span>

<span data-ttu-id="34a67-134">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="34a67-134">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="34a67-135">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="34a67-135">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="34a67-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="34a67-136">Remarks</span></span>

<span data-ttu-id="34a67-137">La función **PvkGetCryptProv** primero intenta obtener el identificador de proveedor desde el nombre del contenedor de claves especificado por el parámetro *pwszKeyContainerName* .</span><span class="sxs-lookup"><span data-stu-id="34a67-137">The **PvkGetCryptProv** function first tries to get the provider handle from the key container name specified by the *pwszKeyContainerName* parameter.</span></span> <span data-ttu-id="34a67-138">Si pasa **null** para el parámetro *pwszKeyContainerName* , **PvkGetCryptProv** intenta obtener el proveedor del archivo de clave privada especificado en el parámetro *pwszPvkFile* .</span><span class="sxs-lookup"><span data-stu-id="34a67-138">If you pass **NULL** for the *pwszKeyContainerName* parameter, **PvkGetCryptProv** tries to get the provider from the private key file specified in the *pwszPvkFile* parameter.</span></span>

<span data-ttu-id="34a67-139">Cuando haya terminado de usar el CSP, libere el identificador del proveedor y el contenedor de claves temporal mediante una llamada a la función [**PvkFreeCryptProv**](pvkfreecryptprov.md) .</span><span class="sxs-lookup"><span data-stu-id="34a67-139">When you have finished using the CSP, free the provider handle and temporary key container by calling the [**PvkFreeCryptProv**](pvkfreecryptprov.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="34a67-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34a67-140">Requirements</span></span>



| <span data-ttu-id="34a67-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="34a67-141">Requirement</span></span> | <span data-ttu-id="34a67-142">Value</span><span class="sxs-lookup"><span data-stu-id="34a67-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34a67-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34a67-143">Minimum supported client</span></span><br/> | <span data-ttu-id="34a67-144">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="34a67-144">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="34a67-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34a67-145">Minimum supported server</span></span><br/> | <span data-ttu-id="34a67-146">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="34a67-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="34a67-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="34a67-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34a67-148"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34a67-148"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
