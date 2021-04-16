---
description: Especifica si un estilo que no es de color tiene el estilo de negrita.
ms.assetid: fd34af7f-8847-43aa-9e69-264a08eba98b
title: FBoldIMEStyle función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FBoldIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: f54e62feae710dd51cae688d380ccf7da1eda4d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650055"
---
# <a name="fboldimestyle-function"></a><span data-ttu-id="33446-103">FBoldIMEStyle función)</span><span class="sxs-lookup"><span data-stu-id="33446-103">FBoldIMEStyle function</span></span>

<span data-ttu-id="33446-104">Especifica si un estilo que no es de color tiene el estilo de negrita.</span><span class="sxs-lookup"><span data-stu-id="33446-104">Specifies whether a non-color style has the bold style.</span></span>

## <a name="syntax"></a><span data-ttu-id="33446-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33446-105">Syntax</span></span>


```C++
BOOL FBoldIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="33446-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33446-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33446-107">*pimestyle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33446-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33446-108">Una estructura **IMESTYLE** devuelta por la función [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="33446-108">An **IMESTYLE** structure returned from the [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33446-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="33446-109">Return value</span></span>

<span data-ttu-id="33446-110">**True** si el estilo tiene el estilo de negrita.</span><span class="sxs-lookup"><span data-stu-id="33446-110">**TRUE** if the style has the bold style.</span></span>

## <a name="remarks"></a><span data-ttu-id="33446-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33446-111">Remarks</span></span>

<span data-ttu-id="33446-112">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="33446-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="33446-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33446-113">Requirements</span></span>



| <span data-ttu-id="33446-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="33446-114">Requirement</span></span> | <span data-ttu-id="33446-115">Value</span><span class="sxs-lookup"><span data-stu-id="33446-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33446-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="33446-116">DLL</span></span><br/> | <dl> <span data-ttu-id="33446-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33446-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33446-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="33446-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33446-119">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="33446-119">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
