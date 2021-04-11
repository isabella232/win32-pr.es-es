---
description: Llama a la función GetLastError y convierte el código de retorno en HRESULT.
ms.assetid: 7b8eab85-212b-44bc-9d1b-60587652380d
title: SignError función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignError
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 7a405bef4666721e485e8b5ad6905209b2244bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082183"
---
# <a name="signerror-function"></a><span data-ttu-id="2156d-103">SignError función)</span><span class="sxs-lookup"><span data-stu-id="2156d-103">SignError function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2156d-104">Esta API está en desuso.</span><span class="sxs-lookup"><span data-stu-id="2156d-104">This API is deprecated.</span></span> <span data-ttu-id="2156d-105">Microsoft puede quitar esta API en futuras versiones.</span><span class="sxs-lookup"><span data-stu-id="2156d-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="2156d-106">La función **SignError** llama a la función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) y convierte el código de retorno en **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2156d-106">The **SignError** function calls the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function and converts the return code to an **HRESULT**.</span></span>

> [!Note]  
> <span data-ttu-id="2156d-107">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="2156d-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="2156d-108">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="2156d-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2156d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2156d-109">Syntax</span></span>


```C++
HRESULT WINAPI SignError(void);
```



## <a name="parameters"></a><span data-ttu-id="2156d-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2156d-110">Parameters</span></span>

<span data-ttu-id="2156d-111">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2156d-111">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2156d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2156d-112">Return value</span></span>

<span data-ttu-id="2156d-113">Si el método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="2156d-113">If the method succeeds, it returns **S\_OK**.</span></span>

<span data-ttu-id="2156d-114">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="2156d-114">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="2156d-115">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="2156d-115">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2156d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2156d-116">Requirements</span></span>



| <span data-ttu-id="2156d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2156d-117">Requirement</span></span> | <span data-ttu-id="2156d-118">Value</span><span class="sxs-lookup"><span data-stu-id="2156d-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2156d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2156d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2156d-120">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2156d-120">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2156d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2156d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2156d-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2156d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2156d-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2156d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2156d-124"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2156d-124"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
