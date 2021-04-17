---
description: Guarda una clave privada y su correspondiente clave pública en un archivo especificado.
ms.assetid: 491a128a-b4aa-4cca-a835-d0e8d7df6720
title: PvkPrivateKeySave función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeySave
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: ef60c3f615a704248fbcb8630322fa6b598141ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688036"
---
# <a name="pvkprivatekeysave-function"></a><span data-ttu-id="965dc-103">PvkPrivateKeySave función)</span><span class="sxs-lookup"><span data-stu-id="965dc-103">PvkPrivateKeySave function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="965dc-104">Esta API está en desuso.</span><span class="sxs-lookup"><span data-stu-id="965dc-104">This API is deprecated.</span></span> <span data-ttu-id="965dc-105">Microsoft puede quitar esta API en futuras versiones.</span><span class="sxs-lookup"><span data-stu-id="965dc-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="965dc-106">La función **PvkPrivateKeySave** guarda una [*clave privada*](../secgloss/p-gly.md) y su correspondiente [*clave pública*](../secgloss/p-gly.md) en un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="965dc-106">The **PvkPrivateKeySave** function saves a [*private key*](../secgloss/p-gly.md) and its corresponding [*public key*](../secgloss/p-gly.md) to a specified file.</span></span>

> [!Note]  
> <span data-ttu-id="965dc-107">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="965dc-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="965dc-108">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="965dc-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="965dc-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="965dc-109">Syntax</span></span>


```C++
BOOL WINAPI PvkPrivateKeySave(
  _In_ HCRYPTPROV hCryptProv,
  _In_ HANDLE     hFile,
  _In_ DWORD      dwKeySpec,
  _In_ HWND       hwndOwner,
  _In_ LPCWSTR    pwszKeyName,
  _In_ DWORD      dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="965dc-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="965dc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="965dc-111">*hCryptProv* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="965dc-111">*hCryptProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="965dc-112">Identificador de un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="965dc-112">A handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

</dd> <dt>

<span data-ttu-id="965dc-113">*hFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="965dc-113">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="965dc-114">Identificador de un archivo creado con permisos de lectura y escritura iniciales y permisos de solo lectura posteriores.</span><span class="sxs-lookup"><span data-stu-id="965dc-114">A handle to a file created with initial read/write permission and subsequent read-only permission.</span></span>

</dd> <dt>

<span data-ttu-id="965dc-115">*dwKeySpec* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="965dc-115">*dwKeySpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="965dc-116">Entero largo para el tipo de clave.</span><span class="sxs-lookup"><span data-stu-id="965dc-116">A long integer for the type of key.</span></span> <span data-ttu-id="965dc-117">Entre los valores posibles se incluyen **en \_ KEYEXCHANGE** o **en la \_ signatura**.</span><span class="sxs-lookup"><span data-stu-id="965dc-117">Possible values include **AT\_KEYEXCHANGE** or **AT\_SIGNATURE**.</span></span>

</dd> <dt>

<span data-ttu-id="965dc-118">*hwndOwner* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="965dc-118">*hwndOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="965dc-119">Si se requiere una contraseña para cifrar la clave privada, este parámetro es un identificador del elemento primario del cuadro de diálogo. de lo contrario, es **null**.</span><span class="sxs-lookup"><span data-stu-id="965dc-119">If a password is required to encrypt the private key, this parameter is a handle to the parent of the dialog box; otherwise, it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="965dc-120">*pwszKeyName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="965dc-120">*pwszKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="965dc-121">Puntero a una cadena terminada en null para el nombre de la clave que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="965dc-121">A pointer to a null-terminated string for the name of the key to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="965dc-122">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="965dc-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="965dc-123">Valor **DWORD** que especifica opciones adicionales para la función.</span><span class="sxs-lookup"><span data-stu-id="965dc-123">A **DWORD** value that specifies additional options for the function.</span></span> <span data-ttu-id="965dc-124">Para obtener más información, vea el parámetro *dwFlags* en [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span><span class="sxs-lookup"><span data-stu-id="965dc-124">For more information, see the *dwFlags* parameter in [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="965dc-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="965dc-125">Return value</span></span>

<span data-ttu-id="965dc-126">Cuando se realiza correctamente, esta función devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="965dc-126">Upon success, this function returns **TRUE**.</span></span> <span data-ttu-id="965dc-127">La función **PvkPrivateKeySave** devuelve **false** si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="965dc-127">The **PvkPrivateKeySave** function returns **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="965dc-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="965dc-128">Requirements</span></span>



| <span data-ttu-id="965dc-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="965dc-129">Requirement</span></span> | <span data-ttu-id="965dc-130">Value</span><span class="sxs-lookup"><span data-stu-id="965dc-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="965dc-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="965dc-131">Minimum supported client</span></span><br/> | <span data-ttu-id="965dc-132">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="965dc-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="965dc-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="965dc-133">Minimum supported server</span></span><br/> | <span data-ttu-id="965dc-134">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="965dc-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="965dc-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="965dc-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="965dc-136"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="965dc-136"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
