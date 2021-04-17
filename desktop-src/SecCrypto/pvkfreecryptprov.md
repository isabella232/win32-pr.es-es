---
description: Libera el identificador de un proveedor de servicios criptográficos (CSP) y, opcionalmente, elimina el contenedor temporal creado por la función PvkGetCryptProv.
ms.assetid: e7dcb5c5-dd80-4810-bf1f-4b7b921fa22c
title: PvkFreeCryptProv función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkFreeCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 70ff29c968fe8f50c813f1da71b2e73a112f25f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688428"
---
# <a name="pvkfreecryptprov-function"></a><span data-ttu-id="d97f3-103">PvkFreeCryptProv función)</span><span class="sxs-lookup"><span data-stu-id="d97f3-103">PvkFreeCryptProv function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d97f3-104">Esta API está en desuso.</span><span class="sxs-lookup"><span data-stu-id="d97f3-104">This API is deprecated.</span></span> <span data-ttu-id="d97f3-105">Microsoft puede quitar esta API en futuras versiones.</span><span class="sxs-lookup"><span data-stu-id="d97f3-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="d97f3-106">La función **PvkFreeCryptProv** libera el identificador de un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) y, opcionalmente, elimina el contenedor temporal creado por la función [**PvkGetCryptProv**](pvkgetcryptprov.md) .</span><span class="sxs-lookup"><span data-stu-id="d97f3-106">The **PvkFreeCryptProv** function releases the handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and optionally deletes the temporary container created by the [**PvkGetCryptProv**](pvkgetcryptprov.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="d97f3-107">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="d97f3-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="d97f3-108">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="d97f3-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d97f3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d97f3-109">Syntax</span></span>


```C++
void WINAPI PvkFreeCryptProv(
  _In_     HCRYPTPROV hProv,
  _In_     LPCWSTR    pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="d97f3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d97f3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d97f3-111">*hProv* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d97f3-111">*hProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d97f3-112">Identificador para el CSP.</span><span class="sxs-lookup"><span data-stu-id="d97f3-112">A handle to the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="d97f3-113">*pwszCapiProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d97f3-113">*pwszCapiProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d97f3-114">Un puntero a una cadena terminada en null para el nombre de CSP.</span><span class="sxs-lookup"><span data-stu-id="d97f3-114">A pointer to a null-terminated string for the CSP name.</span></span>

</dd> <dt>

<span data-ttu-id="d97f3-115">*dwProviderType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d97f3-115">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d97f3-116">Valor **DWORD** que representa el tipo de proveedor de servicios criptográficos.</span><span class="sxs-lookup"><span data-stu-id="d97f3-116">A **DWORD** value that represents the cryptographic provider type.</span></span> <span data-ttu-id="d97f3-117">Para obtener más información, vea [tipos de proveedor de servicios criptográficos](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="d97f3-117">For more information, see [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="d97f3-118">*pwszTmpContainer* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d97f3-118">*pwszTmpContainer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d97f3-119">Un puntero a una cadena terminada en null para el nombre del contenedor de claves temporal.</span><span class="sxs-lookup"><span data-stu-id="d97f3-119">A pointer to a null-terminated string for the temporary key container name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d97f3-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d97f3-120">Return value</span></span>

<span data-ttu-id="d97f3-121">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d97f3-121">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d97f3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d97f3-122">Requirements</span></span>



| <span data-ttu-id="d97f3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d97f3-123">Requirement</span></span> | <span data-ttu-id="d97f3-124">Value</span><span class="sxs-lookup"><span data-stu-id="d97f3-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d97f3-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d97f3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d97f3-126">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d97f3-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d97f3-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d97f3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d97f3-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d97f3-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d97f3-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d97f3-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d97f3-130"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d97f3-130"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
