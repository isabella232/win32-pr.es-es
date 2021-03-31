---
description: La función HTMLValueToUnicode convierte una \_ cadena UTF8 de CP HTML en una cadena Unicode.
ms.assetid: d175476e-9c84-48b8-9c89-00255b7cb638
title: Función HTMLValueToUnicode (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HTMLValueToUnicode
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8ef5f4a2b49139ce1ab5366dac3f6c141425653e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808701"
---
# <a name="htmlvaluetounicode-function"></a><span data-ttu-id="0bb37-103">HTMLValueToUnicode función)</span><span class="sxs-lookup"><span data-stu-id="0bb37-103">HTMLValueToUnicode function</span></span>

<span data-ttu-id="0bb37-104">La función **HTMLValueToUnicode** convierte una \_ cadena UTF8 de CP HTML en una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="0bb37-104">The **HTMLValueToUnicode** function converts an HTML CP\_UTF8 string to a Unicode string.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bb37-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0bb37-105">Syntax</span></span>


```C++
WCHAR* HTMLValueToUnicode(
  _Inout_ const char *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="0bb37-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0bb37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bb37-107">*pValue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0bb37-107">*pValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bb37-108">En la entrada, puntero a la cadena HTML proporcionada por MCSVC.</span><span class="sxs-lookup"><span data-stu-id="0bb37-108">On input, pointer to the HTML string supplied by the MCSVC.</span></span>

<span data-ttu-id="0bb37-109">En la salida, puntero a la cadena Unicode convertida.</span><span class="sxs-lookup"><span data-stu-id="0bb37-109">On output, pointer to the converted Unicode string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bb37-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0bb37-110">Return value</span></span>

<span data-ttu-id="0bb37-111">La función devuelve el equivalente Unicode de la cadena.</span><span class="sxs-lookup"><span data-stu-id="0bb37-111">The function returns the Unicode equivalent of the string.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bb37-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bb37-112">Requirements</span></span>



| <span data-ttu-id="0bb37-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bb37-113">Requirement</span></span> | <span data-ttu-id="0bb37-114">Value</span><span class="sxs-lookup"><span data-stu-id="0bb37-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0bb37-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0bb37-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0bb37-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0bb37-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0bb37-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0bb37-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0bb37-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0bb37-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0bb37-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0bb37-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bb37-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bb37-120"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="0bb37-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0bb37-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="0bb37-122"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0bb37-122"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="0bb37-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0bb37-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bb37-124"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bb37-124"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




