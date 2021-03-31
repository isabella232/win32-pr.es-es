---
description: La función GetProtocolFromName devuelve un identificador a un protocolo de un nombre determinado.
ms.assetid: 18f5a9a7-4245-479d-a0da-2ede362a60b8
title: Función GetProtocolFromName (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e104c066be2a5465083c7983aaefebd46f548b7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808707"
---
# <a name="getprotocolfromname-function"></a><span data-ttu-id="c8c6a-103">GetProtocolFromName función)</span><span class="sxs-lookup"><span data-stu-id="c8c6a-103">GetProtocolFromName function</span></span>

<span data-ttu-id="c8c6a-104">La función **GetProtocolFromName** devuelve un identificador a un protocolo de un nombre determinado.</span><span class="sxs-lookup"><span data-stu-id="c8c6a-104">The **GetProtocolFromName** function returns a handle to a protocol of a given name.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8c6a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8c6a-105">Syntax</span></span>


```C++
HPROTOCOL WINAPI GetProtocolFromName(
  _In_ LPSTR ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="c8c6a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8c6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8c6a-107">*ProtocolName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c8c6a-107">*ProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8c6a-108">Nombre del Protocolo (por ejemplo, IP).</span><span class="sxs-lookup"><span data-stu-id="c8c6a-108">Protocol name (for example, IP).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8c6a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8c6a-109">Return value</span></span>

<span data-ttu-id="c8c6a-110">Si la función se realiza correctamente, el valor devuelto es un identificador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="c8c6a-110">If the function is successful, the return value is a protocol handle.</span></span>

<span data-ttu-id="c8c6a-111">Si la función no se realiza correctamente, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="c8c6a-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8c6a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8c6a-112">Remarks</span></span>

<span data-ttu-id="c8c6a-113">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetProtocolFromName** .</span><span class="sxs-lookup"><span data-stu-id="c8c6a-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProtocolFromName** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8c6a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8c6a-114">Requirements</span></span>



| <span data-ttu-id="c8c6a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8c6a-115">Requirement</span></span> | <span data-ttu-id="c8c6a-116">Value</span><span class="sxs-lookup"><span data-stu-id="c8c6a-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c8c6a-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8c6a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c8c6a-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c8c6a-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c8c6a-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8c6a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c8c6a-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c8c6a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c8c6a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8c6a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8c6a-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8c6a-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="c8c6a-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c8c6a-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="c8c6a-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8c6a-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c8c6a-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8c6a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8c6a-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8c6a-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




