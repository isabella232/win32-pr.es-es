---
description: Identifica si el estilo que no es de color especificado tiene subrayado.
ms.assetid: 72056bf7-0a18-4ad3-a8c4-d2335a7218ae
title: IdUlIMEStyle función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IdUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 262f726e8b2201b809a9416a67c2af860acee65e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650001"
---
# <a name="idulimestyle-function"></a><span data-ttu-id="57600-103">IdUlIMEStyle función)</span><span class="sxs-lookup"><span data-stu-id="57600-103">IdUlIMEStyle function</span></span>

<span data-ttu-id="57600-104">Identifica si el estilo que no es de color especificado tiene subrayado.</span><span class="sxs-lookup"><span data-stu-id="57600-104">Identifies whether the specified non-color style has underline.</span></span>

## <a name="syntax"></a><span data-ttu-id="57600-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57600-105">Syntax</span></span>


```C++
UINT __cdecl IdUlIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="57600-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57600-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57600-107">*pimestyle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="57600-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57600-108">Una estructura **IMESTYLE** devuelta por la función [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="57600-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57600-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57600-109">Return value</span></span>

<span data-ttu-id="57600-110">Esta función puede devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="57600-110">This function can returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="57600-111">**IMESTY \_ UL \_ min** (2002)</span><span class="sxs-lookup"><span data-stu-id="57600-111">**IMESTY\_UL\_MIN** (2002)</span></span>
</dt> <dt>

<span data-ttu-id="57600-112">**IMESTY \_ UL \_ ninguno** (2002)</span><span class="sxs-lookup"><span data-stu-id="57600-112">**IMESTY\_UL\_NONE** (2002)</span></span>
</dt> <dt>

<span data-ttu-id="57600-113">**IMESTY \_ UL \_ único** (2003)</span><span class="sxs-lookup"><span data-stu-id="57600-113">**IMESTY\_UL\_SINGLE** (2003)</span></span>
</dt> <dt>

<span data-ttu-id="57600-114">**IMESTY \_ UL \_ puntos** (2005)</span><span class="sxs-lookup"><span data-stu-id="57600-114">**IMESTY\_UL\_DOTTED** (2005)</span></span>
</dt> <dt>

<span data-ttu-id="57600-115">**IMESTY \_ \_Gruesa UL** (2006)</span><span class="sxs-lookup"><span data-stu-id="57600-115">**IMESTY\_UL\_THICK** (2006)</span></span>
</dt> <dt>

<span data-ttu-id="57600-116">**IMESTY \_ UL \_ inferior** (2011)</span><span class="sxs-lookup"><span data-stu-id="57600-116">**IMESTY\_UL\_LOWER** (2011)</span></span>
</dt> <dt>

<span data-ttu-id="57600-117">**IMESTY \_ UL \_ THICKLOWER** (2012)</span><span class="sxs-lookup"><span data-stu-id="57600-117">**IMESTY\_UL\_THICKLOWER** (2012)</span></span>
</dt> <dt>

<span data-ttu-id="57600-118">**IMESTY \_ UL \_ THICKDITHLOWER** (2013)</span><span class="sxs-lookup"><span data-stu-id="57600-118">**IMESTY\_UL\_THICKDITHLOWER** (2013)</span></span>
</dt> <dt>

<span data-ttu-id="57600-119">**IMESTY \_ UL \_ DITHLOWER** (2014)</span><span class="sxs-lookup"><span data-stu-id="57600-119">**IMESTY\_UL\_DITHLOWER** (2014)</span></span>
</dt> <dt>

<span data-ttu-id="57600-120">**IMESTY \_ UL \_ máx** . (2014)</span><span class="sxs-lookup"><span data-stu-id="57600-120">**IMESTY\_UL\_MAX** (2014)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="57600-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57600-121">Remarks</span></span>

<span data-ttu-id="57600-122">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="57600-122">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="57600-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57600-123">Requirements</span></span>



| <span data-ttu-id="57600-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="57600-124">Requirement</span></span> | <span data-ttu-id="57600-125">Value</span><span class="sxs-lookup"><span data-stu-id="57600-125">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57600-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="57600-126">DLL</span></span><br/> | <dl> <span data-ttu-id="57600-127"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57600-127"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57600-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="57600-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57600-129">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="57600-129">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
