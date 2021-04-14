---
description: Registra una clase de ventana que permite usar el control común SysLink en una ventana.
ms.assetid: 1e6dd741-81be-40bb-a8b5-d565f593c4e9
title: LinkWindow_RegisterClass función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_RegisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 7b5bfd2e1a45ff3f65df7cf3d3cae41bf4926aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985671"
---
# <a name="linkwindow_registerclass-function"></a><span data-ttu-id="884de-103">LinkWindow \_ RegisterClass (función)</span><span class="sxs-lookup"><span data-stu-id="884de-103">LinkWindow\_RegisterClass function</span></span>

<span data-ttu-id="884de-104">\[Esta función está disponible a través de Windows XP con Service Pack 2 (SP2) y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="884de-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="884de-105">Podría modificarse o no estar disponible en versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="884de-105">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="884de-106">Use [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="884de-106">Use [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) instead.\]</span></span>

<span data-ttu-id="884de-107">Registra una clase de ventana que permite usar el control común [SysLink](../controls/syslink-overview.md) en una ventana.</span><span class="sxs-lookup"><span data-stu-id="884de-107">Registers a window class that allows for the [SysLink](../controls/syslink-overview.md) common control to be used in a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="884de-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="884de-108">Syntax</span></span>


```C++
BOOL LinkWindow_RegisterClass(void);
```



## <a name="parameters"></a><span data-ttu-id="884de-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="884de-109">Parameters</span></span>

<span data-ttu-id="884de-110">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="884de-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="884de-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="884de-111">Return value</span></span>

<span data-ttu-id="884de-112">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="884de-112">Type: **BOOL**</span></span>

<span data-ttu-id="884de-113">Devuelve **true** si el registro se realizó correctamente; De lo contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="884de-113">Returns **TRUE** if registration was successful; **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="884de-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="884de-114">Remarks</span></span>

<span data-ttu-id="884de-115">Esta función no tiene un archivo de encabezado o biblioteca asociado, por lo que debe llamarse por valor ordinal.</span><span class="sxs-lookup"><span data-stu-id="884de-115">This function does not have an associated header or library file so it must be called by ordinal value.</span></span> <span data-ttu-id="884de-116">Llame a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre de dll Shell32.dll para obtener un identificador de módulo.</span><span class="sxs-lookup"><span data-stu-id="884de-116">Call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name Shell32.dll to obtain a module handle.</span></span> <span data-ttu-id="884de-117">A continuación, llame a [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con ese identificador de módulo y el número ordinal 258 para usar esta función.</span><span class="sxs-lookup"><span data-stu-id="884de-117">Then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the ordinal number 258 to use this function.</span></span>

<span data-ttu-id="884de-118">Use [**LinkWindow \_ UnregisterClass**](linkwindow-unregisterclass.md) para anular el registro de la clase después del uso.</span><span class="sxs-lookup"><span data-stu-id="884de-118">Use [**LinkWindow\_UnregisterClass**](linkwindow-unregisterclass.md) to unregister the class after use.</span></span>

## <a name="requirements"></a><span data-ttu-id="884de-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="884de-119">Requirements</span></span>



| <span data-ttu-id="884de-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="884de-120">Requirement</span></span> | <span data-ttu-id="884de-121">Value</span><span class="sxs-lookup"><span data-stu-id="884de-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="884de-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="884de-122">Minimum supported client</span></span><br/> | <span data-ttu-id="884de-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="884de-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="884de-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="884de-124">Minimum supported server</span></span><br/> | <span data-ttu-id="884de-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="884de-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="884de-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="884de-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="884de-127"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="884de-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="884de-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="884de-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="884de-129">Información general sobre los controles SysLink</span><span class="sxs-lookup"><span data-stu-id="884de-129">Overview of SysLink Controls</span></span>](../controls/syslink-overview.md)
</dt> </dl>

 

 
