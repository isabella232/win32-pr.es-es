---
description: Muestra el cuadro de diálogo Administrador de claves en la interfaz de usuario.
ms.assetid: 65c2763f-42d5-4534-94f7-e753f6486014
title: KRShowKeyMgr función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KRShowKeyMgr
api_type:
- DllExport
api_location:
- Keymgr.dll
ms.openlocfilehash: 59b6b38cf7e78755c7d5c481a22a0a8b3854c8a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670419"
---
# <a name="krshowkeymgr-function"></a><span data-ttu-id="ef171-103">KRShowKeyMgr función)</span><span class="sxs-lookup"><span data-stu-id="ef171-103">KRShowKeyMgr function</span></span>

<span data-ttu-id="ef171-104">\[Esta función solo se incluye en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ef171-104">\[This function is included only in Windows XP.</span></span> <span data-ttu-id="ef171-105">No se incluye actualmente en ninguna otra versión de Windows ni se espera que se incluya en las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ef171-105">It is not currently included in any other version of Windows, nor is it expected to be included in any future versions of Windows.\]</span></span>

<span data-ttu-id="ef171-106">Muestra el cuadro de diálogo Administrador de claves en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ef171-106">Brings up the key manager dialog into the user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef171-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef171-107">Syntax</span></span>


```C++
void KRShowKeyMgr(
   HWND      hwParent,
   HINSTANCE hInstance,
   LPWSTR    pszCmdLine,
   int       CmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="ef171-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef171-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef171-109">*hwParent*</span><span class="sxs-lookup"><span data-stu-id="ef171-109">*hwParent*</span></span> 
</dt> <dd>

<span data-ttu-id="ef171-110">Identificador de la ventana primaria del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ef171-110">A handle to the parent window of the dialog.</span></span> <span data-ttu-id="ef171-111">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ef171-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ef171-112">*hInstance*</span><span class="sxs-lookup"><span data-stu-id="ef171-112">*hInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="ef171-113">Este parámetro no se utiliza y debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="ef171-113">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ef171-114">*pszCmdLine*</span><span class="sxs-lookup"><span data-stu-id="ef171-114">*pszCmdLine*</span></span> 
</dt> <dd>

<span data-ttu-id="ef171-115">Este parámetro no se utiliza y debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="ef171-115">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ef171-116">*CmdShow*</span><span class="sxs-lookup"><span data-stu-id="ef171-116">*CmdShow*</span></span> 
</dt> <dd>

<span data-ttu-id="ef171-117">Este parámetro no se utiliza y debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="ef171-117">This parameter is not used and should be set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef171-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef171-118">Return value</span></span>

<span data-ttu-id="ef171-119">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ef171-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef171-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef171-120">Remarks</span></span>

<span data-ttu-id="ef171-121">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="ef171-121">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef171-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef171-122">Requirements</span></span>



| <span data-ttu-id="ef171-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef171-123">Requirement</span></span> | <span data-ttu-id="ef171-124">Value</span><span class="sxs-lookup"><span data-stu-id="ef171-124">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef171-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ef171-125">DLL</span></span><br/> | <dl> <span data-ttu-id="ef171-126"><dt>Keymgr.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef171-126"><dt>Keymgr.dll</dt></span></span> </dl> |



 

 
