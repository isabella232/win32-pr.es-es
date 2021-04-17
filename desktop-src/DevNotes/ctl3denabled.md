---
description: Comprueba si los controles pueden utilizar efectos 3D.
ms.assetid: fb7b892f-2580-41ac-b2ef-938da3cc1dc2
title: Ctl3dEnabled función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dEnabled
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: d0eecec5650ecc00b69c0745e58a3e1d0f931a00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661109"
---
# <a name="ctl3denabled-function"></a><span data-ttu-id="5f940-103">Ctl3dEnabled función)</span><span class="sxs-lookup"><span data-stu-id="5f940-103">Ctl3dEnabled function</span></span>

<span data-ttu-id="5f940-104">Comprueba si los controles pueden utilizar efectos 3D.</span><span class="sxs-lookup"><span data-stu-id="5f940-104">Verifies whether controls can use 3D effects.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f940-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f940-105">Syntax</span></span>


```C++
BOOL Ctl3dEnabled(void);
```



## <a name="parameters"></a><span data-ttu-id="5f940-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f940-106">Parameters</span></span>

<span data-ttu-id="5f940-107">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5f940-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f940-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f940-108">Return value</span></span>

<span data-ttu-id="5f940-109">Devuelve **true** si los controles pueden utilizar efectos 3D; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="5f940-109">Returns **TRUE** if controls can use 3D effects; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f940-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f940-110">Remarks</span></span>

<span data-ttu-id="5f940-111">En Windows 4,0 o posterior, **Ctl3dEnabled** y [**Ctl3dRegister**](ctl3dregister.md) devuelven **false**.</span><span class="sxs-lookup"><span data-stu-id="5f940-111">In Windows 4.0 or later, **Ctl3dEnabled** and [**Ctl3dRegister**](ctl3dregister.md) return **FALSE**.</span></span>

<span data-ttu-id="5f940-112">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="5f940-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f940-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f940-113">Requirements</span></span>



| <span data-ttu-id="5f940-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f940-114">Requirement</span></span> | <span data-ttu-id="5f940-115">Value</span><span class="sxs-lookup"><span data-stu-id="5f940-115">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f940-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5f940-116">DLL</span></span><br/> | <dl> <span data-ttu-id="5f940-117"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f940-117"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
