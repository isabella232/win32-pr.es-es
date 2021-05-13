---
description: Se usa para determinar si se debe mostrar la opción Compartir esta carpeta en la vista web.
title: Función CanShareFolderW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CanShareFolderW
- CanShareFolderW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.assetid: 5fd28a14-53e7-4016-9c49-9bb14ce7808b
ms.openlocfilehash: 46df03208ecc468aac366fb0b4cfb33e1a68157e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841686"
---
# <a name="cansharefolderw-function"></a><span data-ttu-id="c0020-103">Función CanShareFolderW</span><span class="sxs-lookup"><span data-stu-id="c0020-103">CanShareFolderW function</span></span>

<span data-ttu-id="c0020-104">\[Esta función está disponible a través de Windows XP con Service Pack 2 (SP2) y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c0020-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="c0020-105">Podría modificarse o no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c0020-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="c0020-106">Se usa para determinar si se debe mostrar la **opción Compartir esta** carpeta en la vista web.</span><span class="sxs-lookup"><span data-stu-id="c0020-106">Used to determine whether to show the **Share this folder** option in web view.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0020-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0020-107">Syntax</span></span>


```C++
STDAPI CanShareFolderW(
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a><span data-ttu-id="c0020-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c0020-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0020-109">*pszPath* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c0020-109">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0020-110">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="c0020-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="c0020-111">Puntero a una cadena que especifica la ruta de acceso de la carpeta que se debe probar.</span><span class="sxs-lookup"><span data-stu-id="c0020-111">A pointer to a string that specifies the path of the folder to test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0020-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0020-112">Return value</span></span>

<span data-ttu-id="c0020-113">Tipo: **STDAPI**</span><span class="sxs-lookup"><span data-stu-id="c0020-113">Type: **STDAPI**</span></span>

<span data-ttu-id="c0020-114">Los valores devueltos incluyen lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="c0020-114">Return values include the following.</span></span>



| <span data-ttu-id="c0020-115">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0020-115">Return code/value</span></span>                                                                        | <span data-ttu-id="c0020-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0020-116">Description</span></span>                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c0020-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c0020-117"><dt>**S\_OK**</dt></span></span> </dl>     | <span data-ttu-id="c0020-118">La ruta de acceso a *la que apunta pszPath* especifica una carpeta que se puede compartir.</span><span class="sxs-lookup"><span data-stu-id="c0020-118">The path pointed to by *pszPath* specifies a folder that can be shared.</span></span><br/>    |
| <dl> <span data-ttu-id="c0020-119"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="c0020-119"><dt>**S\_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="c0020-120">La ruta de acceso a *la que apunta pszPath* especifica una carpeta que no se puede compartir.</span><span class="sxs-lookup"><span data-stu-id="c0020-120">The path pointed to by *pszPath* specifies a folder that cannot be shared.</span></span><br/> |
| <dl> <span data-ttu-id="c0020-121"><dt>Error HRESULT</dt></span><span class="sxs-lookup"><span data-stu-id="c0020-121"><dt>HRESULT error</dt></span></span> </dl> | <span data-ttu-id="c0020-122">Se ha producido un error.</span><span class="sxs-lookup"><span data-stu-id="c0020-122">An error has occurred.</span></span><br/>                                                     |



 

## <a name="remarks"></a><span data-ttu-id="c0020-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c0020-123">Remarks</span></span>

<span data-ttu-id="c0020-124">Esta función no tiene ningún archivo .lib asociado.</span><span class="sxs-lookup"><span data-stu-id="c0020-124">This function has no associated .lib file.</span></span> <span data-ttu-id="c0020-125">Debe usar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para usarlo.</span><span class="sxs-lookup"><span data-stu-id="c0020-125">You must use [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to use it.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0020-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0020-126">Requirements</span></span>



| <span data-ttu-id="c0020-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0020-127">Requirement</span></span> | <span data-ttu-id="c0020-128">Value</span><span class="sxs-lookup"><span data-stu-id="c0020-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0020-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0020-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c0020-130">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c0020-130">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c0020-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0020-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c0020-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c0020-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c0020-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c0020-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0020-134"><dt>Ntshrui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0020-134"><dt>Ntshrui.dll</dt></span></span> </dl> |
| <span data-ttu-id="c0020-135">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="c0020-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c0020-136">**CanShareFolderW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="c0020-136">**CanShareFolderW** (Unicode)</span></span><br/>                                               |



## <a name="see-also"></a><span data-ttu-id="c0020-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c0020-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0020-138">**ShowShareFolderUI**</span><span class="sxs-lookup"><span data-stu-id="c0020-138">**ShowShareFolderUI**</span></span>](./showsharefolderui.md)
</dt> </dl>

 

 
