---
description: Recupera el estilo de color de fondo del estilo especificado.
ms.assetid: 1b0acac1-c36d-49b6-8154-f69bda008e9a
title: PColorStyleBackFromIMEStyle función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PColorStyleBackFromIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 33ff9072fc5e850654f932817cd4ecf0e9372aad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671009"
---
# <a name="pcolorstylebackfromimestyle-function"></a><span data-ttu-id="266ad-103">PColorStyleBackFromIMEStyle función)</span><span class="sxs-lookup"><span data-stu-id="266ad-103">PColorStyleBackFromIMEStyle function</span></span>

<span data-ttu-id="266ad-104">Recupera el estilo de color de fondo del estilo especificado.</span><span class="sxs-lookup"><span data-stu-id="266ad-104">Retrieves the background color style of the specified style.</span></span>

## <a name="syntax"></a><span data-ttu-id="266ad-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="266ad-105">Syntax</span></span>


```C++
const IMECOLORSTY* __cdecl PColorStyleBackFromIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="266ad-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="266ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="266ad-107">*pimestyle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="266ad-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="266ad-108">Una estructura **IMESTYLE** devuelta por la función [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="266ad-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="266ad-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="266ad-109">Return value</span></span>

<span data-ttu-id="266ad-110">Puntero a una estructura **IMECOLORSTY** que representa el estilo de color de fondo.</span><span class="sxs-lookup"><span data-stu-id="266ad-110">Pointer to an **IMECOLORSTY** structure representing the background color style.</span></span>

## <a name="remarks"></a><span data-ttu-id="266ad-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="266ad-111">Remarks</span></span>

<span data-ttu-id="266ad-112">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="266ad-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="266ad-113">La estructura **IMECOLORSTY** se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="266ad-113">The **IMECOLORSTY** structure is defined as follows:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="266ad-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="266ad-114">Requirements</span></span>



| <span data-ttu-id="266ad-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="266ad-115">Requirement</span></span> | <span data-ttu-id="266ad-116">Value</span><span class="sxs-lookup"><span data-stu-id="266ad-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="266ad-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="266ad-117">DLL</span></span><br/> | <dl> <span data-ttu-id="266ad-118"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="266ad-118"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="266ad-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="266ad-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="266ad-120">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="266ad-120">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
