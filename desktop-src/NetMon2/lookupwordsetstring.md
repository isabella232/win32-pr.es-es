---
description: La función LookupWordSetString devuelve la cadena correspondiente al valor solicitado de un conjunto con etiqueta.
ms.assetid: e8d158a1-8544-4c10-b8e8-46888c1097e4
title: Función LookupWordSetString (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupWordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7487becb195571e1eb88044195293b2c0b226e8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542374"
---
# <a name="lookupwordsetstring-function"></a><span data-ttu-id="9f2e4-103">LookupWordSetString función)</span><span class="sxs-lookup"><span data-stu-id="9f2e4-103">LookupWordSetString function</span></span>

<span data-ttu-id="9f2e4-104">La función **LookupWordSetString** devuelve la cadena correspondiente al valor solicitado de un conjunto con etiqueta.</span><span class="sxs-lookup"><span data-stu-id="9f2e4-104">The **LookupWordSetString** function returns the string corresponding to the requested value from a labeled set.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f2e4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f2e4-105">Syntax</span></span>


```C++
LPBYTE WINAPI LookupWordSetString(
   LPSET lpSet,
   WORD  Value
);
```



## <a name="parameters"></a><span data-ttu-id="9f2e4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f2e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f2e4-107">*lpSet*</span><span class="sxs-lookup"><span data-stu-id="9f2e4-107">*lpSet*</span></span> 
</dt> <dd>

<span data-ttu-id="9f2e4-108">Conjunto con etiqueta del que se extrae la etiqueta del valor.</span><span class="sxs-lookup"><span data-stu-id="9f2e4-108">Labeled set from which you extract the value's label.</span></span>

</dd> <dt>

<span data-ttu-id="9f2e4-109">*Valor*</span><span class="sxs-lookup"><span data-stu-id="9f2e4-109">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="9f2e4-110">Valor de un conjunto con etiqueta.</span><span class="sxs-lookup"><span data-stu-id="9f2e4-110">Value of a labeled set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f2e4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f2e4-111">Return value</span></span>

<span data-ttu-id="9f2e4-112">Si la función es correcta, el valor devuelto es una cadena que corresponde al valor solicitado.</span><span class="sxs-lookup"><span data-stu-id="9f2e4-112">If the function is successful, the return value is a string that corresponds to the requested value.</span></span>

<span data-ttu-id="9f2e4-113">Si la función no es correcta, el valor especificado no está en el conjunto, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="9f2e4-113">If the function is unsuccessful, the specified value is not in the set, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f2e4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f2e4-114">Requirements</span></span>



| <span data-ttu-id="9f2e4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f2e4-115">Requirement</span></span> | <span data-ttu-id="9f2e4-116">Value</span><span class="sxs-lookup"><span data-stu-id="9f2e4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9f2e4-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f2e4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9f2e4-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9f2e4-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9f2e4-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f2e4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9f2e4-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9f2e4-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9f2e4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f2e4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f2e4-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f2e4-122"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="9f2e4-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f2e4-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f2e4-124"><dt>Analizador. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f2e4-124"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="9f2e4-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9f2e4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f2e4-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f2e4-126"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




