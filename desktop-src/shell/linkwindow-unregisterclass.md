---
description: Anula el registro de una clase de ventana registrada por LinkWindow \_ RegisterClass.
ms.assetid: 9e5c4326-efd1-43ca-a087-a436fe3f9bbd
title: LinkWindow_UnregisterClass función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_UnregisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 604cea299156444a1fedf34a46c50b5b397a65da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985670"
---
# <a name="linkwindow_unregisterclass-function"></a><span data-ttu-id="0822a-103">LinkWindow \_ UnregisterClass función)</span><span class="sxs-lookup"><span data-stu-id="0822a-103">LinkWindow\_UnregisterClass function</span></span>

<span data-ttu-id="0822a-104">\[Esta función está disponible a través de Windows XP con Service Pack 2 (SP2) y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0822a-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="0822a-105">Podría modificarse o no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0822a-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="0822a-106">Anula el registro de una clase de ventana registrada por [**LinkWindow \_ RegisterClass**](linkwindow-registerclass.md).</span><span class="sxs-lookup"><span data-stu-id="0822a-106">Unregisters a window class registered by [**LinkWindow\_RegisterClass**](linkwindow-registerclass.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0822a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0822a-107">Syntax</span></span>


```C++
BOOL LinkWindow_UnregisterClass(void);
```



## <a name="parameters"></a><span data-ttu-id="0822a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0822a-108">Parameters</span></span>

<span data-ttu-id="0822a-109">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0822a-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0822a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0822a-110">Return value</span></span>

<span data-ttu-id="0822a-111">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="0822a-111">Type: **BOOL**</span></span>

<span data-ttu-id="0822a-112">Devuelve **true** si la operación se realizó correctamente; De lo contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="0822a-112">Returns **TRUE** if the operation was successful; **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0822a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0822a-113">Remarks</span></span>

<span data-ttu-id="0822a-114">Esta función no tiene un archivo de encabezado o biblioteca asociado, por lo que debe llamarse por valor ordinal.</span><span class="sxs-lookup"><span data-stu-id="0822a-114">This function does not have an associated header or library file so it must be called by ordinal value.</span></span> <span data-ttu-id="0822a-115">Llame a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre de dll Shell32.dll para obtener un identificador de módulo.</span><span class="sxs-lookup"><span data-stu-id="0822a-115">Call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name Shell32.dll to obtain a module handle.</span></span> <span data-ttu-id="0822a-116">A continuación, llame a [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con ese identificador de módulo y el número ordinal 259 para usar esta función.</span><span class="sxs-lookup"><span data-stu-id="0822a-116">Then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the ordinal number 259 to use this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0822a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0822a-117">Requirements</span></span>



| <span data-ttu-id="0822a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0822a-118">Requirement</span></span> | <span data-ttu-id="0822a-119">Value</span><span class="sxs-lookup"><span data-stu-id="0822a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0822a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0822a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0822a-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0822a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0822a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0822a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0822a-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0822a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0822a-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0822a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0822a-125"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="0822a-125"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0822a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="0822a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0822a-127">Información general sobre los controles SysLink</span><span class="sxs-lookup"><span data-stu-id="0822a-127">Overview of SysLink Controls</span></span>](../controls/syslink-overview.md)
</dt> </dl>

 

 
