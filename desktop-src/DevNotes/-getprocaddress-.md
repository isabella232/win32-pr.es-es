---
description: Obtiene la dirección de una función de un archivo DLL.
ms.assetid: e425948c-5588-4a4f-994c-4e608af18439
title: _GetProcAddress_ (función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetProcAddress_
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 0d717036b92e79056fd3b1bf69f1fd17784db713
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661158"
---
# <a name="_getprocaddress_-function"></a><span data-ttu-id="c6460-103">\_GetProcAddress ( \_ función)</span><span class="sxs-lookup"><span data-stu-id="c6460-103">\_GetProcAddress\_ function</span></span>

<span data-ttu-id="c6460-104">\[Esta función es un contenedor de la función **GetProcAddress** .</span><span class="sxs-lookup"><span data-stu-id="c6460-104">\[This function is a wrapper over the **GetProcAddress** function.</span></span> <span data-ttu-id="c6460-105">Esta función puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="c6460-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="c6460-106">Las aplicaciones deben llamar a **GetProcAddress** directamente.\]</span><span class="sxs-lookup"><span data-stu-id="c6460-106">Applications should call **GetProcAddress** directly.\]</span></span>

<span data-ttu-id="c6460-107">Obtiene la dirección de una función de un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="c6460-107">Gets the address of a function from a DLL.</span></span> <span data-ttu-id="c6460-108">Vea [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="c6460-108">See [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

## <a name="syntax"></a><span data-ttu-id="c6460-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6460-109">Syntax</span></span>


```C++
FARPROC _GetProcAddress_(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="c6460-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6460-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6460-111">*...*</span><span class="sxs-lookup"><span data-stu-id="c6460-111">*...*</span></span> 
<span data-ttu-id="c6460-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c6460-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="c6460-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6460-113">Requirements</span></span>



| <span data-ttu-id="c6460-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6460-114">Requirement</span></span> | <span data-ttu-id="c6460-115">Value</span><span class="sxs-lookup"><span data-stu-id="c6460-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6460-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c6460-116">DLL</span></span><br/> | <dl> <span data-ttu-id="c6460-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6460-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6460-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6460-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6460-119">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="c6460-119">**GetProcAddress**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 
