---
description: Carga una biblioteca.
ms.assetid: 191fcbd8-4542-4cad-955e-6951f3005fc5
title: _LoadLibrary función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _LoadLibrary
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: ce4502813c1ca2a292486a18f1946f4c605c96cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649590"
---
# <a name="_loadlibrary-function"></a><span data-ttu-id="ba81b-103">\_LoadLibrary (función)</span><span class="sxs-lookup"><span data-stu-id="ba81b-103">\_LoadLibrary function</span></span>

<span data-ttu-id="ba81b-104">\[Esta función es un contenedor de la función **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="ba81b-104">\[This function is a wrapper over the **LoadLibrary** function.</span></span> <span data-ttu-id="ba81b-105">Esta función puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="ba81b-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="ba81b-106">Las aplicaciones deben llamar a **LoadLibrary** directamente.\]</span><span class="sxs-lookup"><span data-stu-id="ba81b-106">Applications should call **LoadLibrary** directly.\]</span></span>

<span data-ttu-id="ba81b-107">Carga una biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ba81b-107">Loads a library.</span></span> <span data-ttu-id="ba81b-108">Consulte [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span><span class="sxs-lookup"><span data-stu-id="ba81b-108">See [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span>

## <a name="syntax"></a><span data-ttu-id="ba81b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba81b-109">Syntax</span></span>


```C++
HMODULE _LoadLibrary(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="ba81b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba81b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba81b-111">*...*</span><span class="sxs-lookup"><span data-stu-id="ba81b-111">*...*</span></span> 
<span data-ttu-id="ba81b-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ba81b-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ba81b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba81b-113">Requirements</span></span>



| <span data-ttu-id="ba81b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba81b-114">Requirement</span></span> | <span data-ttu-id="ba81b-115">Value</span><span class="sxs-lookup"><span data-stu-id="ba81b-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba81b-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ba81b-116">DLL</span></span><br/> | <dl> <span data-ttu-id="ba81b-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba81b-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba81b-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba81b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba81b-119">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="ba81b-119">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
