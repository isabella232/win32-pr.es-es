---
description: Se usa para determinar si se debe mostrar la opción compartir esta carpeta en la vista Web.
title: CanShareFolderW función)
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
ms.openlocfilehash: cf7d0feb31666f3a918c0307a0b0983bff246fea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540563"
---
# <a name="cansharefolderw-function"></a><span data-ttu-id="8ac87-103">CanShareFolderW función)</span><span class="sxs-lookup"><span data-stu-id="8ac87-103">CanShareFolderW function</span></span>

<span data-ttu-id="8ac87-104">\[Esta función está disponible a través de Windows XP con Service Pack 2 (SP2) y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8ac87-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="8ac87-105">Podría modificarse o no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8ac87-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="8ac87-106">Se usa para determinar si se debe mostrar la opción **compartir esta carpeta en la** vista Web.</span><span class="sxs-lookup"><span data-stu-id="8ac87-106">Used to determine whether to show the **Share this folder** option in web view.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ac87-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ac87-107">Syntax</span></span>


```C++
STDAPI CanShareFolderW(
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a><span data-ttu-id="8ac87-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ac87-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ac87-109">*pszPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ac87-109">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ac87-110">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="8ac87-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="8ac87-111">Puntero a una cadena que especifica la ruta de acceso de la carpeta que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="8ac87-111">A pointer to a string that specifies the path of the folder to test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ac87-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ac87-112">Return value</span></span>

<span data-ttu-id="8ac87-113">Tipo: **STDAPI**</span><span class="sxs-lookup"><span data-stu-id="8ac87-113">Type: **STDAPI**</span></span>

<span data-ttu-id="8ac87-114">Los valores devueltos son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="8ac87-114">Return values include the following.</span></span>



| <span data-ttu-id="8ac87-115">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ac87-115">Return code/value</span></span>                                                                        | <span data-ttu-id="8ac87-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ac87-116">Description</span></span>                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8ac87-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8ac87-117"><dt>**S\_OK**</dt></span></span> </dl>     | <span data-ttu-id="8ac87-118">La ruta de acceso a la que apunta *pszPath* especifica una carpeta que se puede compartir.</span><span class="sxs-lookup"><span data-stu-id="8ac87-118">The path pointed to by *pszPath* specifies a folder that can be shared.</span></span><br/>    |
| <dl> <span data-ttu-id="8ac87-119"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="8ac87-119"><dt>**S\_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="8ac87-120">La ruta de acceso a la que apunta *pszPath* especifica una carpeta que no se puede compartir.</span><span class="sxs-lookup"><span data-stu-id="8ac87-120">The path pointed to by *pszPath* specifies a folder that cannot be shared.</span></span><br/> |
| <dl> <span data-ttu-id="8ac87-121"><dt>Error HRESULT</dt></span><span class="sxs-lookup"><span data-stu-id="8ac87-121"><dt>HRESULT error</dt></span></span> </dl> | <span data-ttu-id="8ac87-122">Se ha producido un error.</span><span class="sxs-lookup"><span data-stu-id="8ac87-122">An error has occurred.</span></span><br/>                                                     |



 

## <a name="remarks"></a><span data-ttu-id="8ac87-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ac87-123">Remarks</span></span>

<span data-ttu-id="8ac87-124">Esta función no tiene ningún archivo. lib asociado.</span><span class="sxs-lookup"><span data-stu-id="8ac87-124">This function has no associated .lib file.</span></span> <span data-ttu-id="8ac87-125">Debe utilizar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para usarlo.</span><span class="sxs-lookup"><span data-stu-id="8ac87-125">You must use [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to use it.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ac87-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ac87-126">Requirements</span></span>



| <span data-ttu-id="8ac87-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ac87-127">Requirement</span></span> | <span data-ttu-id="8ac87-128">Value</span><span class="sxs-lookup"><span data-stu-id="8ac87-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ac87-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ac87-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8ac87-130">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="8ac87-130">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8ac87-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ac87-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8ac87-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8ac87-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8ac87-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8ac87-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ac87-134"><dt>Ntshrui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ac87-134"><dt>Ntshrui.dll</dt></span></span> </dl> |
| <span data-ttu-id="8ac87-135">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="8ac87-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8ac87-136">**CanShareFolderW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="8ac87-136">**CanShareFolderW** (Unicode)</span></span><br/>                                               |



## <a name="see-also"></a><span data-ttu-id="8ac87-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ac87-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ac87-138">**ShowShareFolderUI**</span><span class="sxs-lookup"><span data-stu-id="8ac87-138">**ShowShareFolderUI**</span></span>](./showsharefolderui.md)
</dt> </dl>

 

 
