---
UID: ''
title: UnicodeToBytes función)
description: Convierte los caracteres Unicode a GB18030 bytes.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: WideCharToMultiByte, MultiByteToWideChar
ms.topic: reference
req.header: Gb18030.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: c_g18030.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- c_g18030.dll
api_name:
- UnicodeToBytes
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 66ed21768c3acef7f2aa2128df057da8552b2ad2
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2020
ms.locfileid: "103785489"
---
# <a name="unicodetobytes-function"></a><span data-ttu-id="31d7a-103">UnicodeToBytes función)</span><span class="sxs-lookup"><span data-stu-id="31d7a-103">UnicodeToBytes function</span></span>

## <a name="description"></a><span data-ttu-id="31d7a-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="31d7a-104">Description</span></span>

<span data-ttu-id="31d7a-105">En desuso.</span><span class="sxs-lookup"><span data-stu-id="31d7a-105">Deprecated.</span></span> <span data-ttu-id="31d7a-106">Convierte los caracteres Unicode a GB18030 bytes.</span><span class="sxs-lookup"><span data-stu-id="31d7a-106">Converts Unicode characters to GB18030 bytes.</span></span>

<span data-ttu-id="31d7a-107">**Nota:**  Al convertir los caracteres Unicode a GB18030 bytes, una aplicación que se ejecute en Windows Vista y versiones posteriores debería usar la función [WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) .</span><span class="sxs-lookup"><span data-stu-id="31d7a-107">**Note**  When converting Unicode characters to GB18030 bytes, an application to run on Windows Vista and later should use the [WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) function.</span></span>

```cpp
DWORD UnicodeToBytes(
  _In_ LPWSTR lpWideCharStr,
  _In_ UINT   cchWideChar,
  _In_ LPSTR  lpMultiByteStr,
  _In_ UINT   cchMultiByte
);
```

## <a name="parameters"></a><span data-ttu-id="31d7a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31d7a-108">Parameters</span></span>

### <a name="lpwidecharstr-in"></a><span data-ttu-id="31d7a-109">lpWideCharStr [in]</span><span class="sxs-lookup"><span data-stu-id="31d7a-109">lpWideCharStr [in]</span></span>

<span data-ttu-id="31d7a-110">Puntero a la cadena Unicode que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="31d7a-110">Pointer to the Unicode string to convert.</span></span>

### <a name="cchwidechar-in"></a><span data-ttu-id="31d7a-111">cchWideChar [in]</span><span class="sxs-lookup"><span data-stu-id="31d7a-111">cchWideChar [in]</span></span>

<span data-ttu-id="31d7a-112">Recuento de caracteres de la cadena Unicode que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="31d7a-112">Character count of the Unicode string to convert.</span></span>

### <a name="lpmultibytestr-in"></a><span data-ttu-id="31d7a-113">lpMultiByteStr [in]</span><span class="sxs-lookup"><span data-stu-id="31d7a-113">lpMultiByteStr [in]</span></span>

<span data-ttu-id="31d7a-114">Puntero al búfer multibyte de destino.</span><span class="sxs-lookup"><span data-stu-id="31d7a-114">Pointer to the target multibyte buffer.</span></span>
<span data-ttu-id="31d7a-115">Si *lpMultiByteStr* es 0, se devuelve el recuento de bytes del resultado de GB18030 y no se realiza ninguna conversión.</span><span class="sxs-lookup"><span data-stu-id="31d7a-115">If *lpMultiByteStr* is 0, the byte count of the GB18030 result is returned, and no conversion is done.</span></span>

### <a name="cchmultibyte-in"></a><span data-ttu-id="31d7a-116">cchMultiByte [in]</span><span class="sxs-lookup"><span data-stu-id="31d7a-116">cchMultiByte [in]</span></span>

<span data-ttu-id="31d7a-117">Recuento de bytes del búfer multibyte de destino.</span><span class="sxs-lookup"><span data-stu-id="31d7a-117">Byte count of the target multibyte buffer.</span></span>
<span data-ttu-id="31d7a-118">Si *cchMultiByte* es 0, se devuelve el recuento de bytes del resultado de GB18030 y no se realiza ninguna conversión.</span><span class="sxs-lookup"><span data-stu-id="31d7a-118">If *cchMultiByte* is 0, the byte count of the GB18030 result is returned, and no conversion is done.</span></span>

## <a name="returns"></a><span data-ttu-id="31d7a-119">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="31d7a-119">Returns</span></span>

<span data-ttu-id="31d7a-120">Devuelve el recuento de bytes de los caracteres multibyte que se generan si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="31d7a-120">Returns the byte count of the multibyte characters that are generated, if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="31d7a-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31d7a-121">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="31d7a-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="31d7a-122">See also</span></span>

[<span data-ttu-id="31d7a-123">WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="31d7a-123">WideCharToMultiByte</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)

[<span data-ttu-id="31d7a-124">MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="31d7a-124">MultiByteToWideChar</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
