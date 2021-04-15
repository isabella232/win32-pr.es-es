---
description: Especifica si el color especificado es un color de ventana especial.
ms.assetid: 41f7d4fb-9718-42a8-89df-c29bd8c0665b
title: FSpecialWindowIMEColorStyle función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialWindowIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 6fb667186789361a106a23f8daa82088b9bcb2ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649682"
---
# <a name="fspecialwindowimecolorstyle-function"></a><span data-ttu-id="262ce-103">FSpecialWindowIMEColorStyle función)</span><span class="sxs-lookup"><span data-stu-id="262ce-103">FSpecialWindowIMEColorStyle function</span></span>

<span data-ttu-id="262ce-104">Especifica si el color especificado es un color de ventana especial.</span><span class="sxs-lookup"><span data-stu-id="262ce-104">Specifies whether the specified color is a special window color.</span></span>

## <a name="syntax"></a><span data-ttu-id="262ce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="262ce-105">Syntax</span></span>


```C++
BOOL __cdecl FSpecialWindowIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="262ce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="262ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="262ce-107">*pcolorstyle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="262ce-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="262ce-108">Una estructura **IMECOLORSTY** devuelta por una función [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) o [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="262ce-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="262ce-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="262ce-109">Return value</span></span>

<span data-ttu-id="262ce-110">Devuelve **verdadero** cuando el color es un color de ventana especial (uno de color especial).</span><span class="sxs-lookup"><span data-stu-id="262ce-110">Returns **TRUE** when the color is a special window color (one of special color).</span></span>

## <a name="remarks"></a><span data-ttu-id="262ce-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="262ce-111">Remarks</span></span>

<span data-ttu-id="262ce-112">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="262ce-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="262ce-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="262ce-113">Requirements</span></span>



| <span data-ttu-id="262ce-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="262ce-114">Requirement</span></span> | <span data-ttu-id="262ce-115">Value</span><span class="sxs-lookup"><span data-stu-id="262ce-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="262ce-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="262ce-116">DLL</span></span><br/> | <dl> <span data-ttu-id="262ce-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="262ce-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="262ce-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="262ce-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="262ce-119">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="262ce-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="262ce-120">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="262ce-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
