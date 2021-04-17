---
description: Obtiene la ruta de acceso del módulo.
ms.assetid: ff632357-8d4a-4de4-a69a-0be9e380639d
title: _GetModuleFileName función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetModuleFileName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 5bf18e8baac62de6474f4ce1e48a0ae115ced778
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661160"
---
# <a name="_getmodulefilename-function"></a><span data-ttu-id="d2e02-103">\_GetModuleFileName, función</span><span class="sxs-lookup"><span data-stu-id="d2e02-103">\_GetModuleFileName function</span></span>

<span data-ttu-id="d2e02-104">\[Esta función es un contenedor de la función **GetModuleFileName** .</span><span class="sxs-lookup"><span data-stu-id="d2e02-104">\[This function is a wrapper over the **GetModuleFileName** function.</span></span> <span data-ttu-id="d2e02-105">Esta función puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="d2e02-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="d2e02-106">Las aplicaciones deben llamar a **GetModuleFileName** directamente.\]</span><span class="sxs-lookup"><span data-stu-id="d2e02-106">Applications should call **GetModuleFileName** directly.\]</span></span>

<span data-ttu-id="d2e02-107">Obtiene la ruta de acceso del módulo.</span><span class="sxs-lookup"><span data-stu-id="d2e02-107">Gets the module path.</span></span> <span data-ttu-id="d2e02-108">Vea [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea).</span><span class="sxs-lookup"><span data-stu-id="d2e02-108">See [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea).</span></span>

## <a name="syntax"></a><span data-ttu-id="d2e02-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2e02-109">Syntax</span></span>


```C++
DWORD _GetModuleFileName(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="d2e02-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2e02-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2e02-111">*...*</span><span class="sxs-lookup"><span data-stu-id="d2e02-111">*...*</span></span> 
<span data-ttu-id="d2e02-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d2e02-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d2e02-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2e02-113">Requirements</span></span>



| <span data-ttu-id="d2e02-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2e02-114">Requirement</span></span> | <span data-ttu-id="d2e02-115">Value</span><span class="sxs-lookup"><span data-stu-id="d2e02-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2e02-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d2e02-116">DLL</span></span><br/> | <dl> <span data-ttu-id="d2e02-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2e02-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2e02-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2e02-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2e02-119">**GetModuleFileName**</span><span class="sxs-lookup"><span data-stu-id="d2e02-119">**GetModuleFileName**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
