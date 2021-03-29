---
description: La función LookupDwordSetString devuelve la cadena correspondiente al valor especificado de un conjunto con etiqueta.
ms.assetid: ee2b1b7a-6b64-4c8c-a71d-de970b66d46e
title: Función LookupDwordSetString (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupDwordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 57688edab7421f939e03322b8b244219b00d31fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810291"
---
# <a name="lookupdwordsetstring-function"></a><span data-ttu-id="63018-103">LookupDwordSetString función)</span><span class="sxs-lookup"><span data-stu-id="63018-103">LookupDwordSetString function</span></span>

<span data-ttu-id="63018-104">La función **LookupDwordSetString** devuelve la cadena correspondiente al valor especificado de un conjunto con etiqueta.</span><span class="sxs-lookup"><span data-stu-id="63018-104">The **LookupDwordSetString** function returns the string corresponding to the specified value of a labeled set.</span></span>

## <a name="syntax"></a><span data-ttu-id="63018-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63018-105">Syntax</span></span>


```C++
LPBYTE WINAPI LookupDwordSetString(
   LPSET lpSet,
   DWORD Value
);
```



## <a name="parameters"></a><span data-ttu-id="63018-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63018-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63018-107">*lpSet*</span><span class="sxs-lookup"><span data-stu-id="63018-107">*lpSet*</span></span> 
</dt> <dd>

<span data-ttu-id="63018-108">Conjunto con etiqueta, desde el que puede extraer la etiqueta del valor.</span><span class="sxs-lookup"><span data-stu-id="63018-108">Labeled set, from which you can extract the value's label.</span></span>

</dd> <dt>

<span data-ttu-id="63018-109">*Valor*</span><span class="sxs-lookup"><span data-stu-id="63018-109">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="63018-110">Valor de un conjunto con etiqueta.</span><span class="sxs-lookup"><span data-stu-id="63018-110">Value of a labeled set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63018-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63018-111">Return value</span></span>

<span data-ttu-id="63018-112">Si la función es correcta, el valor devuelto es la cadena que corresponde al valor especificado.</span><span class="sxs-lookup"><span data-stu-id="63018-112">If the function is successful, the return value is the string that corresponds to the specified value.</span></span>

<span data-ttu-id="63018-113">Si la función no es correcta, el valor especificado no está en el conjunto, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="63018-113">If the function is unsuccessful, the specified value is not in the set, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="63018-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63018-114">Requirements</span></span>



| <span data-ttu-id="63018-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="63018-115">Requirement</span></span> | <span data-ttu-id="63018-116">Value</span><span class="sxs-lookup"><span data-stu-id="63018-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63018-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63018-117">Minimum supported client</span></span><br/> | <span data-ttu-id="63018-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="63018-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="63018-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63018-119">Minimum supported server</span></span><br/> | <span data-ttu-id="63018-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="63018-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="63018-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63018-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="63018-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="63018-122"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="63018-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="63018-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="63018-124"><dt>Analizador. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63018-124"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="63018-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="63018-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63018-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63018-126"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




