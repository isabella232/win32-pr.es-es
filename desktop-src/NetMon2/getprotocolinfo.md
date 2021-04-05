---
description: La función GetProtocolInfo devuelve un puntero a un valor de información de protocolo.
ms.assetid: 1ba47889-b2ed-47ba-94f9-1b781af6d01f
title: Función GetProtocolInfo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2ec9fb58957c2e0fd64bc1c5878892fe6542af8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000922"
---
# <a name="getprotocolinfo-function"></a><span data-ttu-id="6f5b4-103">GetProtocolInfo función)</span><span class="sxs-lookup"><span data-stu-id="6f5b4-103">GetProtocolInfo function</span></span>

<span data-ttu-id="6f5b4-104">La función **GetProtocolInfo** devuelve un puntero a un valor de información de protocolo.</span><span class="sxs-lookup"><span data-stu-id="6f5b4-104">The **GetProtocolInfo** function returns a pointer to a protocol information value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f5b4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f5b4-105">Syntax</span></span>


```C++
LPPROTOCOLINFO WINAPI GetProtocolInfo(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="6f5b4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f5b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f5b4-107">*hProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f5b4-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f5b4-108">Identificador de un protocolo.</span><span class="sxs-lookup"><span data-stu-id="6f5b4-108">Handle to a protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f5b4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f5b4-109">Return value</span></span>

<span data-ttu-id="6f5b4-110">Si la función se realiza correctamente, el valor devuelto es un puntero al valor de información del protocolo.</span><span class="sxs-lookup"><span data-stu-id="6f5b4-110">If the function is successful, the return value is a pointer to the protocol information value.</span></span>

<span data-ttu-id="6f5b4-111">Si la función no se realiza correctamente, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="6f5b4-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f5b4-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f5b4-112">Remarks</span></span>

<span data-ttu-id="6f5b4-113">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetProtocolInfo** .</span><span class="sxs-lookup"><span data-stu-id="6f5b4-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProtocolInfo** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f5b4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f5b4-114">Requirements</span></span>



| <span data-ttu-id="6f5b4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f5b4-115">Requirement</span></span> | <span data-ttu-id="6f5b4-116">Value</span><span class="sxs-lookup"><span data-stu-id="6f5b4-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6f5b4-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f5b4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6f5b4-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6f5b4-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6f5b4-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f5b4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6f5b4-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6f5b4-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6f5b4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f5b4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f5b4-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f5b4-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="6f5b4-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6f5b4-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="6f5b4-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f5b4-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="6f5b4-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f5b4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f5b4-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f5b4-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




