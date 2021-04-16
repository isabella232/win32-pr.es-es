---
description: Anula el registro de una aplicación como cliente de CTL3D.
ms.assetid: 21990A79-F90D-4AE1-AB02-2B33583B47F5
title: Ctl3dUnregister función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnregister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 85cd45062da9c01ef8af5a312a855bfaab6a6bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650080"
---
# <a name="ctl3dunregister-function"></a><span data-ttu-id="2f94f-103">Ctl3dUnregister función)</span><span class="sxs-lookup"><span data-stu-id="2f94f-103">Ctl3dUnregister function</span></span>

<span data-ttu-id="2f94f-104">Anula el registro de una aplicación como cliente de CTL3D.</span><span class="sxs-lookup"><span data-stu-id="2f94f-104">Unregisters an application as a client of CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f94f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f94f-105">Syntax</span></span>


```C++
BOOL Ctl3dUnregister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a><span data-ttu-id="2f94f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f94f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f94f-107">*hinstApp*</span><span class="sxs-lookup"><span data-stu-id="2f94f-107">*hinstApp*</span></span> 
</dt> <dd>

<span data-ttu-id="2f94f-108">Identificador de la aplicación cuya registro se va a anular como cliente.</span><span class="sxs-lookup"><span data-stu-id="2f94f-108">A handle to the application to be unregistered as a client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f94f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f94f-109">Return value</span></span>

<span data-ttu-id="2f94f-110">Devuelve **true** si se anula el registro de la aplicación como cliente de CTL3D; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="2f94f-110">Returns **TRUE** if the application is unregistered as a client of CTL3D; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f94f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f94f-111">Remarks</span></span>

<span data-ttu-id="2f94f-112">Una aplicación que usa CTL3D debe llamar a esta función en WinMain.</span><span class="sxs-lookup"><span data-stu-id="2f94f-112">An application that uses CTL3D should call this function in WinMain.</span></span>

<span data-ttu-id="2f94f-113">los efectos 3D no están disponibles en los sistemas que tienen una resolución inferior a VGA.</span><span class="sxs-lookup"><span data-stu-id="2f94f-113">3D effects are not available on systems that have less than VGA resolution.</span></span>

<span data-ttu-id="2f94f-114">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="2f94f-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f94f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f94f-115">Requirements</span></span>



| <span data-ttu-id="2f94f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f94f-116">Requirement</span></span> | <span data-ttu-id="2f94f-117">Value</span><span class="sxs-lookup"><span data-stu-id="2f94f-117">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f94f-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2f94f-118">DLL</span></span><br/> | <dl> <span data-ttu-id="2f94f-119"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f94f-119"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
