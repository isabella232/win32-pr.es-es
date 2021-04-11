---
description: Crea un contenedor temporal en el proveedor de servicios criptográficos (CSP) y carga una clave privada de la memoria en el contenedor.
ms.assetid: 9388b49b-fad4-4499-a391-fe58ed672552
title: PvkPrivateKeyAcquireContextFromMemory función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeyAcquireContextFromMemory
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1552d1e35845ffb7407d11d6e520b914ab805d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361296"
---
# <a name="pvkprivatekeyacquirecontextfrommemory-function"></a><span data-ttu-id="79034-103">PvkPrivateKeyAcquireContextFromMemory función)</span><span class="sxs-lookup"><span data-stu-id="79034-103">PvkPrivateKeyAcquireContextFromMemory function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="79034-104">Esta API está en desuso.</span><span class="sxs-lookup"><span data-stu-id="79034-104">This API is deprecated.</span></span> <span data-ttu-id="79034-105">Microsoft puede quitar esta API en futuras versiones.</span><span class="sxs-lookup"><span data-stu-id="79034-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="79034-106">La función **PvkPrivateKeyAcquireContextFromMemory** crea un contenedor temporal en el [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) y carga una [*clave privada*](../secgloss/p-gly.md) de la memoria en el contenedor.</span><span class="sxs-lookup"><span data-stu-id="79034-106">The **PvkPrivateKeyAcquireContextFromMemory** function creates a temporary container in the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and loads a [*private key*](../secgloss/p-gly.md) from memory into the container.</span></span>

> [!Note]  
> <span data-ttu-id="79034-107">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="79034-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="79034-108">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="79034-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="79034-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79034-109">Syntax</span></span>


```C++
BOOL WINAPI PvkPrivateKeyAcquireContextFromMemory(
  _In_        LPCWSTR    pwszProvName,
  _In_        DWORD      dwProvType,
  _In_        BYTE       *pbData,
  _In_        DWORD      cbData,
  _In_        HWND       hwndOwner,
  _In_        LPCWSTR    pwszKeyName,
  _Inout_opt_ DWORD      *pdwKeySpec,
  _Out_       HCRYPTPROV *phCryptProv,
  _Out_       LPTSTR     *ppwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="79034-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79034-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79034-111">*pwszProvName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79034-111">*pwszProvName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79034-112">Un puntero a una cadena terminada en null que contiene el nombre del CSP cuyo tipo se solicita en *dwProvType*.</span><span class="sxs-lookup"><span data-stu-id="79034-112">A pointer to a null-terminated string that contains the name of the CSP whose type is requested in *dwProvType*.</span></span>

</dd> <dt>

<span data-ttu-id="79034-113">*dwProvType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79034-113">*dwProvType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79034-114">Valor **DWORD** para el tipo de CSP.</span><span class="sxs-lookup"><span data-stu-id="79034-114">A **DWORD** value for the CSP type.</span></span> <span data-ttu-id="79034-115">Para obtener más información sobre los tipos de CSP, consulte [tipos de proveedor de servicios criptográficos](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="79034-115">For more information about CSP types, see [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="79034-116">*pbData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79034-116">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79034-117">Un puntero a un búfer para recibir los datos de contexto.</span><span class="sxs-lookup"><span data-stu-id="79034-117">A pointer to a buffer to receive the context data.</span></span> <span data-ttu-id="79034-118">El autor de la llamada debe proporcionar este recurso.</span><span class="sxs-lookup"><span data-stu-id="79034-118">The caller must provide this resource.</span></span>

</dd> <dt>

<span data-ttu-id="79034-119">*cbData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79034-119">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79034-120">Valor **DWORD** que especifica el tamaño, en bytes, del búfer *pbData* .</span><span class="sxs-lookup"><span data-stu-id="79034-120">A **DWORD** value that specifies the size, in bytes, of the *pbData* buffer.</span></span> <span data-ttu-id="79034-121">El autor de la llamada debe proporcionar este valor.</span><span class="sxs-lookup"><span data-stu-id="79034-121">The caller must provide this value.</span></span>

</dd> <dt>

<span data-ttu-id="79034-122">*hwndOwner* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79034-122">*hwndOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79034-123">Si se requiere una contraseña para descifrar los datos de contexto a los que apunta el parámetro *pbData* , este parámetro es un identificador del elemento primario del cuadro de diálogo. de lo contrario, es **null**.</span><span class="sxs-lookup"><span data-stu-id="79034-123">If a password is required to decrypt the context data pointed to by the *pbData* parameter, this parameter is a handle to the parent of the dialog box; otherwise, it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="79034-124">*pwszKeyName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79034-124">*pwszKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79034-125">Puntero a una cadena terminada en null que contiene el nombre de la clave que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="79034-125">A pointer to a null-terminated string that contains the name of the key to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="79034-126">*pdwKeySpec* \[ in, out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="79034-126">*pdwKeySpec* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="79034-127">Un puntero a un valor **DWORD** que especifica el tipo de clave.</span><span class="sxs-lookup"><span data-stu-id="79034-127">A pointer to a **DWORD** value that specifies the type of key.</span></span> <span data-ttu-id="79034-128">Entre los valores posibles se incluyen **en \_ KEYEXCHANGE** o **en la \_ signatura**.</span><span class="sxs-lookup"><span data-stu-id="79034-128">Possible values include **AT\_KEYEXCHANGE** or **AT\_SIGNATURE**.</span></span>

</dd> <dt>

<span data-ttu-id="79034-129">*phCryptProv* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="79034-129">*phCryptProv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79034-130">Un puntero a un identificador para el CSP.</span><span class="sxs-lookup"><span data-stu-id="79034-130">A pointer to a handle for the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="79034-131">*ppwszTmpContainer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="79034-131">*ppwszTmpContainer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79034-132">Dirección de un puntero a una cadena terminada en null para el nombre del contenedor temporal.</span><span class="sxs-lookup"><span data-stu-id="79034-132">The address of a pointer to a null-terminated string for the temporary container name.</span></span> <span data-ttu-id="79034-133">La función **PvkPrivateKeyAcquireContextFromMemory** proporciona el búfer para esta cadena y lo inicializa.</span><span class="sxs-lookup"><span data-stu-id="79034-133">The **PvkPrivateKeyAcquireContextFromMemory** function provides the buffer for this string and initializes it.</span></span> <span data-ttu-id="79034-134">Al llamar a **PvkPrivateKeyAcquireContextFromMemory**, la dirección debe apuntar a un valor **null** .</span><span class="sxs-lookup"><span data-stu-id="79034-134">When calling **PvkPrivateKeyAcquireContextFromMemory**, the address should point to a **NULL** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79034-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79034-135">Return value</span></span>

<span data-ttu-id="79034-136">Cuando se realiza correctamente, esta función devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="79034-136">Upon success, this function returns **TRUE**.</span></span> <span data-ttu-id="79034-137">La función **PvkPrivateKeyAcquireContextFromMemory** devuelve **false** si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="79034-137">The **PvkPrivateKeyAcquireContextFromMemory** function returns **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="79034-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79034-138">Requirements</span></span>



| <span data-ttu-id="79034-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="79034-139">Requirement</span></span> | <span data-ttu-id="79034-140">Value</span><span class="sxs-lookup"><span data-stu-id="79034-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79034-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79034-141">Minimum supported client</span></span><br/> | <span data-ttu-id="79034-142">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="79034-142">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="79034-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79034-143">Minimum supported server</span></span><br/> | <span data-ttu-id="79034-144">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="79034-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="79034-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79034-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79034-146"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79034-146"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
