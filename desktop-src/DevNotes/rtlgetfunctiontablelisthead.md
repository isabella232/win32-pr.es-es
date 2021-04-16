---
description: Permite que un depurador examine la información de la tabla de funciones dinámicas.
ms.assetid: 32fd0dfd-ca7c-45e4-9d59-2b3318d7e13d
title: RtlGetFunctionTableListHead función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetFunctionTableListHead
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3dde476ee9958952d85c66816a113b92529aa13e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671362"
---
# <a name="rtlgetfunctiontablelisthead-function"></a><span data-ttu-id="12fcf-103">RtlGetFunctionTableListHead función)</span><span class="sxs-lookup"><span data-stu-id="12fcf-103">RtlGetFunctionTableListHead function</span></span>

<span data-ttu-id="12fcf-104">\[Esta función se puede cambiar o quitar de Windows sin previo aviso.\]</span><span class="sxs-lookup"><span data-stu-id="12fcf-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="12fcf-105">Permite que un depurador examine la información de la tabla de funciones dinámicas.</span><span class="sxs-lookup"><span data-stu-id="12fcf-105">Enables a debugger to examine dynamic function table information.</span></span>

## <a name="syntax"></a><span data-ttu-id="12fcf-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12fcf-106">Syntax</span></span>


```C++
PLIST_ENTRY RtlGetFunctionTableListHead(void);
```



## <a name="parameters"></a><span data-ttu-id="12fcf-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="12fcf-107">Parameters</span></span>

<span data-ttu-id="12fcf-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="12fcf-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="12fcf-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="12fcf-109">Return value</span></span>

<span data-ttu-id="12fcf-110">Devuelve un puntero al encabezado de la lista de la tabla de funciones.</span><span class="sxs-lookup"><span data-stu-id="12fcf-110">Returns a pointer to the head of the function table list.</span></span>

## <a name="remarks"></a><span data-ttu-id="12fcf-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12fcf-111">Remarks</span></span>

<span data-ttu-id="12fcf-112">Tenga en cuenta que el archivo de encabezado de Windows Driver Kit (WDK) Ntdef. h es necesario para algunas definiciones.</span><span class="sxs-lookup"><span data-stu-id="12fcf-112">Note that the Windows Driver Kit (WDK) header file Ntdef.h is required for some definitions.</span></span> <span data-ttu-id="12fcf-113">La biblioteca de importación asociada, ntdll. lib, está disponible en el WDK.</span><span class="sxs-lookup"><span data-stu-id="12fcf-113">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="12fcf-114">También puede utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="12fcf-114">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="12fcf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12fcf-115">Requirements</span></span>



| <span data-ttu-id="12fcf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="12fcf-116">Requirement</span></span> | <span data-ttu-id="12fcf-117">Value</span><span class="sxs-lookup"><span data-stu-id="12fcf-117">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="12fcf-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="12fcf-118">DLL</span></span><br/> | <dl> <span data-ttu-id="12fcf-119"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12fcf-119"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
