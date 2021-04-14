---
title: TF_InvalidAssemblyListCacheIfExist función)
description: La \_ función TF InvalidAssemblyListCacheIfExist invalida la caché de Descripción del procesador de entrada de texto.
ms.assetid: a0f61b25-598c-417c-8679-7523c041f9ef
keywords:
- TF_InvalidAssemblyListCacheIfExist Framework de servicios de texto de función
topic_type:
- apiref
api_name:
- TF_InvalidAssemblyListCacheIfExist
api_location:
- msctf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8dd28ab2247fae28af1c5f322832aebe071fab4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533957"
---
# <a name="tf_invalidassemblylistcacheifexist-function"></a><span data-ttu-id="ab1db-104">TF \_ InvalidAssemblyListCacheIfExist función)</span><span class="sxs-lookup"><span data-stu-id="ab1db-104">TF\_InvalidAssemblyListCacheIfExist function</span></span>

<span data-ttu-id="ab1db-105">La función **TF \_ InvalidAssemblyListCacheIfExist** invalida la caché de Descripción del procesador de entrada de texto.</span><span class="sxs-lookup"><span data-stu-id="ab1db-105">The **TF\_InvalidAssemblyListCacheIfExist** function invalidates the text input processor's description cache.</span></span> <span data-ttu-id="ab1db-106">No es necesario llamar a esta función si el programa de instalación del procesador de entrada requiere que se reinicie o se inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="ab1db-106">It is not necessary to call this function if the input processor setup program requires you to restart or log on.</span></span> <span data-ttu-id="ab1db-107">La memoria caché es válida hasta que el usuario cierra la sesión.</span><span class="sxs-lookup"><span data-stu-id="ab1db-107">The cache is valid until the user logs off.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab1db-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab1db-108">Syntax</span></span>


```C++
HRESULT TF_InvalidAssemblyListCacheIfExist(void);
```



## <a name="parameters"></a><span data-ttu-id="ab1db-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab1db-109">Parameters</span></span>

<span data-ttu-id="ab1db-110">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ab1db-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ab1db-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab1db-111">Return value</span></span>

<span data-ttu-id="ab1db-112">Esta función puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="ab1db-112">This function can return one of these values.</span></span>



| <span data-ttu-id="ab1db-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ab1db-113">Return code</span></span>                                                                            | <span data-ttu-id="ab1db-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab1db-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="ab1db-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ab1db-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="ab1db-116">La función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ab1db-116">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="ab1db-117"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="ab1db-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="ab1db-118">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="ab1db-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="ab1db-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ab1db-119">Examples</span></span>

<span data-ttu-id="ab1db-120">No hay ninguna biblioteca de importación disponible que defina esta función, por lo que es necesario obtener un puntero a esta función mediante [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="ab1db-120">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="ab1db-121">En el ejemplo siguiente se muestra cómo obtener un puntero a esta función.</span><span class="sxs-lookup"><span data-stu-id="ab1db-121">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="ab1db-122">El uso incorrecto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede poner en peligro la seguridad de la aplicación mediante la carga de una DLL incorrecta.</span><span class="sxs-lookup"><span data-stu-id="ab1db-122">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="ab1db-123">Consulte el [orden de búsqueda de la biblioteca de vínculos dinámicos](/windows/desktop/Dlls/dynamic-link-library-search-order) para obtener información sobre cómo cargar correctamente los archivos DLL con diferentes versiones de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ab1db-123">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *pTF_InvalidAssemblyListCacheIfExist )(void);

HMODULE hMSCTF = LoadLibrary(TEXT("msctf.dll"));

if(hMSCTF == NULL)
{
    //Error loading module -- fail as securely as possible 
}

else
{
    pTF_InvalidAssemblyListCacheIfExist pfnInvalidAssemblyListCacheIfExist;
    
    pfnInvalidAssemblyListCacheIfExist = (pTF_InvalidAssemblyListCacheIfExist )GetProcAddress(hMSCTF, "TF_InvalidAssemblyListCacheIfExist");

    if(pfnInvalidAssemblyListCacheIfExist)
    {
        (*pfnInvalidAssemblyListCacheIfExist)();
       
    }

    FreeLibrary(hMSCTF);
}
```



## <a name="requirements"></a><span data-ttu-id="ab1db-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab1db-124">Requirements</span></span>



| <span data-ttu-id="ab1db-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab1db-125">Requirement</span></span> | <span data-ttu-id="ab1db-126">Value</span><span class="sxs-lookup"><span data-stu-id="ab1db-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ab1db-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab1db-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ab1db-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ab1db-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ab1db-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab1db-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ab1db-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ab1db-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ab1db-131">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="ab1db-131">Redistributable</span></span><br/>          | <span data-ttu-id="ab1db-132">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ab1db-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="ab1db-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ab1db-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab1db-134"><dt>Msctf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab1db-134"><dt>Msctf.dll</dt></span></span> </dl> |



 

