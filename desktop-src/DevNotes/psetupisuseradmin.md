---
description: Indica si el usuario actual es un administrador.
ms.assetid: e759a6b9-19c3-4a2e-b8cf-1398037f88ee
title: pSetupIsUserAdmin función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupIsUserAdmin
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1c40a69fd682c22e2625a3ba362d11d719cf9cce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671345"
---
# <a name="psetupisuseradmin-function"></a><span data-ttu-id="9856c-103">pSetupIsUserAdmin función)</span><span class="sxs-lookup"><span data-stu-id="9856c-103">pSetupIsUserAdmin function</span></span>

<span data-ttu-id="9856c-104">\[Esta función no está disponible en Windows Vista ni Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="9856c-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="9856c-105">Indica si el usuario actual es un administrador.</span><span class="sxs-lookup"><span data-stu-id="9856c-105">Indicates whether the current user is an administrator.</span></span>

## <a name="syntax"></a><span data-ttu-id="9856c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9856c-106">Syntax</span></span>


```C++
BOOL pSetupIsUserAdmin(void);
```



## <a name="parameters"></a><span data-ttu-id="9856c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9856c-107">Parameters</span></span>

<span data-ttu-id="9856c-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9856c-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9856c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9856c-109">Return value</span></span>

<span data-ttu-id="9856c-110">**True** si el usuario actual es un administrador; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="9856c-110">**TRUE** if the current user is an administrator, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9856c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9856c-111">Remarks</span></span>

<span data-ttu-id="9856c-112">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="9856c-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9856c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9856c-113">Requirements</span></span>



| <span data-ttu-id="9856c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9856c-114">Requirement</span></span> | <span data-ttu-id="9856c-115">Value</span><span class="sxs-lookup"><span data-stu-id="9856c-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9856c-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9856c-116">DLL</span></span><br/> | <dl> <span data-ttu-id="9856c-117"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9856c-117"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
