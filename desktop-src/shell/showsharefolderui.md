---
description: Muestra la ficha compartir carpetas de la hoja de propiedades de la carpeta especificada.
ms.assetid: e622e4bb-eaf7-494f-b2a2-78ba1311a496
title: ShowShareFolderUI función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShowShareFolderUI
- ShowShareFolderUIW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.openlocfilehash: e6270f72d1574a21b98ac9ee3151af1f34f08a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360884"
---
# <a name="showsharefolderui-function"></a><span data-ttu-id="386b7-103">ShowShareFolderUI función)</span><span class="sxs-lookup"><span data-stu-id="386b7-103">ShowShareFolderUI function</span></span>

<span data-ttu-id="386b7-104">Muestra la ficha **compartir carpetas** de la hoja de propiedades de la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="386b7-104">Displays the **Folder Sharing** tab on the properties sheet for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="386b7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="386b7-105">Syntax</span></span>


```C++
HRESULT ShowShareFolderUI(
  _In_ HWND    hwndParent,
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a><span data-ttu-id="386b7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="386b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="386b7-107">*hwndParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="386b7-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="386b7-108">Tipo: **hWnd**</span><span class="sxs-lookup"><span data-stu-id="386b7-108">Type: **HWND**</span></span>

<span data-ttu-id="386b7-109">Identificador de la ventana primaria de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="386b7-109">A handle to the parent window for the property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="386b7-110">*pszPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="386b7-110">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="386b7-111">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="386b7-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="386b7-112">Un puntero a una cadena que especifica la ruta de acceso a la carpeta que muestra su ficha de **uso compartido de carpetas** .</span><span class="sxs-lookup"><span data-stu-id="386b7-112">A pointer to a string that specifies the path to the folder that displays its **Folder Sharing** tab.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="386b7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="386b7-113">Return value</span></span>

<span data-ttu-id="386b7-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="386b7-114">Type: **HRESULT**</span></span>

<span data-ttu-id="386b7-115">Esta función siempre devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="386b7-115">This function always returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="386b7-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="386b7-116">Remarks</span></span>

<span data-ttu-id="386b7-117">Esta función no tiene ningún archivo. lib asociado.</span><span class="sxs-lookup"><span data-stu-id="386b7-117">This function has no associated .lib file.</span></span> <span data-ttu-id="386b7-118">Debe utilizar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para usarlo.</span><span class="sxs-lookup"><span data-stu-id="386b7-118">You must use [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to use it.</span></span>

## <a name="requirements"></a><span data-ttu-id="386b7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="386b7-119">Requirements</span></span>



| <span data-ttu-id="386b7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="386b7-120">Requirement</span></span> | <span data-ttu-id="386b7-121">Value</span><span class="sxs-lookup"><span data-stu-id="386b7-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="386b7-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="386b7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="386b7-123">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="386b7-123">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="386b7-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="386b7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="386b7-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="386b7-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="386b7-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="386b7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="386b7-127"><dt>Ntshrui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="386b7-127"><dt>Ntshrui.dll</dt></span></span> </dl> |
| <span data-ttu-id="386b7-128">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="386b7-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="386b7-129">**ShowShareFolderUIW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="386b7-129">**ShowShareFolderUIW** (Unicode)</span></span><br/>                                            |



## <a name="see-also"></a><span data-ttu-id="386b7-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="386b7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="386b7-131">**CanShareFolderW**</span><span class="sxs-lookup"><span data-stu-id="386b7-131">**CanShareFolderW**</span></span>](cansharefolderw.md)
</dt> </dl>

 

 
