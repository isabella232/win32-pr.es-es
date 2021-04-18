---
description: Convierte una ruta de acceso de Microsoft MS-DOS en una dirección URL con formato canónico.
ms.assetid: 1186b970-9ae1-4020-b999-55157cff1741
title: MFCreateURLFromPath función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateURLFromPath
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: e43c2d7df299792d8b5be99226e9cfdbd11976a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715370"
---
# <a name="mfcreateurlfrompath-function"></a><span data-ttu-id="b0d17-103">MFCreateURLFromPath función)</span><span class="sxs-lookup"><span data-stu-id="b0d17-103">MFCreateURLFromPath function</span></span>

<span data-ttu-id="b0d17-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b0d17-104">\[This API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="b0d17-105">En su lugar, las aplicaciones deben llamar a [UrlCreateFromPath](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha).\]</span><span class="sxs-lookup"><span data-stu-id="b0d17-105">Instead, Applications should call [UrlCreateFromPath](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha).\]</span></span>

<span data-ttu-id="b0d17-106">Convierte una ruta de acceso de Microsoft MS-DOS en una dirección URL con formato canónico.</span><span class="sxs-lookup"><span data-stu-id="b0d17-106">Converts a Microsoft MS-DOS path to a canonicalized URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0d17-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0d17-107">Syntax</span></span>


```C++
HRESULT MFCreateURLFromPath(
  _In_opt_ LPCWSTR pwszFilePath,
  _Out_    LPWSTR  *ppwszFileURL
);
```



## <a name="parameters"></a><span data-ttu-id="b0d17-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0d17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0d17-109">*pwszFilePath* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b0d17-109">*pwszFilePath* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0d17-110">Una cadena terminada en null que contiene la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="b0d17-110">A null-terminated string that contains the path.</span></span> <span data-ttu-id="b0d17-111">La longitud máxima de la cadena es **longitud máxima de \_ \_ dirección URL \_ de Internet**.</span><span class="sxs-lookup"><span data-stu-id="b0d17-111">The maximum length of the string is **INTERNET\_MAX\_URL\_LENGTH**.</span></span>

</dd> <dt>

<span data-ttu-id="b0d17-112">*ppwszFileURL* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b0d17-112">*ppwszFileURL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0d17-113">Recibe una cadena terminada en null que contiene la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="b0d17-113">Receives a null-terminated string that contains the URL.</span></span> <span data-ttu-id="b0d17-114">El autor de la llamada debe liberar la cadena mediante una llamada a [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="b0d17-114">The caller must free the string by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0d17-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0d17-115">Return value</span></span>

<span data-ttu-id="b0d17-116">La función devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b0d17-116">The function returns an **HRESULT**.</span></span> <span data-ttu-id="b0d17-117">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="b0d17-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b0d17-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b0d17-118">Return code</span></span>                                                                             | <span data-ttu-id="b0d17-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0d17-119">Description</span></span>                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b0d17-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="b0d17-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="b0d17-121">La cadena especificada en el parámetro *pwszFilePath* ya está en formato de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="b0d17-121">The string given in the *pwszFilePath* parameter is already in URL format.</span></span> <span data-ttu-id="b0d17-122">En este caso, *pszFilePath* simplemente se copia en *ppszFileURL* sin modificarlo.</span><span class="sxs-lookup"><span data-stu-id="b0d17-122">In this case, *pszFilePath* is simply copied to *ppszFileURL* without modification.</span></span><br/> |
| <dl> <span data-ttu-id="b0d17-123"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b0d17-123"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="b0d17-124">La función se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b0d17-124">The function succeeded.</span></span> <br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="b0d17-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0d17-125">Remarks</span></span>

<span data-ttu-id="b0d17-126">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="b0d17-126">This function has no associated import library.</span></span> <span data-ttu-id="b0d17-127">Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mfplat.dll.</span><span class="sxs-lookup"><span data-stu-id="b0d17-127">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mfplat.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0d17-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0d17-128">Requirements</span></span>



| <span data-ttu-id="b0d17-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0d17-129">Requirement</span></span> | <span data-ttu-id="b0d17-130">Value</span><span class="sxs-lookup"><span data-stu-id="b0d17-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0d17-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0d17-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b0d17-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b0d17-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b0d17-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0d17-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b0d17-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b0d17-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0d17-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b0d17-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0d17-136"><dt>Mfplat.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0d17-136"><dt>Mfplat.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0d17-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0d17-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0d17-138">Funciones de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b0d17-138">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> </dl>

 

 
