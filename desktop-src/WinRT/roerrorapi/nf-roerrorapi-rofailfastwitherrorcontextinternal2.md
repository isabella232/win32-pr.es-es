---
title: RoFailFastWithErrorContextInternal2 función)
description: Genera una excepción no continuada en el proceso actual y también permite incluir el contexto de error adicional aún no capturado por el sistema operativo.
ms.localizationpriority: low
ms.topic: reference
ms.date: 03/13/2020
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ComBase.dll
api_name:
- RoFailFastWithErrorContextInternal2
targetos: Windows
ms.openlocfilehash: 84584c339851ecbf8df5d6dbda2aaa575ca6487b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "105720182"
---
# <a name="rofailfastwitherrorcontextinternal2-function"></a><span data-ttu-id="14284-103">RoFailFastWithErrorContextInternal2 función)</span><span class="sxs-lookup"><span data-stu-id="14284-103">RoFailFastWithErrorContextInternal2 function</span></span>

<span data-ttu-id="14284-104">Genera una excepción no continuada en el proceso actual y también permite incluir el contexto de error adicional aún no capturado por el sistema operativo (SO).</span><span class="sxs-lookup"><span data-stu-id="14284-104">Raises a non-continuable exception in the current process, and also allows you to include additional error context not already captured by the operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="14284-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14284-105">Syntax</span></span>

```cpp
void WINAPI RoFailFastWithErrorContextInternal2(
  HRESULT hrError,
  ULONG cStowedExceptions,
  _In_reads_opt_(cStowedExceptions) PSTOWED_EXCEPTION_INFORMATION_V2 aStowedExceptionPointers[]
);
```

## <a name="parameters"></a><span data-ttu-id="14284-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14284-106">Parameters</span></span>

`hrError`

<span data-ttu-id="14284-107">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="14284-107">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="14284-108">**HRESULT** asociado al error actual.</span><span class="sxs-lookup"><span data-stu-id="14284-108">The **HRESULT** associated with the current error.</span></span> <span data-ttu-id="14284-109">La excepción se produce para cualquier valor de *hrError*.</span><span class="sxs-lookup"><span data-stu-id="14284-109">The exception is raised for any value of *hrError*.</span></span>

`cStowedExceptions`

<span data-ttu-id="14284-110">Tipo: **[ULong](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14284-110">Type: **[ULONG](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14284-111">Número de elementos de la matriz *aStowedExceptionPointers* .</span><span class="sxs-lookup"><span data-stu-id="14284-111">The number of elements in the *aStowedExceptionPointers* array.</span></span>

`aStowedExceptionPointers`

<span data-ttu-id="14284-112">Tipo: **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**</span><span class="sxs-lookup"><span data-stu-id="14284-112">Type: **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**</span></span>

<span data-ttu-id="14284-113">Matriz de punteros a estructuras de [**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md) .</span><span class="sxs-lookup"><span data-stu-id="14284-113">An array of pointers to [**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md) structures.</span></span> <span data-ttu-id="14284-114">Cada estructura contiene información que describe una excepción estibada.</span><span class="sxs-lookup"><span data-stu-id="14284-114">Each structure contains info describing a stowed exception.</span></span> <span data-ttu-id="14284-115">La información de estas estructuras se envía a Informe de errores de Windows (WER) junto con la información de excepción estibada capturada por la plataforma.</span><span class="sxs-lookup"><span data-stu-id="14284-115">The info in these structures is then submitted to Windows Error Reporting (WER) along with the stowed exception information that was captured by the platform.</span></span>

## <a name="return-value"></a><span data-ttu-id="14284-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14284-116">Return value</span></span>

<span data-ttu-id="14284-117">Esta función no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="14284-117">This function doesn't return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="14284-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14284-118">Remarks</span></span>

<span data-ttu-id="14284-119">**RoFailFastWithErrorContextInternal2** no está asociado a una biblioteca de importación ni a un archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="14284-119">**RoFailFastWithErrorContextInternal2** isn't associated with an import library nor a header file.</span></span> <span data-ttu-id="14284-120">Puede llamarlo primero mediante la función [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) (para cargar `ComBase.dll` ) y, a continuación, llamando a la función [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para recuperar la dirección de **RoFailFastWithErrorContextInternal2**.</span><span class="sxs-lookup"><span data-stu-id="14284-120">You can call it by first using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) function (to load `ComBase.dll`), and then by calling the [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) function to retrieve the address of **RoFailFastWithErrorContextInternal2**.</span></span>

<span data-ttu-id="14284-121">Para obtener más información, consulte [función RoFailFastWithErrorContext](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext).</span><span class="sxs-lookup"><span data-stu-id="14284-121">For more info, see [RoFailFastWithErrorContext function](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext).</span></span>

## <a name="requirements"></a><span data-ttu-id="14284-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14284-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="14284-123">**Plataforma de destino**</span><span class="sxs-lookup"><span data-stu-id="14284-123">**Target Platform**</span></span> | <span data-ttu-id="14284-124">Windows</span><span class="sxs-lookup"><span data-stu-id="14284-124">Windows</span></span> |
| <span data-ttu-id="14284-125">**Header**</span><span class="sxs-lookup"><span data-stu-id="14284-125">**Header**</span></span> | <span data-ttu-id="14284-126">N/D</span><span class="sxs-lookup"><span data-stu-id="14284-126">N/A</span></span> |
| <span data-ttu-id="14284-127">**Library**</span><span class="sxs-lookup"><span data-stu-id="14284-127">**Library**</span></span> | <span data-ttu-id="14284-128">N/D</span><span class="sxs-lookup"><span data-stu-id="14284-128">N/A</span></span> |
| <span data-ttu-id="14284-129">**DLL**</span><span class="sxs-lookup"><span data-stu-id="14284-129">**DLL**</span></span> | <span data-ttu-id="14284-130">ComBase.dll</span><span class="sxs-lookup"><span data-stu-id="14284-130">ComBase.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="14284-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="14284-131">See also</span></span>

* [<span data-ttu-id="14284-132">RoFailFastWithErrorContext función)</span><span class="sxs-lookup"><span data-stu-id="14284-132">RoFailFastWithErrorContext function</span></span>](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext)