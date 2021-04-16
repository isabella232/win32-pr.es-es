---
description: La función LookupByteSetString devuelve la cadena correspondiente al valor especificado de un conjunto con etiqueta.
ms.assetid: 295891f9-dc8d-4dbe-aac9-7d0a96993cfa
title: Función LookupByteSetString (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupByteSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7a2b5bffbfcb30ed8ec00da42fbc9ad6008fd5ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677411"
---
# <a name="lookupbytesetstring-function"></a><span data-ttu-id="4d0db-103">LookupByteSetString función)</span><span class="sxs-lookup"><span data-stu-id="4d0db-103">LookupByteSetString function</span></span>

<span data-ttu-id="4d0db-104">La función **LookupByteSetString** devuelve la cadena correspondiente al valor especificado de un conjunto con etiqueta.</span><span class="sxs-lookup"><span data-stu-id="4d0db-104">The **LookupByteSetString** function returns the string corresponding to the specified value of a labeled set.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d0db-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d0db-105">Syntax</span></span>


```C++
LPBYTE WINAPI LookupByteSetString(
   LPSET lpSet,
   BYTE  Value
);
```



## <a name="parameters"></a><span data-ttu-id="4d0db-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d0db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d0db-107">*lpSet*</span><span class="sxs-lookup"><span data-stu-id="4d0db-107">*lpSet*</span></span> 
</dt> <dd>

<span data-ttu-id="4d0db-108">Puntero a un conjunto con etiqueta, desde el que puede extraer la etiqueta del valor.</span><span class="sxs-lookup"><span data-stu-id="4d0db-108">Pointer to a labeled set, from which you can extract the value's label.</span></span>

</dd> <dt>

<span data-ttu-id="4d0db-109">*Valor*</span><span class="sxs-lookup"><span data-stu-id="4d0db-109">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="4d0db-110">Valor de un conjunto con etiqueta.</span><span class="sxs-lookup"><span data-stu-id="4d0db-110">Value of a labeled set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d0db-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d0db-111">Return value</span></span>

<span data-ttu-id="4d0db-112">Si la función es correcta, el valor devuelto es una cadena que corresponde al valor proporcionado.</span><span class="sxs-lookup"><span data-stu-id="4d0db-112">If the function is successful, the return value is a string corresponding to the value provided.</span></span>

<span data-ttu-id="4d0db-113">Si la función no se realiza correctamente, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="4d0db-113">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d0db-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d0db-114">Requirements</span></span>



| <span data-ttu-id="4d0db-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d0db-115">Requirement</span></span> | <span data-ttu-id="4d0db-116">Value</span><span class="sxs-lookup"><span data-stu-id="4d0db-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d0db-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d0db-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4d0db-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4d0db-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4d0db-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d0db-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4d0db-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4d0db-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4d0db-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d0db-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d0db-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d0db-122"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="4d0db-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4d0db-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="4d0db-124"><dt>Analizador. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d0db-124"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="4d0db-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4d0db-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d0db-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d0db-126"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




