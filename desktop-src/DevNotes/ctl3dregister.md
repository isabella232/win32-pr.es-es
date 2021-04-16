---
description: Registra una aplicación como un cliente de CTL3D.
ms.assetid: 38a4a04a-6322-4eb8-b272-ae9b90f84e0f
title: Ctl3dRegister función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dRegister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 4b855c162d9d5f1c43a15d1ebd7219da6f847f37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650057"
---
# <a name="ctl3dregister-function"></a><span data-ttu-id="4369f-103">Ctl3dRegister función)</span><span class="sxs-lookup"><span data-stu-id="4369f-103">Ctl3dRegister function</span></span>

<span data-ttu-id="4369f-104">Registra una aplicación como un cliente de CTL3D.</span><span class="sxs-lookup"><span data-stu-id="4369f-104">Registers an application as a client of CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="4369f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4369f-105">Syntax</span></span>


```C++
BOOL Ctl3dRegister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a><span data-ttu-id="4369f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4369f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4369f-107">*hinstApp*</span><span class="sxs-lookup"><span data-stu-id="4369f-107">*hinstApp*</span></span> 
</dt> <dd>

<span data-ttu-id="4369f-108">Identificador de la aplicación que se va a registrar como cliente.</span><span class="sxs-lookup"><span data-stu-id="4369f-108">A handle to the application to be registered as a client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4369f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4369f-109">Return value</span></span>

<span data-ttu-id="4369f-110">Devuelve **true** si los efectos 3D están activos; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="4369f-110">Returns **TRUE** if 3D effects are active; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4369f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4369f-111">Remarks</span></span>

<span data-ttu-id="4369f-112">Una aplicación que usa CTL3D debe llamar a esta función en WinMain.</span><span class="sxs-lookup"><span data-stu-id="4369f-112">An application that uses CTL3D should call this function in WinMain.</span></span>

<span data-ttu-id="4369f-113">los efectos 3D no están disponibles en los sistemas que tienen una resolución inferior a VGA.</span><span class="sxs-lookup"><span data-stu-id="4369f-113">3D effects are not available on systems that have less than VGA resolution.</span></span>

<span data-ttu-id="4369f-114">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4369f-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4369f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4369f-115">Requirements</span></span>



| <span data-ttu-id="4369f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4369f-116">Requirement</span></span> | <span data-ttu-id="4369f-117">Value</span><span class="sxs-lookup"><span data-stu-id="4369f-117">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4369f-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4369f-118">DLL</span></span><br/> | <dl> <span data-ttu-id="4369f-119"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4369f-119"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
