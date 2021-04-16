---
description: Especifica si un estilo que no es de color tiene un estilo de subrayado.
ms.assetid: 452dda6e-b12b-457c-9a01-c5363359c9f5
title: FUlIMEStyle función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: a49090d2ca192dfd3ec6d0064b92bd2233af79c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649681"
---
# <a name="fulimestyle-function"></a><span data-ttu-id="667a5-103">FUlIMEStyle función)</span><span class="sxs-lookup"><span data-stu-id="667a5-103">FUlIMEStyle function</span></span>

<span data-ttu-id="667a5-104">Especifica si un estilo que no es de color tiene un estilo de subrayado.</span><span class="sxs-lookup"><span data-stu-id="667a5-104">Specifies whether a non-color style has an underline style.</span></span>

## <a name="syntax"></a><span data-ttu-id="667a5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="667a5-105">Syntax</span></span>


```C++
BOOL __cdecl FUlIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="667a5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="667a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="667a5-107">*pimestyle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="667a5-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="667a5-108">Una estructura **IMESTYLE** devuelta por la función [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="667a5-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="667a5-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="667a5-109">Return value</span></span>

<span data-ttu-id="667a5-110">TRUE si el estilo tiene un estilo de subrayado.</span><span class="sxs-lookup"><span data-stu-id="667a5-110">TRUE if the style has an underline style.</span></span>

## <a name="remarks"></a><span data-ttu-id="667a5-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="667a5-111">Remarks</span></span>

<span data-ttu-id="667a5-112">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="667a5-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="667a5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="667a5-113">Requirements</span></span>



| <span data-ttu-id="667a5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="667a5-114">Requirement</span></span> | <span data-ttu-id="667a5-115">Value</span><span class="sxs-lookup"><span data-stu-id="667a5-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="667a5-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="667a5-116">DLL</span></span><br/> | <dl> <span data-ttu-id="667a5-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="667a5-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="667a5-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="667a5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="667a5-119">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="667a5-119">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
