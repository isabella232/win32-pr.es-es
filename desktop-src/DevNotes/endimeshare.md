---
description: Finaliza el recurso compartido de IME.
ms.assetid: aa33b5ed-fd4a-4829-9b7f-d545a4e7bd02
title: EndIMEShare función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 2a0d246537f2788afbb200cd35a81f7d6809ad89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660165"
---
# <a name="endimeshare-function"></a><span data-ttu-id="ed800-103">EndIMEShare función)</span><span class="sxs-lookup"><span data-stu-id="ed800-103">EndIMEShare function</span></span>

<span data-ttu-id="ed800-104">Finaliza el recurso compartido de IME.</span><span class="sxs-lookup"><span data-stu-id="ed800-104">Terminates IME Share.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed800-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed800-105">Syntax</span></span>


```C++
void __cdecl EndIMEShare(void);
```



## <a name="parameters"></a><span data-ttu-id="ed800-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed800-106">Parameters</span></span>

<span data-ttu-id="ed800-107">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ed800-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ed800-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed800-108">Return value</span></span>

<span data-ttu-id="ed800-109">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ed800-109">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed800-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed800-110">Remarks</span></span>

<span data-ttu-id="ed800-111">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="ed800-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="ed800-112">Se debe llamar a esta función después de que se llame a la última función de recurso compartido de IME.</span><span class="sxs-lookup"><span data-stu-id="ed800-112">This function should be called after the last IME Share function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed800-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed800-113">Requirements</span></span>



| <span data-ttu-id="ed800-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed800-114">Requirement</span></span> | <span data-ttu-id="ed800-115">Value</span><span class="sxs-lookup"><span data-stu-id="ed800-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed800-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ed800-116">DLL</span></span><br/> | <dl> <span data-ttu-id="ed800-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed800-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed800-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed800-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed800-119">**FInitIMEShare**</span><span class="sxs-lookup"><span data-stu-id="ed800-119">**FInitIMEShare**</span></span>](finitimeshare.md)
</dt> </dl>

 

 
