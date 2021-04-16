---
description: Desactiva la subclase automática.
ms.assetid: 85e5689f-6805-4aad-b97c-aa496e315900
title: Ctl3dUnAutoSubclass función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 1250deb16307400898c92d36b9dda214115ec01d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650118"
---
# <a name="ctl3dunautosubclass-function"></a><span data-ttu-id="af7c0-103">Ctl3dUnAutoSubclass función)</span><span class="sxs-lookup"><span data-stu-id="af7c0-103">Ctl3dUnAutoSubclass function</span></span>

<span data-ttu-id="af7c0-104">Desactiva la subclase automática.</span><span class="sxs-lookup"><span data-stu-id="af7c0-104">Turns off automatic subclassing.</span></span>

## <a name="syntax"></a><span data-ttu-id="af7c0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af7c0-105">Syntax</span></span>


```C++
BOOL Ctl3dUnAutoSubclass(void);
```



## <a name="parameters"></a><span data-ttu-id="af7c0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af7c0-106">Parameters</span></span>

<span data-ttu-id="af7c0-107">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="af7c0-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="af7c0-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af7c0-108">Return value</span></span>

<span data-ttu-id="af7c0-109">Devuelve **true** si la función se ejecuta correctamente; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="af7c0-109">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="af7c0-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="af7c0-110">Remarks</span></span>

<span data-ttu-id="af7c0-111">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="af7c0-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="af7c0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af7c0-112">Requirements</span></span>



| <span data-ttu-id="af7c0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="af7c0-113">Requirement</span></span> | <span data-ttu-id="af7c0-114">Value</span><span class="sxs-lookup"><span data-stu-id="af7c0-114">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af7c0-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="af7c0-115">DLL</span></span><br/> | <dl> <span data-ttu-id="af7c0-116"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af7c0-116"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
