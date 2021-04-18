---
description: Especifica si un estilo que no es de color tiene el estilo de cursiva.
ms.assetid: 4295c0b1-6e37-4fa9-9015-68bcc4784cda
title: FItalicIMEStyle función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FItalicIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 828e701773d666830473e92afc73f80ccdae3bc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649941"
---
# <a name="fitalicimestyle-function"></a><span data-ttu-id="72c92-103">FItalicIMEStyle función)</span><span class="sxs-lookup"><span data-stu-id="72c92-103">FItalicIMEStyle function</span></span>

<span data-ttu-id="72c92-104">Especifica si un estilo que no es de color tiene el estilo de cursiva.</span><span class="sxs-lookup"><span data-stu-id="72c92-104">Specifies whether a non-color style has the italic style.</span></span>

## <a name="syntax"></a><span data-ttu-id="72c92-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72c92-105">Syntax</span></span>


```C++
BOOL __cdecl FItalicIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="72c92-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72c92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72c92-107">*pimestyle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="72c92-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72c92-108">Una estructura **IMESTYLE** devuelta por la función [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="72c92-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72c92-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72c92-109">Return value</span></span>

<span data-ttu-id="72c92-110">**True** si el estilo tiene el estilo de cursiva.</span><span class="sxs-lookup"><span data-stu-id="72c92-110">**TRUE** if the style has the italic style.</span></span>

## <a name="remarks"></a><span data-ttu-id="72c92-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72c92-111">Remarks</span></span>

<span data-ttu-id="72c92-112">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="72c92-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="72c92-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72c92-113">Requirements</span></span>



| <span data-ttu-id="72c92-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="72c92-114">Requirement</span></span> | <span data-ttu-id="72c92-115">Value</span><span class="sxs-lookup"><span data-stu-id="72c92-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72c92-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="72c92-116">DLL</span></span><br/> | <dl> <span data-ttu-id="72c92-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72c92-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72c92-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="72c92-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72c92-119">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="72c92-119">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
