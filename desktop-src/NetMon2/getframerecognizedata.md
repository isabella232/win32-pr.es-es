---
description: La función GetFrameRecognizeData devuelve una tabla de estructuras RECOGNIZEDATA. Cada una de estas estructuras contiene un identificador de protocolo y un desplazamiento que apunta al inicio del protocolo especificado en los datos.
ms.assetid: 3bf809ff-8d87-4746-95ee-fb68c5e51d42
title: Función GetFrameRecognizeData (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameRecognizeData
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 627ba046b3adead0291239f5d94f4e56958e6a80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000929"
---
# <a name="getframerecognizedata-function"></a><span data-ttu-id="8b18c-104">GetFrameRecognizeData función)</span><span class="sxs-lookup"><span data-stu-id="8b18c-104">GetFrameRecognizeData function</span></span>

<span data-ttu-id="8b18c-105">La función **GetFrameRecognizeData** devuelve una tabla de estructuras **RECOGNIZEDATA** .</span><span class="sxs-lookup"><span data-stu-id="8b18c-105">The **GetFrameRecognizeData** function returns a table of **RECOGNIZEDATA** structures.</span></span> <span data-ttu-id="8b18c-106">Cada una de estas estructuras contiene un identificador de protocolo y un desplazamiento que apunta al inicio del protocolo especificado en los datos.</span><span class="sxs-lookup"><span data-stu-id="8b18c-106">Each of these structures contains a protocol identifier and an offset that points to the start of the specified protocol in the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b18c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b18c-107">Syntax</span></span>


```C++
LPRECOGNIZEDATATABLE WINAPI GetFrameRecognizeData(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="8b18c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b18c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b18c-109">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8b18c-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b18c-110">Identificador de un marco.</span><span class="sxs-lookup"><span data-stu-id="8b18c-110">Handle to a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b18c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b18c-111">Return value</span></span>

<span data-ttu-id="8b18c-112">Si la función se realiza correctamente, el valor devuelto es un puntero a una estructura **RECOGNIZEDATATABLE** .</span><span class="sxs-lookup"><span data-stu-id="8b18c-112">If the function is successful, the return value is a pointer to a **RECOGNIZEDATATABLE** structure.</span></span>

<span data-ttu-id="8b18c-113">Si la función no es correcta, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="8b18c-113">If the function is not successful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b18c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8b18c-114">Remarks</span></span>

<span data-ttu-id="8b18c-115">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetFrameRecognizeData** .</span><span class="sxs-lookup"><span data-stu-id="8b18c-115">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameRecognizeData** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b18c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b18c-116">Requirements</span></span>



| <span data-ttu-id="8b18c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b18c-117">Requirement</span></span> | <span data-ttu-id="8b18c-118">Value</span><span class="sxs-lookup"><span data-stu-id="8b18c-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8b18c-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b18c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8b18c-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8b18c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8b18c-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b18c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8b18c-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8b18c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8b18c-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b18c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b18c-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b18c-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="8b18c-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8b18c-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="8b18c-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b18c-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="8b18c-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8b18c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b18c-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b18c-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




