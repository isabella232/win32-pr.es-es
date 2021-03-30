---
description: La función GetPropertyInfo devuelve un puntero a la información de propiedad de un protocolo determinado.
ms.assetid: f65166ba-1d94-4d65-b9d7-edb84ada0826
title: Función GetPropertyInfo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 007332a85f170f865604526199681cad6d68cdcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907669"
---
# <a name="getpropertyinfo-function"></a><span data-ttu-id="d0386-103">GetPropertyInfo función)</span><span class="sxs-lookup"><span data-stu-id="d0386-103">GetPropertyInfo function</span></span>

<span data-ttu-id="d0386-104">La función **GetPropertyInfo** devuelve un puntero a la información de propiedad de un protocolo determinado.</span><span class="sxs-lookup"><span data-stu-id="d0386-104">The **GetPropertyInfo** function returns a pointer to the property information of a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0386-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0386-105">Syntax</span></span>


```C++
LPPROPERTYINFO WINAPI GetPropertyInfo(
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a><span data-ttu-id="d0386-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0386-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0386-107">*hProperty* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0386-107">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0386-108">Identificador de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="d0386-108">Handle to a property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0386-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0386-109">Return value</span></span>

<span data-ttu-id="d0386-110">Si la función se realiza correctamente, el valor devuelto es un puntero a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d0386-110">If the function is successful, the return value is a pointer to the property.</span></span>

<span data-ttu-id="d0386-111">Si la función no se realiza correctamente, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="d0386-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0386-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0386-112">Remarks</span></span>

<span data-ttu-id="d0386-113">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetPropertyInfo** .</span><span class="sxs-lookup"><span data-stu-id="d0386-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetPropertyInfo** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0386-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0386-114">Requirements</span></span>



| <span data-ttu-id="d0386-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0386-115">Requirement</span></span> | <span data-ttu-id="d0386-116">Value</span><span class="sxs-lookup"><span data-stu-id="d0386-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d0386-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0386-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d0386-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d0386-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d0386-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0386-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d0386-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d0386-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d0386-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0386-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0386-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0386-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d0386-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d0386-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="d0386-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0386-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d0386-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d0386-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0386-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0386-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




