---
description: Convierte una dirección URL de archivo en una ruta de acceso de Microsoft MS-DOS.
ms.assetid: c35988ad-6cf8-41ec-bee9-e3bb982310ee
title: MFCreatePathFromURL función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreatePathFromURL
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: c1838a3b09dc5375588d562aa503d555a186e394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715369"
---
# <a name="mfcreatepathfromurl-function"></a><span data-ttu-id="9830d-103">MFCreatePathFromURL función)</span><span class="sxs-lookup"><span data-stu-id="9830d-103">MFCreatePathFromURL function</span></span>

<span data-ttu-id="9830d-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="9830d-104">\[This API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="9830d-105">En su lugar, las aplicaciones deben llamar a [**PathCreateFromUrl**](/windows/win32/api/shlwapi/nf-shlwapi-pathcreatefromurla).\]</span><span class="sxs-lookup"><span data-stu-id="9830d-105">Instead, applications should call [**PathCreateFromUrl**](/windows/win32/api/shlwapi/nf-shlwapi-pathcreatefromurla).\]</span></span>

<span data-ttu-id="9830d-106">Convierte una dirección URL de archivo en una ruta de acceso de Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="9830d-106">Converts a file URL to a Microsoft MS-DOS path.</span></span>

## <a name="syntax"></a><span data-ttu-id="9830d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9830d-107">Syntax</span></span>


```C++
HRESULT MFCreatePathFromURL(
  _In_opt_ LPCWSTR pwszFileURL,
  _Out_    LPWSTR  *ppwszFilePath
);
```



## <a name="parameters"></a><span data-ttu-id="9830d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9830d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9830d-109">*pwszFileURL* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9830d-109">*pwszFileURL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9830d-110">Una cadena terminada en null que contiene la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="9830d-110">A null-terminated string that contains the URL.</span></span> <span data-ttu-id="9830d-111">La longitud máxima de la cadena es **longitud máxima de \_ \_ dirección URL \_ de Internet**.</span><span class="sxs-lookup"><span data-stu-id="9830d-111">The maximum length of the string is **INTERNET\_MAX\_URL\_LENGTH**.</span></span>

</dd> <dt>

<span data-ttu-id="9830d-112">*ppwszFilePath* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9830d-112">*ppwszFilePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9830d-113">Recibe una cadena terminada en null que contiene la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="9830d-113">Receives a null-terminated string that contains the URL.</span></span> <span data-ttu-id="9830d-114">El autor de la llamada debe liberar la cadena mediante una llamada a [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="9830d-114">The caller must free the string by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9830d-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9830d-115">Return value</span></span>

<span data-ttu-id="9830d-116">La función devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9830d-116">The function returns an **HRESULT**.</span></span> <span data-ttu-id="9830d-117">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="9830d-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9830d-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9830d-118">Return code</span></span>                                                                                  | <span data-ttu-id="9830d-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="9830d-119">Description</span></span>                                                                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9830d-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9830d-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="9830d-121">La función se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9830d-121">The function succeeded.</span></span> <br/>                                                                         |
| <dl> <span data-ttu-id="9830d-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9830d-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="9830d-123">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="9830d-123">Invalid argument.</span></span> <span data-ttu-id="9830d-124">La cadena especificada en el parámetro *pwszFileURL* no se puede convertir en una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="9830d-124">The string given in the *pwszFileURL* parameter cannot be converted to a path.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9830d-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9830d-125">Remarks</span></span>

<span data-ttu-id="9830d-126">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="9830d-126">This function has no associated import library.</span></span> <span data-ttu-id="9830d-127">Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mfplat.dll.</span><span class="sxs-lookup"><span data-stu-id="9830d-127">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mfplat.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="9830d-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9830d-128">Requirements</span></span>



| <span data-ttu-id="9830d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9830d-129">Requirement</span></span> | <span data-ttu-id="9830d-130">Value</span><span class="sxs-lookup"><span data-stu-id="9830d-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9830d-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9830d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9830d-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9830d-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9830d-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9830d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9830d-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9830d-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9830d-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9830d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9830d-136"><dt>Mfplat.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9830d-136"><dt>Mfplat.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9830d-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="9830d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9830d-138">Funciones de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9830d-138">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> </dl>

 

 
