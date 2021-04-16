---
description: Recupera el estilo de color del texto del estilo especificado.
ms.assetid: 242c37af-5b39-4b18-9c8f-4e692f41c497
title: PColorStyleTextFromIMEStyle función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PColorStyleTextFromIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 791fdaca4a93b0a44099306b8ae14ae4d5cb11cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649960"
---
# <a name="pcolorstyletextfromimestyle-function"></a><span data-ttu-id="833dd-103">PColorStyleTextFromIMEStyle función)</span><span class="sxs-lookup"><span data-stu-id="833dd-103">PColorStyleTextFromIMEStyle function</span></span>

<span data-ttu-id="833dd-104">Recupera el estilo de color del texto del estilo especificado.</span><span class="sxs-lookup"><span data-stu-id="833dd-104">Retrieves the text color style of the specified style.</span></span>

## <a name="syntax"></a><span data-ttu-id="833dd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="833dd-105">Syntax</span></span>


```C++
const IMECOLORSTY* __cdecl PColorStyleTextFromIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="833dd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="833dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="833dd-107">*pimestyle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="833dd-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="833dd-108">Una estructura **IMESTYLE** devuelta por la función [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="833dd-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="833dd-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="833dd-109">Return value</span></span>

<span data-ttu-id="833dd-110">Puntero a una estructura **IMECOLORSTY** que representa el estilo de color del texto.</span><span class="sxs-lookup"><span data-stu-id="833dd-110">Pointer to an **IMECOLORSTY** structure representing the text color style.</span></span>

## <a name="remarks"></a><span data-ttu-id="833dd-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="833dd-111">Remarks</span></span>

<span data-ttu-id="833dd-112">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="833dd-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="833dd-113">La estructura **IMECOLORSTY** se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="833dd-113">The **IMECOLORSTY** structure is defined as follows:</span></span>

``` syntax
typedef struct {
    UINT colorId;
    union {
        COLORREF    rgb;
        UINT        colorWin;
        UINT        colorSpec;
        UINT        colorFund;
    };
} IMECOLORSTY;
```

## <a name="requirements"></a><span data-ttu-id="833dd-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="833dd-114">Requirements</span></span>



| <span data-ttu-id="833dd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="833dd-115">Requirement</span></span> | <span data-ttu-id="833dd-116">Value</span><span class="sxs-lookup"><span data-stu-id="833dd-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="833dd-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="833dd-117">DLL</span></span><br/> | <dl> <span data-ttu-id="833dd-118"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="833dd-118"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="833dd-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="833dd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="833dd-120">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="833dd-120">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
